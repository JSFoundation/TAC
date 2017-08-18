# Introduction and Project description.

WebdriverIO is an open source testing utility for nodejs. It makes it possible to write super easy selenium tests with Javascript in your favorite BDD or TDD test framework. It basically sends requests to a Selenium server or browser driver via the WebDriver Protocol and handles its response. These requests are wrapped in useful commands and can be used to test several aspects of your site in an automated way. Therefor it lets you control a browser or a mobile application with just a few lines of code. Your test code will look simple, concise and easy to read. The integrated test runner let you write asynchronous commands in a synchronous way so that you don’t need to care about how to handle a Promise to avoid racing conditions. Additionally it takes away all the cumbersome setup work and manages the Selenium session for you. WebdriverIO was designed to be as flexible and framework agnostic as possible. It can be applied in any context and serves not only the purpose of testing.

# Project history.

The project was initiated by Camilo Tapia (https://twitter.com/camilotapia) and was the first Selenium client library available on NPM. At that time it was called WebdriverJS (NPM package is still owned by the contributors: https://www.npmjs.com/package/webdriverjs). After the Selenium maintainer released an own tool called selenium-webdriver they started to promote it as WebdriverJS as well and labeled it as the “official bindings". With growing confusion in the user community about which project is WebdriverJS the maintainers decided to rebrand the project to WebdriverIO throughout all social media channels. It is gaining more and more popularity since then.

# Any available metrics or even estimates about the user base, ecosystem and community.

* NPM stats:
    * ~18k daily downloads (https://npm-stat.com/charts.html?package=webdriverio)
    * 148 dependent projects
    * Automation driver for tools like Spectron (official Electron Testing Framework maintained by GitHub), Chimp and CodeceptJS
* Gitter support Channel: ~1800 user (https://gitter.im/webdriverio/webdriverio)
* Most active authors

![Active users](https://mo.github.io/assets/javascript-e2e-integration-testing-active-devs.png)

# Project scope.

The goal of WebdriverIO is to provide developers a framework to run e2e tests on their desktop and mobile applications. It tries to simplify the test process by taking care of common pitfalls in e2e testing. It is not made to run any kind of other tests like unit or API tests. It only speaks the Webdriver protocol. However services and add ons may provide additional functionalities.

# Current governance process.

The project is currently governed by myself (Christian Bromann). I release all projects that are part of the WebdriverIO ecosystem (https://github.com/webdriverio) and answer most of the issue.

# Current contribution process.

No special process. People propose changes in form of pull requests on GitHub and I review and merge them. If someone shows constant support he/she will be added as project maintainer.

# List of current tools in use by the project (forums, issue trackers, GitHub orgs, etc).

Website: [http://webdriver.io/](http://webdriver.io/)<br>
GitHub Organisation: [https://github.com/webdriverio](https://github.com/webdriverio)<br>
Issue Tracker: [https://github.com/webdriverio/webdriverio/issues](https://github.com/webdriverio/webdriverio/issues)<br>
Twitter: [https://twitter.com/webdriverio](https://twitter.com/webdriverio)<br>
Gitter Channel: [https://gitter.im/webdriverio/webdriverio](https://gitter.im/webdriverio/webdriverio)<br>
VersionEye: [https://www.versioneye.com/](https://www.versioneye.com/)<br>
Travis CI: [https://travis-ci.org/webdriverio/webdriverio](https://travis-ci.org/webdriverio/webdriverio)<br>
Greenkeeper: [https://greenkeeper.io/](https://greenkeeper.io/)<br>
Code Climate: [https://codeclimate.com/github/webdriverio/webdriverio](https://codeclimate.com/github/webdriverio/webdriverio)

# Existing IP Policy and relevant intellectual property (trademarks, domain names, etc).

Domain [http://webdriver.io/](http://webdriver.io/) owned by Camilo Tapia

# List of initial Project Collaborators and Maintainers.

* [Camilo Tapia](https://github.com/camme)
* [Christian Bromann](https://github.com/christian-bromann)

# List of initial Working Groups, if any.

N/A

# CLA

Will be changed to the one provided by the JSFoundation once this project was approved by the working group.

# License

Currently [MIT](https://github.com/webdriverio/webdriverio/blob/master/LICENSE-MIT) but happy to switch it to Apache 2.0

# Code of Conduct

See [here](https://github.com/webdriverio/webdriverio/blob/master/CONDUCT.md)
