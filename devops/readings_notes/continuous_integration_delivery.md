## The old way
+ Parallel branches are developed
+ Branches are merged in to master when complete
+ Over time branches will drift from master
  + re-merging can cause huge headaches

## Continuous integration
+ ensure everyones' changes are integrated
+ bug catching
+ reduce merge conflicts

+ automated testing with a dedicated server
+ server determines if new code can be integrated
+ server outputs test results

## Continuous delivery and deployment
### Continuous Delivery
+ develop to release at any time

### Continuous Deployment
+ deploy new features immediately


### CI
+ push to github when you make changes
+ changes go from github to CI server and check them against main dev branch
+ github uses webhooks to send messages to external systems about activity in your projects
+ Developers can subscribe their CI server to updates from code changes on github.
  + CI server
    + parses message from github
    + grabs current copy from github
    + builds branch
    + runs test
    + sends message back to github with status of this commit
    + this tells you what changes will work with the current codebase

### CD
  + CI server deploy branches as part of your processes
  + Any time master receives a new commit CI provider grabs a copy of the current code and deploys this to production

Use deployment API + webhooks to notify 3rd party systems to retrieve code from github and deploy requested code to the production environment desired.
