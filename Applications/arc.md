*JS Foundation Project Proposal*

# arc
 
> `arc` is a text format and collection of tools for enabling architecture as text for repeatable, disposable, and remixable _functions as a service_.
 
- Version control your app architecture and generate cloud infrastructure in `.arc` text files
- Rapidly provision, deliver and deploy cloud functions
- Iterate faster with more frequent and lower-risk releases
- Ship with the confidence of cloud scalability, availability, and security
- Avoid vendor lock-in by focusing on application architecture instead of vendor infrastructure
 
`arc`’s text format and subsequent tooling is completely vendor neutral. Currently, arc only supports Amazon Web Services.

## History
 
In December 2015, we began development of begin.com, a productivity application and platform. Looking to the future, it seemed clear that the cloud was right way to deliver our software. Considering the state of the cloud in 2015, it was also very clear that functions as a service was going to become a very compelling development model.
 
We decided to completely adopt the cloud and functions as a service into our application architecture, estimating that during the expected timeline of our development, both would mature significantly and likely convey an advantage for getting to and competing in an already fiercely established market. 
 
However, in the first year of our development we found tooling in the cloud ecosystem to be largely immature, vendor specific, and, worse, too often closely emulating defunct server metaphors. In order to build our product, we eventually came to the determination that we needed tooling capable of addressing the specific kinds of problems a microservices-based application architecture will inevitably surface. 
 
Fast forward to June of 2017: begin.com is in alpha, and we’re in a position to share our experiences in building microservices-based applications, and to open and donate our related tooling with the broader free/open source software developer community.
We believe that architectural and infrastructure tooling should be open source for a host of reasons. It is proven that many eyeballs make bugs (and security holes) very shallow. A large community also brings the potential of cloud platform portability. However most importantly, philosophically we believe the existence of a devops focused, vendor-neutral microservices tooling solution, with open and transparent community governance, can be a rising tide that will lift all ships.
 
## Metrics
 
Some portions of what we’re now calling `arc` have been open source for a while. Our first foray is a simple wrapper library that has relatively small user base (which may be largely comprised of begin.com’s continuous integration systems).
 
- https://github.com/smallwins/lambda
- https://npm-stat.com/charts.html?package=%40smallwins%2Flambda
 
However, we think that’s totally ok, and that the effort is still worth our while. It’s very early days for the idea of _functions as a service_, and we believe the JS Foundation is the right place to grow this solution. 
 
### Ecosystem
 
The cloud ecosystem is very large and is growing fast. First-generation cloud solutions that use traditional server-based metaphors aren’t appropriate targets for `arc`, even if they offer elastic scaling of virtual machine instances based on demand (or orchestrate containers).
 
These types of solutions are anchored in an incompatible server metaphor and applying this abstraction would be leaky. 
 
The kinds of infrastructure solutions we believe would be better targets include:
 
- Amazon Web Services Lambdas
- Microsoft Azure Cloud Functions
- IBM OpenWhisk 
- Google Cloud Platform Cloud Functions
 
Other, possibly more interesting, but smaller vendors’ solutions include: 
 
- Stripe Runkit
- Twilio Functions
- stdlib.io
- iron.io
- webtask.io
 
Frameworks/tooling alternatives to `arc` include:
 
- Serverless Framework
- Terraform
- AWS SAM (Cloudformation™)
 
The developer community understands _open_ means *open governance*, and not just a LICENSE file on Github, which is why we believe this kind of tooling should not be tied to any one company.
 
## Project Scope

`arc` is a text format and collection of command line tools implemented in Node. 
 
- `.arc` - text format specification 
- `arc-parser` - parses `.arc` text format into a javascript object
- `arc-create` - generates local code and related infrastructure if it does not yet exist
- `arc-prototype` - accepts vanilla javascript function(s) and returns it wrapped with an aws lambda function signature [Plan to rename! This was the original repo.]
- `arc-offline` - runs infrastructure offline (specifically: lambdas handlers for json/html http endpoints and in memory db tables/indexes for running tests …very fast)
- `arc-deploy` - deploys one or all functions in `./src` in parallel; a typical deployment of a dozen endpoints takes about 10 seconds, with zero downtime
- `arc-www` - docs website (built with `.arc` of course)

