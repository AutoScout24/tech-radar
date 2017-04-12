# AutoScout24 Technology Radar

* [AutoScout24 Radar Nov 2016 (current)](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F16eELLsZvDuRfBf-YryEXD8UjQlmmRivr3GX919O5V0k%2Fedit%23gid%3D0)
* [AutoScout24 Radar Apr 2016](http://autoscout24.github.io/tech-radar-2016/)

### Defaults
Blips that are adopted at AutoScout24 by default and are not mentioned in every radar.

#### Techniques
* Blue/Green Deployment
* Continuous Delivery
* Infrastructure as Code
* Avoid Lockstep Releases
* Two-Factor auth. for everyone where possible
* Shadow Traffic

#### Platform
* Node Js as build tools
* AWS
* Serverless architecture
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
* Data Dog

#### Languages & Frameworks
* SCALA
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
* Spinnaker (ASSESS)
* ElasticSearch Watcher (ASSESS) - We also have put "Log everything" on hold. Use metrics for metrics and not logging for metrics.
* Cassandra (ASSESS) - Currently no use case
* X-Pack Graph (ASSESS) - To expensive
* Protobuf (ASSESS) - Avro in trial
* Thrift (ASSESS) - Avro in trial
* Ratpack (ASSESS) - Nobody investigated
