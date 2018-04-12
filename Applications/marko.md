# Marko

Architectures based on UI components have become the predominant paradigm for
building modern web applications. UI components simplify web application
development by providing encapsulation and UI components are typically
independently testable. There are many libraries out there that provide
solutions for building UI components, each with their own strengths and
weaknesses. [Marko](https://markojs.com/) is a library for building UI components
with the following strengths:

- Minimal boilerplate for users
- Lightweight runtime for the browser (around 10kb gzip)
- Changes to state or input result in automatic updates to the view
- Async and streaming server-side rendering (under Node.js)
- Smart compiler with advanced compile-time optimizations
- Best-in-class rendering performance on the server and in the browser
- Both single and multi-file UI components
- Isomorphic UI components
- When utilizing server-side rendering, the UI component tree is automatically
recreated in the browser when the page boots in the browser
- No references to “Marko” in user code
- Offers both a familiar HTML syntax and a concise, indentation based syntax
- Supports shorthands based on CSS selectors for assigning IDs and classes
to HTML elements

## History

Marko has a long history within eBay, dating back to around 2012 when we started
exploring using Node.js as our web application development stack. This was at a
time when JavaScript templating was starting to take off. At eBay, server-side
rendering was very important and we wanted support for UI components and
asynchronous rendering. Dust.js was used by a few teams because it offered
streaming and async rendering, but it lacked support for UI components. Dust.js
also provided very few hooks to optimize templates at compile-time and it
promoted what we considered the bad practice of global helpers. eBay open
sourced a JavaScript toolkit named RaptorJS that included a very early version
of Marko called Raptor Templates. RaptorJS is now defunct, but many of the
modules that were part of RaptorJS now live on as independent projects (including Marko).

Marko has evolved a lot over the years. Marko has always had very strong
performance on the server, but many other features came later and were inspired
by other UI libraries/frameworks. For example, after React was announced and
gained popularity due to VDOM rendering and diffing, we also introduced VDOM
rendering and DOM diffing/patching into Marko to avoid manual DOM manipulation
and we also introduced virtual DOM rendering into Marko. Internal state for UI
components was inspired by React and Vue. Single file UI components was inspired
by single file UI components in Vue and Riot.js. Marko has always aimed to stay
competitive with other UI libraries by innovating and closely following industry
trends while also focusing on keeping the runtime fast and small.

Marko is now heavily used within eBay and it is also starting to be used by
outside companies, startups, government agencies and educational institutions.
The Marko ecosystem has continued to grow and Marko is supported in many
different IDEs, editors, and services like GitHub support syntax highlighting
for .marko files. The core Marko team has continued to grow and it consists of a
mix of eBay employees and outside developers.

## Metrics

At last count, there are over 13,000 unique Marko pages and UI components at eBay.
We are seeing [over 200,000 downloads from npm per month](https://npm-stat.com/charts.html?package=marko).
Marko (and Node.js) are used by the majority of teams working on building the
web applications that are part of ebay.com. As a vanity metric, Marko has reached
5,000 stars on GitHub and the star count has accelerated in recent months
(see [star chart](https://starcharts.herokuapp.com/marko-js/marko)). We have over
500 people in our [public Gitter chat room](https://gitter.im/marko-js/marko).
From interactions with the Marko community, we know that there are at least a
handful of large enterprises using Marko in varying degrees.

Feedback on social media has been mostly positive:

- [Hacker News: Marko – An isomorphic UI framework similar to Vue](https://news.ycombinator.com/item?id=15057371)
- [Hacker News: Vue.js vs. React](https://news.ycombinator.com/item?id=15054009)
- [Reddit: Marko 4.0 released - the friendly and fast UI library from eBay](https://www.reddit.com/r/javascript/comments/5xgk9q/marko_40_released_the_friendly_and_fast_ui/)
- [Reddit: Marko is a friendly (and fast!) UI library that makes building web apps fun.](https://www.reddit.com/r/webdev/comments/6vapeb/marko_is_a_friendly_and_fast_ui_library_that/)
- [Marko 4.0 is here – Michael Rawlings – Medium](https://medium.com/@mlrawlings/marko-4-0-is-here-837884c5f60d)
- [Marko vs React: An In-depth Look – Hacker Noon](https://hackernoon.com/marko-vs-react-an-in-depth-look-767de0a5f9a6)
- [Why is Marko Fast? – Hacker Noon](https://hackernoon.com/why-is-marko-fast-a20796cb8ae3)
- [Server-side Rendering Shootout with Marko, Preact ... - Hacker Noon](https://hackernoon.com/server-side-rendering-shootout-with-marko-preact-rax-react-and-vue-25e1ae17800f)
- [Building the UI - a comparison of React, Vue, and Marko - YouTube](https://www.youtube.com/watch?v=i6eZA8Y_GgA&feature=youtu.be)
- [10 Awesome Marko Features](https://medium.com/@austinkelleher/10-awesome-marko-features-afba9d094d42)

## Project Scope

Marko wants to help developers quickly create high performance web applications
that are maintainable. We want Marko to have a minimal learning curve and we
want it to be easy for developers to get started if they already know HTML, CSS
and JavaScript. Marko is much more than an HTML templating language, and we allow
developers to utilize almost all of the full power of JavaScript within a Marko
template. We want Marko to evolve quickly with minimal breaking changes by taking
advantage of our smart compiler. We want to support and interop with the latest
web platform technologies wherever possible.

## Current Governance Process

The Marko core team builds features and determines direction based on getting
consensus from the core team. All members of the core team must agree before we
add a new developer to the core team. We review each other’s pull requests
and we openly solicit input from the community whenever it makes sense. We aim
to be as transparent as possible.

## Current Contribution Process

Please see: [Marko: Contribution tips and guidelines](https://github.com/marko-js/marko/blob/master/.github/CONTRIBUTING.md)

## Current Project Tooling

- GitHub organizations:
  - [https://github.com/marko-js](https://github.com/marko-js)
  - [https://github.com/marko-js-samples](https://github.com/marko-js-samples)
- GitHub is used for all issue tracking
- GitHub Pages is used to host [markojs.com](https://markojs.com)
- Gitter is used for our public chat room: https://gitter.im/marko-js/marko

## Existing IP

- Domain name: [markojs.com](https://markojs.com)
- Logo: https://github.com/marko-js/branding

## Initial Project Collaborators and Maintainers

- [Patrick Steele-Idem](https://github.com/patrick-steele-idem) (Twitter: [@psteeleidem](https://twitter.com/psteeleidem))
- [Michael Rawlings](https://github.com/mlrawlings) (Twitter: [@mlrawlings](https://twitter.com/mlrawlings))
- [Austin Kelleher](https://github.com/austinkelleher) (Twitter: [@austinkelleher](https://twitter.com/austinkelleher))
- [Dylan Piercey](https://github.com/DylanPiercey) (Twitter [@dylan_piercey](https://twitter.com/dylan_piercey))
- [Phillip Gates-Idem](https://github.com/philidem) (Twitter: [@philidem](https://twitter.com/philidem))
- [Martin Aberer](https://github.com/tindli) (Twitter: [@metacoffee](https://twitter.com/metacoffee))
- [Jason MacDonald](https://github.com/jasonmacdonald)

## CLA

This project plans to use the [JSF CLA](https://cla.js.foundation/).

## License

MIT License

## Code of Conduct

This project plans to adhere to the [JSF Code of Conduct](https://js.foundation/community/code-of-conduct). Currently using [eBay Code of Conduct](http://ebay.github.io/codeofconduct).