Possibly noticable in its absence is tooling for taking down generated deployment infrastructure. Nothing is ever destroyed programmically and things are only ever created by `arc-create` if they do not yet exist. Maybe in the future we will add destructive actions to make one off testing easier but so far a manually handling destructive actions has worked well enough for us. The  workflow ends up being incremental. You make small edits to `.arc` and `npm run create` to generate local code and remote infra as you go. 

Here is an example `.arc` file:

```bash
# arc manifest format supports comments
@app
hello-world  # an app name is required; it gets used for the generated infra

# routes will map to lambdas
@html
get /
get /hello
post /like

@json
get /api/likes
get /api/likes/:likeID
post /api/likes
post /api/likes/:likeID
post /api/likes/:likeID/delete # arc only supports get/post http verbs (like browsers!)

@events
hit-counter

@tables
likes
  likeID *String
```

`arc-create` is an npm script. if you add it and `npm run create` the `.arc` file above would generate the following local code:

```
/
|-src
| |-html
| | |-get-index
| | |-get-hello
| | '-post-like
| |-json
| | |-get-api-likes
| | |-get-api-likes-000likeID
| | |-post-api-likes
| | |-post-api-likes-000likeID
| | '-post-api-likes-000likeID-delete
| '-events
|   '-hit-counter
|-.arc
'-package.json
```

It gets better. `arc-create` would also ensure the corosponding lambdas are created, endpoints wired, permissions set and immediately ready for deployment to two identical environments for `staging` and `production`. You can delete the infrastructure anytime and re-run `arc-create` to regenerate it from your local source. The `.arc` above would generate the following infra:

##### API Gateway APIs

- `hello-world-staging`
- `hello-world-production`

`@html` lambda route handlers work very similarily to Express. Responses can be one of 200, 302, 404 or 500 status codes. Sessions are supported by default. `@json` works the same (except `content-type` is `application/json` instead of `html/text`).

##### API Gateway Invoked Lambdas

- `hello-world-staging-get-index`
- `hello-world-staging-get-hello`
- `hello-world-staging-post-like`
- `hello-world-production-get-index`
- `hello-world-production-get-hello`
- `hello-world-production-post-like`
- `hello-world-staging-get-api-likes`
- `hello-world-staging-get-api-likes-000likeID`
- `hello-world-staging-post-api-likes`
- `hello-world-staging-post-api-likes-000likeID`
- `hello-world-staging-post-api-likes-000likeID-delete`
- `hello-world-production-get-api-likes`
- `hello-world-production-get-api-likes-000likeID`
- `hello-world-production-post-api-likes`
- `hello-world-production-post-api-likes-000likeID`
- `hello-world-production-post-api-likes-000likeID-delete`
 
##### SNS Event Triggered Lambdas

- `hello-world-staging-hit-counter`
- `hello-world-production-hit-counter`

##### DynamoDB Tables 

> Additionally `.arc` supports DynamoDB table indexes and lambdas triggered by insert, update and delete events.

- `hello-world-staging-likes`
- `hello-world-producion-likes`

---

This is getting a lot of finicky configuration work done very quickly. Isolation of the runtime infrastructure between `staging` and `production` makes deployment trivially automatable and worry free. The architecture is safely revisioned in `.arc` and easily reproduced (which can be helpful across availability zones or even for just spinning up a disposable demo version of an app).

## Current Governance and Contribution Policy

Begin (Small Wins, Inc.) has a Code of Conduct and Contribution Guidelines. All code is to be available under the Apache 2.0 license.
 
Commit rights are currently granted to anyone:
 
1. That signs the CLA (we plan to use the foundation template and link it in the docs)
2. Has proven an interest
3. Demonstrates alignment with the project values
4. Agrees to the Code of Conduct and Contribution Guidelines
 
## Current Tooling and Infra

- Github
- Codeship
- npm 
 
## Initial Project Collaborators and Maintainers

- Angelina Fabbro
- Brian LeRoux
- Jen Fong-Adwent
- Kristofer Joseph
- Ryan Block
 
## Existing IP

No trademarks, domain names, or other assets beyond source code and docs.
