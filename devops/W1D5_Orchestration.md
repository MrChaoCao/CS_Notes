# Overview
  + Fleet management
  + Puppet vs Chef
  + Ansible vs SaltStack
  + Opsworks

# Deploying to a large fleet - series
ssh to machine install jenkins, install programs and start processes
Imagine we have many machines instead of just one
there were a lot of errors with just one, imagine we have many more now
  this is way more time consuming even if it's just linear difficulty
  this is the way it used to be

## issues and concerns
+ if we're dealing with multiple machines some can be different, any given machine might have a different state, dealing with different machines can be very time consuming
+ even with a perfect script, we can have errors from external factors
+ we can mitigate risks

What machine tells the database to update? (we're gonna ignore that question)

 
## Puppet
In order for this machine to be considered healthy, we need git project, conflict theory,
coe you right does not execute sequentially
run based o the sate of the

Eventually consistent, eventually all servers will be consistent.


# Ansible
doesn't use middleman server itself
