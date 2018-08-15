# Introduction and Project description.

Being a good web developer nowadays can be really challenging. 
Not only does one need to know about HTML, JavaScript, and CSS, 
but also about accessibility, security, performance, interoperability, 
responsive web design, PWAs, keep up with new standards and how 
to progressively enhance and gracefully degrade, polyfills, etc.. 
Of course, all this knowledge needs to get refreshed every few months 
because that’s how fast the web evolves.

It is impossible to know about everything, and finding the right 
guidance can be complicated too: StackOverflow questions might be 
outdated even if they are marked as correct, and with technical 
blogposts it’s even worse because there isn’t a community up/down 
voting.

Over the last few years there have been several tools that have helped 
developers write better code or catch issues, such as ESLint, stylelint, 
aXe, SSL Server Test, etc. Unfortunately there are still lots of areas 
that are not covered well enough. Additionally, these tools are not 
connected, thus, someone might know about one but not another, or new 
ones might pop up and will take a long time to get traction among the 
web community.

webhint's goal is to help developers write the best possible code 
throughout the entire life-cycle of a project (coding, testing, 
and maintenance) while making a big emphasys in educating why it 
is important. Also, it understands that not all developments are 
the same so it should be easy to configure and expand.

# Project history.

webhint's idea started initially by the Microsoft Edge Web Platform Team 
as a replacement for the current [static 
scanner](https://developer.microsoft.com/en-us/microsoft-edge/tools/staticscan/). 
While we were brainstorming we soon realized that this project should 
be community driven with the input of as many web actors as possible 
(browser vendors, web experts, etc.): the web belongs to all of us. 
In order to achieve this we believe it should be developed in a neutral 
place such as the JS Foundation with the right governance process.

Since then we've started prototyping the tool and reaching out to 
different browser vendors (Google, Mozilla, Samsung), that have show 
interest at different levels of the spectrum. 

# Any available metrics or even estimates about the user base, ecosystem and community.

Any web developer should use this tool so a few million people. Because 
webhint wants to be part of all the development process there will also be 
an online tool lowering the barrier to be used.

# Project scope.

webhint wants to:

* help developers write better code (more secure, accessible, faster)
* make the web a better place for everyone

webhint doesn't want to reinvent the wheel. When there are tools that 
already do a good job in one particular scenario it should integrate 
with them, and contribute back if needed.

# Current governance process.

There isn't one at the moment. The current one proposed by the JS 
Foundation where there can't be more than 1/3 of the people working 
for the same employer as part of the board seems a good one.

# Current contribution process.

There isn't a formal process at the moment, basically create issue, 
assign, and then submit a PR when done. There is a bit of planning 
every couple weeks to prioritize tasks and not a lot more.

# List of current tools in use by the project (forums, issue trackers, GitHub orgs, etc).

GitHub organization: [webhint](https://github.com/webhintio).
There is an Azure subscription to host the website that will also 
power the online service. Microsoft will be paying the bill for now. 
Other cloud services are welcome to contribute as well to we have a 
more diverse infrastructure.

# Existing IP Policy and relevant intellectual property (trademarks, domain names, etc).

Domain name: https://webhint.io

# List of initial Project Collaborators and Maintainers.

* [Antón Molleda](https://github.com/molant)
* [Cătălin Mariș](https://github.com/alrra)

# List of initial Working Groups, if any.

N/A

# CLA

Plan to use the JS Foundation one.

# License

Project is not OSS but would like it to be Apache 2.0 once it is in 
the foundation.

# Code of Conduct

> # Contributor Covenant Code of Conduct
> 
> ## Our Pledge
> 
> In the interest of fostering an open and welcoming environment, we
> as contributors and maintainers pledge to making participation in our
> project and our community a harassment-free experience for everyone,
> regardless of age, body size, disability, ethnicity, gender identity
> and expression, level of experience, nationality, personal appearance,
> race, religion, or sexual identity and orientation>.
> 
> ## Our Standards
> 
> Examples of behavior that contributes to creating a positive
> environment include:
> 
> * Using welcoming and inclusive language
> * Being respectful of differing viewpoints and experiences
> * Gracefully accepting constructive criticism
> * Focusing on what is best for the community
> * Showing empathy towards other community members
> 
> Examples of unacceptable behavior by participants include:
> 
> * The use of sexualized language or imagery and unwelcome sexual
>   attention or advances
> * Trolling, insulting/derogatory comments, and personal or political
>   attacks
> * Public or private harassment
> * Publishing others' private information, such as a physical or
>   electronic address, without explicit permission
> * Other conduct which could reasonably be considered inappropriate
>   in a professional setting
> 
> ## Our Responsibilities
> 
> Project maintainers are responsible for clarifying the standards
> of acceptable behavior and are expected to take appropriate and fair
> corrective action in response to any instances of unacceptable behavior.
> 
> Project maintainers have the right and responsibility to remove,
> edit, or reject comments, commits, code, wiki edits, issues, and other
> contributions that are not aligned to this Code of Conduct, or to ban
> temporarily or permanently any contributor for other behaviors that
> they deem inappropriate, threatening, offensive, or harmful.
> 
> ## Scope
> 
> This Code of Conduct applies both within project spaces and in public
> spaces when an individual is representing the project or its community.
> Examples of representing a project or community include using an
> official project e-mail address, posting via an official social media
> account, or acting as an appointed representative at an online or
> offline event. Representation of a project may be further defined and
> clarified by project maintainers.
> 
> ## Enforcement
> 
> Instances of abusive, harassing, or otherwise unacceptable behavior
> may be reported by contacting the project team at antonmo@microsoft.com
> or catalin.maris@microsoft.com. All complaints will be reviewed and
> investigated and will result in a response that is deemed necessary
> and appropriate to the circumstances. The project team is obligated
> to maintain confidentiality with regard to the reporter of an incident.
> Further details of specific enforcement policies may be posted separately.
> 
> Project maintainers who do not follow or enforce the Code of Conduct in
> good faith may face temporary or permanent repercussions as determined
> by other members of the project's leadership.
> 
> ## Attribution
> 
> This Code of Conduct is adapted from the [Contributor Covenant][homepage],
> version 1.4, available at [http://contributor-covenant.org/version/1/4][version]
> 
> [homepage]: http://contributor-covenant.org
> [version]: http://contributor-covenant.org/version/1/4/