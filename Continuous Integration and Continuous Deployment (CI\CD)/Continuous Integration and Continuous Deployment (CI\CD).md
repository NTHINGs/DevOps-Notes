# Continuous Integration and Continuous Deployment (CI\CD)

As we talked about in the last topic about software industry and the role of a DevOps on it. Software today requires agility. This means that people want fixes and features (or both) fast. CI/CD practices allows developers to deliver this changes in matter of minutes.

In short, it lays out some practices to follow in order for the code developers write to safely, and quickly get features to users.

## CI

Continuous Integration (CI) is a development practice where developers integrate code into a shared repository frequently, preferably several times a day. Each integration can then be verified by an automated build and automated tests. This provide the benefit of detecting defects before going into production and breaking things. Also uploading and integrating code frequently allows to have more small and manageable changes, couple of lines written in a day are more understandable that a thousand written in a week or more.

In the ideal world where the organization follows CI as it best and developers are making commits in a daily basis (assuming they use Git, if you are not using Git for this wtf is wrong with you.) the merge conflicts are less problematic and developers are always working with the latest code of the project. Which means they are not stepping each other steps.

![merge-conflict](https://pics.me.me/merge-conflict-git-push-force-origin-masteremegenerator-net-29177974.png)

## CD

Continuous Deployment is a strategy for software releases where in any code commit that passes the automated testing phase is automatically released into the production environment, making changes that are visible to the software’s users. Basically if the pipeline goes green, the change will be deployed to production in matter of minutes.

Some organizations doesn't fully trust this approach and take another one called "Continuous Delivery" that basically is use CI and trigger the deployment with a click. This way we have a fully automated deployment but the trigger for this is controlled, it doesn't go automatically when a change is ready.

Continuous Deployment vs. Continuous Delivery? It depends on the organization needs. The ideal is Continuous Deployment because if Continuous Integration is correctly implemented and tests are well designed what's the difference on delivering this changes as soon the test passes or on a particular day?.

![cd-vs-cd](https://resources.codeship.com/hs-fs/hubfs/continuous-delivery-vs-continuous-deployment-b371cf5be55b1c52635058af7b70188cd2b608bfb92ca5487a3e41694e9ccf6b.jpg?width=598&height=359&name=continuous-delivery-vs-continuous-deployment-b371cf5be55b1c52635058af7b70188cd2b608bfb92ca5487a3e41694e9ccf6b.jpg)

I've worked in organizations that are afraid of fully going for Continuous Deployment and are ok with Continuous Delivery. Usually they schedule a particular day to deploy a bunch of changes, usually the ones scheduled for the sprint. Friday every 2 weeks for example (Don't deploy to production on Friday btw).

![Don't deploy to production on Friday](https://miro.medium.com/max/600/0*TzEwS_4n0YzHy1jQ.jpg)

The downside of this way of doing deployments, is that if a change introduces bugs or worst; the whole system went down. Is hard to accurately know the change and who did it. Because is easy to know if 1 change broke everything instead of 20.

## CI/CD Tools

There's a lot of tools in the market to achieve a mature practice in CI/CD. Jenkins lovers may hate it but I personally love and use Gitlab CI/CD. Why? is simple, all in one tool, no need to install stuff in your infrastructure. You can with Gitlab EE, but is not actually needed for most of dev teams.

Gitlab CI/CD allows the implementation of the three approaches we talked about before:
    * Continuous Integration (CI)
    * Continuous Delivery (CD)
    * Continuous Deployment (CD)

Read more about it [here](https://docs.gitlab.com/ee/ci/)

See the demo in [here](https://gitlab.com/NTHINGs/pipeline-demo)
