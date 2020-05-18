# Article - Buddy CICD SaaS

## Oveview

Buddy is a pretty intuitive Countinuous Integration and Countinuous Deployment \(CICD\) build server providing its offerings as a Software as a Service \(SaaS\). It is very developer friendly which I'm pretty sure you'd find convincing after reading through this article. What DigitalOcean does to Kubernetes is pretty much what Buddy does to CICD, something like "CICD for Dummies" on steriod.

## Pipelines & Actions

The concept of Buddy revolves around pipelines, which to my understanding really means a collection of actions you'd like to run to achieve an overall effect, eg. 

* Download my source code
* Download all of it's dependencies do a build 
* If build is ok, startup the server and run cypress tests
* If successfull, create a docker image
* If susccessfull push docker image to docker hub

Each points would possibly constitues an action

The nice things about Buddy's action is that there are plenty of them. All of them required filling in some texts fileds and then your are done. You will find actions \(docker images\) with cypress environment ready, kubernetes environment ready to stuff not limited to DigitalOcean integrations etc.

![](../../.gitbook/assets/selection_211.png)

If docker environment image you require is not there, it is just one click away to getting your specific environment requested. From experiences the Buddy team responsiveness is good, given the stuff I asked about are pretty technical at times.

![](../../.gitbook/assets/image%20%286%29.png)

Or if you are more like a chat person that is also a click away, with a chat icon on the far right bottom.

![](../../.gitbook/assets/selection_214.png)

## How we use Buddy

This section is about how I configure Buddy to suits my own needs. It might not be best practises others agree to but the good side is I find Buddy pretty flexible enough to cater for different situations. I'm saying this as a software developer without much DevOps experience at all, apart from doing some Docker related stuff \(creating image, running them, push and retrieving them from Docker Hub etc.\) and some limited Kubernetes stuff \(deployment of pods, writting simple kubernetes yaml file for demos and development work etc\)

### Grouping of Pipelines

I find it nice to be able to group and categories related pipelines. 

![](../../.gitbook/assets/image%20%281%29.png)

| Category | Description |
| :--- | :--- |
| Daily | Contains build pipelines for Front End \(FE\), Back End \(BE\) and End to End Tests \(E2E\) that runs on a daily basis |
| Manual | Contains build pipelines for FE, BE and E2E that are to be trigger manually |
| Docker | Contains build pipelines to build docker images for FE, BE etc. and publish them to Docker Hub. |
| Kubernetes | Contains build pipelines to run kubernetes commands to apply yaml file changes on node in clusters  |

Notice how the Branch is a drop down list, so this makes it easier in future if out focus branch is say. v2.0.0 instead. All we need to do is to swap the default branch for the pipeline in settings

All these work based on the assumption that code in branch v1.0.0 for example will have scripts to publish to docker hub under v1.0.0 tags, perform kubernetes pod updates based on docker image with v1.0.0 tag etc.

![](../../.gitbook/assets/image%20%2811%29.png)

Or to select a different branch from the drop down if it is a "one time" only build.

![](../../.gitbook/assets/image%20%289%29.png)

### Configuring Pipelines

With the huge number of actions available for selection, it basically minimise the effort of us needing to presetup a particular docker image to run things we need. 

#### Running Cypress Tests

For example in order to run cypress, we'd just pick the cypress action, startup the front end and back end program and use `npx cypress` command to run cypess test.

![](../../.gitbook/assets/image%20%282%29.png)

#### What if we need a different Cypress or Node version

If the default cypress docker image doesn't suits your need, you can switch it the in environment tab.

![](../../.gitbook/assets/image%20%2812%29.png)

#### What about services like database or some NoSQL services?

You can add thoses services should you need it through the "Services" tab, and to be frank the services offerings are pretty comprehensive. Most importantly it saves you the trouble of messing around with installing them on to the image yourself.

![](../../.gitbook/assets/image%20%283%29.png)

### Running Node app

Similarly if you are running a node app, and would like to install, build and test the build, you would need only to choose the "Node" action and commands like npm, node would be available to you. Switch to a different docker image with various tags through the environment tab.

![](../../.gitbook/assets/image.png)

### Building and Publishing Docker Images

Building, publishing docker images, would be just a matter of selecting the right actions and stitching them together in order.

![](../../.gitbook/assets/image%20%284%29.png)

### Kubernetes Provisioning

If you are with a well know kubernetes provider like Google Cloud, AWS or Azure, configuration would be pretty straight forward. For GKE, you'd be selecting your Google account, project, zone and cluster.

![](../../.gitbook/assets/image%20%2810%29.png)

If your provider is not listed, a bit more configuration would be needed but in general still manageable. You would need a cluster server url, which you might be able to figure this out through the `~/.kube/config` file etc.

![](../../.gitbook/assets/image%20%287%29.png)

## Summary

Buddy seems to ticking all the right boxes as far as we are concern, typically in easing on the DevOps skill sets required, leaving one the luxury of conerntrating of the application under development itself, which is nice to have for smaller start ups where resource are often limited and streached. 



