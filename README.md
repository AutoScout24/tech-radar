# AutoScout24 Technology Radar

**Note:** this repository is out-of-date (last update 2018). We are working on a updated version and will release it as soon as it's ready.

## Previous versions

* [AutoScout24 Radar Feb 2018](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2FScout24%2Fas24-tech-radar%2Fmaster%2Fradars%2FAutoScout24%2520Radar%2520Feb%25202018%2520.csv) ([changes since previous version](https://github.com/Scout24/as24-tech-radar/blob/master/radars/AutoScout24%20Radar%20Feb%202018%20Changes.md))
* [AutoScout24 Radar Sep 2017](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2FScout24%2Fas24-tech-radar%2Fmaster%2Fradars%2FAutoScout24%2520Radar%2520Sep%25202017%2520.csv) ([changes since previous version](https://github.com/Scout24/as24-tech-radar/blob/master/radars/AutoScout24%20Radar%20Sep%202017%20Changes.md))
* [AutoScout24 Radar Apr 2017](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2FScout24%2Fas24-tech-radar%2Fmaster%2Fradars%2FAutoScout24%2520Radar%2520Apr%25202017%2520.csv) ([changes since previous version](https://github.com/Scout24/as24-tech-radar/blob/master/radars/AutoScout24%20Radar%20Apr%202017%20Changes.md))
* [AutoScout24 Radar Nov 2016](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2FScout24%2Fas24-tech-radar%2Fmaster%2Fradars%2FAutoScout24%2520Radar%2520Nov%25202016%2520.csv) ([changes since previous version](https://github.com/Scout24/as24-tech-radar/blob/master/radars/AutoScout24%20Radar%20Nov%202016%20Changes.md))
* [AutoScout24 Radar Q1 2016](http://scout24.github.io/as24-tech-radar-q1-2016/)

## Defaults

Blips that are adopted at AutoScout24 by default and are not mentioned in every radar. Most of them are motivated by our
[Scout24 IT principals](https://github.com/AutoScout24/scout24-it-principles).

#### Techniques

* **[Blue-Green Deployment](https://martinfowler.com/bliki/BlueGreenDeployment.html)**: Blue-green deployment is a technique that reduces downtime and risk by having second production environments running and switching traffic from one to another during deployment.
* **[Continuous Delivery](https://martinfowler.com/bliki/ContinuousDelivery.html)**: Continuous delivery is our software engineering approach to support teams in producing software in short cycles and ensuring that the software can be reliably released at any time.
* **[Infrastructure as Code](https://www.thoughtworks.com/de/insights/blog/infrastructure-code-reason-smile)**: We manage, provision and automate all computer data centers and cloud infrastructure through machine-readable definition files: reproducible, traceable, auditable and tested.
* **Shadow Traffic**: Testing new services with natural traffic has proven to be a reliable method. Replicating traffic to the shadowed system is easy to implement and allows to test system in real life situations under real load.
* **Feature Toggles**: There couldn't be a better explanation: [Pete Hodgson on Martin Fowler's Bliki - Feature Toggles](http://martinfowler.com/articles/feature-toggles.html). As we put more and more services into production in new teams, we need emphasize the proper way: The first task in every new story should be to create the release toggle and you are only done, when the toggle is removed.
* **[Circuit breaker](https://martinfowler.com/bliki/CircuitBreaker.html)**: Circuit breaker is a stability pattern for distributed systems. We tried [Hystrix](https://github.com/Netflix/Hystrix) and [Akka Circuit Breaker](http://doc.akka.io/docs/akka/current/common/circuitbreaker.html). Hystrix came out as our default circuit breaker tool.
* **QA in production**: With the rise of Continuous Delivery, the QA role is shifting to include analyzing software product quality in production. This involves monitoring of the production systems, coming up with alert conditions to detect urgent errors, determining ongoing quality issues and figuring out what measurements you can use in the production environment to make this work. This does not mean that pre-production QA is not needed anymore.
* **Pre-compute as much as you can**: Many parts of our web site are read heavy, so in a lot of places it makes sense to pre-compute instead of reacting to a request. Examples would be change propagation for listings, static content and CQRS.
* **Logging using STDOUT**: All running processes log to STDOUT and we use logshipping to export data. As this is industry standard ([twelve-factor apps](https://12factor.net/)) we also switch to this approach. This also helps with our adoption of Docker on ECS/Infinity.
* **State management in the frontend**: Managing, visualising & understanding how state changes in frontend applications is essential for rock solid applications that can scale and are bug-free. We use and strongly recommend [Redux](https://redux.js.org/) for both of our React & vanillaJS apps, which not only helps us tackle state management,  but also lets us implement a flux-like architecture with one-way data flow, isolated side effects via middleware and more.
* **[Multi-factor authentication](https://en.wikipedia.org/wiki/Multi-factor_authentication) where possible**: MFA seriously reduces the incidence of online identity theft and other online fraud, because the victim's password would no longer be enough to give an attacker permanent access to their information.

#### Tools

* **[Datadog](https://www.datadoghq.com)**: We use Datadog as a monitoring service for cloud-scale applications. We bring together data from servers,
databases, tools, and services to present a unified view of our entire stack, build dashboards, and to raise alarms.
* **[OpsGenie](https://www.opsgenie.com/)**: OpsGenie is a modern incident management platform for operating always-on services, empowering teams to plan their on-call duty and stay in control during incidents. If something is getting broken in the middle of the night, it's OpsGenie who wakes us to fix it.
* **[CloudHealth](https://www.cloudhealthtech.com/solutions/enterprise)**: We use CloudHealth to get insights into untilization of our provisioned AWS resources and associated costs.
* **[Chaos Monkey](https://github.com/Scout24/SimianArmy)**: Testing our platform for resiliency is important to us. Chaos Monkey randomly kills machines in our live environment and helps us finding and preventing shortcomings in our service setup. [More](https://principlesofchaos.org/) about principles of chaos.
* **[Cloud Custodian](https://github.com/capitalone/cloud-custodian)**: Rules engine allowing us to define policies for continous monitoring of our provisioned AWS resources in order to keep it well managed and secure.
* **[Kafka](https://kafka.apache.org/)**: We chose Kafka for our internal data pipelines. The lack of the log compaction feature in AWS Kinesis led us to roll our own solution.
* **[Elasticsearch](https://www.elastic.co/products/elasticsearch)**: Search on our platform is powered by Elasticsearch. We use it to store and search logs as well.
* **[Kibana](https://www.elastic.co/products/kibana)**: Given Elasticsearch for storing logs, Kibana is a natural fit for analyzing, navigating and visualising logs data.
* **[Nexus](https://www.sonatype.com/nexus-repository-sonatype)**: We use Nexus to store artifacts we build and as a proxy for Maven and npm repositories.
* **[sbt](https://www.scala-sbt.org/)**: We use sbt (stands for ~~**s**imple~~ **s**cala **b**uild **t**ool) to build our Scala code.
* **[git](https://git-scm.com/)**: Nowadays git is a de-facto standard for version control system, which outclasses other tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenient staging areas, and multiple workflows.
* **[git-secrets](https://github.com/awslabs/git-secrets)**: To prevent secrets leaking on GitHub we are scanning our repositories with git-secrets. Compared to other tools, this tool also scans the file contents and can work preemptively as a pre-commit hook.
* **[webpack](https://webpack.js.org/)**: webpack is a module bundler. Its main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packaging just about any resource or asset.
* **[Firebase](https://firebase.google.com/)**: We use Firebase to send push notifications to Android devices and gathering data about the user and his app usage.
* **[Travis CI](https://travis-ci.org/) for OSS**: Travis CI is one of these tools which supports pipeline configuration as code. It's widely adopted, especially in OSS and can be used as SaaS or on-premise. We use it for Open Source projects only.
* **[WebPageTest.org](https://www.webpagetest.org/)**: We use WebPageTest speed test from multiple locations around the globe using real browsers (IE and Chrome) and at real consumer connection speeds to evaluate performance of our platform and to monitor user experience our consumers are getting.
* **[Auth0](https://auth0.com/)**: For us it's important to authenticate users of internal systems against our active directory. Also, 2FA authentication becomes mandatory. Auth0 makes it easy to integrate with, supports all needed protocols and provides custom rules to enrich the authentication flow.

#### Platforms

* **[Amazon Web Services](https://aws.amazon.com/)**: AWS is our preferred, reliable, scalable, and inexpensive cloud computing service powered by Amazon. We choose AWS platform service over managed service, over self-hosted OSS and over self built solutions.
* **[Serverless Architectures](https://martinfowler.com/articles/serverless.html)**: We build applications with custom code that is run in ephemeral containers operated by a service provider. These systems significantly reduce operational cost and complexity. Amazon Lambda and Amazon ECS are two examples for serverless services.
* **[HTTP/2](https://http2.github.io/)** is the next revision of HTTP. The focus of the protocol is on performance; specifically, end-user perceived latency, network and server resource usage.
* **[Node.js](https://nodejs.org/) for frontend related builds**: The JavaScript ecosystem excels at providing tooling for bundling and packaging frontend-related code. In particular, webpack can transpile/bundle/minify/lint/format all frontend assets via a broad plugin ecosystem. As such, we recommend using it, together with plain npm scripts, even on non-nodeJS backend codebases such as Scala, instead of using Scala-based web plugins for managing frontend code.

#### Languages & Frameworks

* **[Scala](https://www.scala-lang.org/)**: Scala combines object-oriented and functional programming in one concise, high-level language. Scala's static types help avoid bugs in complex applications, and its JVM runtime let you build high-performance systems with easy access to huge ecosystems of libraries.
* **[ScalaTest](http://www.scalatest.org/)**: We chose ScalaTest as our primary Scala testing tool. It's easy to pick up and supports test styles that are familiar to most developers coming from other languages.
* **[Play Framework](https://www.playframework.com/)**: Play is based on a lightweight, stateless, web-friendly architecture. Built on Akka, Play provides predictable and minimal resource consumption (CPU, memory, threads) for highly-scalable applications.
* **[JavaScript](https://www.w3schools.com/js/)**: JavaScript is a high-level, interpreted programming language. It is a language which is also characterized as dynamic, weakly typed, prototype-based and multi-paradigm. JavaScript is easy to learn.
* **[EcmaScript 6](https://www.w3schools.com/js/js_es6.asp)**: ECMAScript 6 (ES6), later renamed to ECMAScript 2015 (ES2015), adds significant new syntax for writing complex applications, including classes and modules, but defines them semantically in the same terms as ECMAScript 5 strict mode. Other new features include iterators and for/of loops, Python-style generators, arrow functions, binary data, typed arrays, collections (maps, sets and weak maps), promises, number and math enhancements, reflection, and proxies (metaprogramming for virtual objects and wrappers).
* **[SCSS aka Sass](https://sass-lang.com/)**: Sass is the most mature, stable, and powerful professional grade CSS extension language in the world.
* **[Swift](https://developer.apple.com/swift/)**: Swift is a powerful and intuitive programming language for macOS, iOS, watchOS and tvOS. Swift is much easier to read and use than Objective C.
* **[XCUITest](https://developer.apple.com/library/content/documentation/developertools/conceptual/testing_with_xcode/chapters/09-ui_testing.html)**: XCUITest is the framework which allows you to easily develop UI tests that reflect users' interaction with the iOS applications.
* **[Kotlin](https://kotlinlang.org/)**: After Google announced first-class support for Kotlin on Android on Google I/O 2017, we had a look on Kotlin and were excited about it, so, Kotlin quickly became default choice for Android development.
* **[espresso test](https://developer.android.com/training/testing/espresso/)**: We use Espresso to write concise, beautiful, and reliable Android UI tests.
* **[ShowCar](https://github.com/Scout24/showcar-ui)**: showcar-ui is the pattern library that is used to build the frontend of AutoScout24. It provides CSS classes, custom elements and components.
* **[Redux](https://redux.js.org/)**: Ported from the [elm](http://elm-lang.org/) language, Redux is the standard for state-managment in the JavaScript world. It allows for very clear top-down one-way data flow, state tracking, and isolated side-effects, together with amazing developer tools (i.e. [remote devtools](https://github.com/zalmoxisus/remote-redux-devtools), [time travel](https://www.youtube.com/watch?v=xsSnOQynTHs), [bug reporting](https://logrocket.com/)). Use is highly encouraged in any JavaScript SPA, specially in combination with React.
* **[Codahale Metrics](http://metrics.dropwizard.io/)**: Dropwizard Metrics (aka Codahale Metrics) allows to easily create custom application-level metrics and export them with JMX to DataDog.

## Removed
Blips removed from the radar without being adopted.

* Background Sync (Service Worker) (ASSESS) - Duplicate: Progressive WebApps
* Visual Monitoring (ASSESS) - Unstable solutions make pain be high
* Elastic Beanstalk (TRIAL)
* Node.js for the backend (ASSESS)
* Unikernel (ASSESS)
* EMR for Spark (HOLD)
* Caddy Server (ASSESS)
* Gitrob (HOLD) - replaced by git-secret
* Codecept.js (HOLD)
* Spinnaker (ASSESS) - Spinnaker is centered around EC2 but our deployments are based on ASG and soon ECS Services
* ElasticSearch Watcher (ASSESS) - We also have put "Log everything" on hold. Use metrics for metrics and not logging for metrics.
* Cassandra (ASSESS) - Currently no use case
* X-Pack Graph (ASSESS) - To expensive
* Protobuf (ASSESS) - Avro in trial
* Thrift (ASSESS) - Avro in trial
* Ratpack (ASSESS) - Nobody investigated
* Decouple Build and Deploy Tool (ASSESS) - Currently not needed
* CMS Boxes misuse (HOLD) - No new misuses
* Gulp.js (ADOPT) - Still in use, but deprecated in favour of Webpack
* Crucible (TRIAL)
* Bluepill (ASSESS)
* GoCD (HOLD) - Still in use; Ongoing discussions
* Elastic.io (HOLD) - The ElasticSearch PaaS offering did not work out for our requirements
* Go for microservices (ASSESS)- Currently no further investigations
* Objective C (HOLD) - All new work is done in Swift
* Pact CDC (HOLD) - During our trial we learned that Pact CDC is cumbersome without also introducing Pact Broker. We stopped our attempts there.
