# AutoScout24 Technology Radar

* [AutoScout24 Radar Apr 2017 (current)](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F1Qn4O4xft4AvPfxkgz2HHtyC7MDUmG4GTkNUkPXxJ8B8%2Fpubhtml)
* [AutoScout24 Radar Nov 2016](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F16eELLsZvDuRfBf-YryEXD8UjQlmmRivr3GX919O5V0k%2Fedit%23gid%3D0)
* [AutoScout24 Radar Apr 2016](http://autoscout24.github.io/tech-radar-2016/)

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

#### Platform
* Node Js as build tools
* [Amazon Web Services - AWS](https://aws.amazon.com/)
*<br>AWS is our preferred, reliable, scalable, and inexpensive cloud computing service powered by Amazon. We choose AWS 
platform service over managed service, over self-hosted OSS and over self built solutions.*
* [Serverless Architectures](https://martinfowler.com/articles/serverless.html)
*<br>We build applications with custom code that is run in ephemeral containers operated by a service provider. These 
systems significantly reduce operational cost and complexity. Amazon Lambda and Amazon ECS are two examples for 
serverless services.*
* Azure AD
* CDN

#### Tools
* Nexus
* Elastic Search
* Kibana
* Ops Genie
* Git
* SBT
* Dashing.IO
* [Datadog](https://www.datadoghq.com)
*<br>We use Datadog as our monitoring service for cloud-scale applications. We bring together data from servers, 
databases, tools, and services to present a unified view of our entire stack and to raise alarms.*


#### Languages & Frameworks
* Scala
* Javascript
* REST API (Public)
* SCSS
* ShowCar
* Play Framework
* EcmaScript 6

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
