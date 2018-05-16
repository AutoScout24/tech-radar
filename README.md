# AutoScout24 Technology Radar

* [AutoScout24 Radar Apr 2018 (current)](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F1EHsJBo14TBKZqEPrzWJLEjkuMzpo6ID3p_u91sPyxzc)
* [AutoScout24 Radar Sep 2017](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F1qurHghIJVEMTIu0gyCgSEK7pqa3tCnYHmxyG-a7JuE0)
* [AutoScout24 Radar Apr 2017](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F1Qn4O4xft4AvPfxkgz2HHtyC7MDUmG4GTkNUkPXxJ8B8%2Fpubhtml)
* [AutoScout24 Radar Nov 2016](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F16eELLsZvDuRfBf-YryEXD8UjQlmmRivr3GX919O5V0k%2Fedit%23gid%3D0)
* [AutoScout24 Radar Apr 2016](http://autoscout24.github.io/as24-tech-radar-2016/)

## Defaults
Blips that are adopted at AutoScout24 by default and are not mentioned in every radar. Most of them are motivated by our
[Scout24 IT principals](https://github.com/AutoScout24/scout24-it-principles).

#### Techniques
* Blue/Green Deployment
* [Continuous Delivery](https://martinfowler.com/bliki/ContinuousDelivery.html)
*<br>Continuous delivery is our  software engineering approach to support teams in producing software in short cycles and
ensuring that the software can be reliably released at any time.*
* [Infrastructure as Code](https://www.thoughtworks.com/de/insights/blog/infrastructure-code-reason-smile)
*<br>We manage, provision and automate all computer data centers and cloud infrastructure through machine-readable definition
files: reproducible, traceable, auditable and tested.*
* Avoid Lockstep Releases
* Two-Factor auth. for everyone where possible
* Shadow Traffic

#### Platforms
* Node Js as build tools
* [Amazon Web Services - AWS](https://aws.amazon.com/)
*<br>AWS is our preferred, reliable, scalable, and inexpensive cloud computing service powered by Amazon. We choose AWS
platform service over managed service, over self-hosted OSS and over self built solutions.*
* [Serverless Architectures](https://martinfowler.com/articles/serverless.html)
*<br>We build applications with custom code that is run in ephemeral containers operated by a service provider. These
systems significantly reduce operational cost and complexity. Amazon Lambda and Amazon ECS are two examples for
serverless services.*
* Q.A. in Production</br>
*With the rise of Continuous Delivery, the QA role is shifting to include analyzing software product quality in production. This involves monitoring of the production systems, coming up with alert conditions to detect urgent errors, determining ongoing quality issues and figuring out what measurements you can use in the production environment to make this work. This does not mean that pre-production QA is not needed anymore.*
* <a href="https://http2.github.io/">HTTP/2</a></br>
*is the next revision of HTTP. Improves user perceived latency.*
* <a href="https://auth0.com/">Auth0</a></br>
*For us it's important to authenticate users of internal systems against our active directory. Also, 2FA authentication becomes mandatory. Auth0 makes it easy to integrate with, supports all needed protocols and provides custom rules to enrich the authentication flow.*

#### Tools
* Nexus
* Elastic Search
* Kibana
* Ops Genie
* Git
* SBT
* Dashing.IO
* [Datadog](https://www.datadoghq.com)</br>
*We use Datadog as our monitoring service for cloud-scale applications. We bring together data from servers,
databases, tools, and services to present a unified view of our entire stack and to raise alarms.*
* Security Monkey</br>
*We are using Security Monkey for auditing our security relevant resources in AWS. It has proven to be a reliable and helpful tool and led to improved overall security.*
* Kafka</br>
*We chose Kafka for our internal data enrichment pipelines. The lack of the log compaction feature in AWS Kinesis led us to roll our own solution.*
* Chaos Monkey</br>
*Testing our systems for resiliency is important to us. Chaos Monkey randomly kills machines in our live environment and helps us finding and preventing shortcomings in our service setup. <a href="http://principlesofchaos.org">http://principlesofchaos.org</a>*
* <a href="https://github.com/awslabs/git-secrets">git-secrets</a></br>
*To prevent secrets leaking on GitHub we are scanning our repositories with git-secrets. Compared to gitrob this tool also scans the file contents and can work preemptively as a pre-commit hook.*
* <a href="https://travis-ci.org/">Travis CI</a> for OSS</br>
*TravisCI is one of these tools which supports configuration as code. It's widely adopted, especially in OSS. It can be used as SaaS or On-Prem. We use it for Open Source projects only.*
* <a href="https://www.webpagetest.org/">WebPageTest.org</a></br>
*WebPageTest is used by our teams to evaluate the page performance in our pipelines.*
* <a href="https://www.cloudhealthtech.com/solutions/enterprise">CloudHealth</a></br>
*is a service to optimize the cloud usage in many aspects including costs.*


#### Languages & Frameworks
* Scala
* Javascript
* REST API (Public)
* SCSS
* ShowCar
* Play Framework
* EcmaScript 6
* <a href="http://metrics.dropwizard.io/">Codahale Metrics</a></br>
*Dropwizard Metrics (aka Codahale Metrics) allows to easily create custom application-level metrics and export them with JMX to DataDog*
* <a href="http://www.scalatest.org/">ScalaTest</a></br>
*We choose ScalaTest as our primary Scala testing tool. It's easy to pick up and supports test styles that are familiar to most developers coming from other languages.*
* Swift</br>
*We choose ScalaTest as our primary Scala testing tool. It's easy to pick up and supports test styles that are familiar to most developers coming from other languages.*
* espresso test</br>
*Andriod UI tests*
* XcuiTest</br>
*iOS UI Tests*
* Redux</br>
*Ported from the <a href="http://elm-lang.org/">elm</a> language, <a href="">Redux</a> is the standard for state-managment in the JS world. It allows for very clear top-down one-way data flow, state tracking, and isolated side-effects, together with amazing developer tools (i.e <a herf="https://github.com/zalmoxisus/remote-redux-devtools">remote devtools</a>, <a href="https://www.youtube.com/watch?v=xsSnOQynTHs">Time travel</a>, <a href="https://logrocket.com/">Bug reporting</a>). Use is highly encouraged in any JS SPA, specially in combination with React.*



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
