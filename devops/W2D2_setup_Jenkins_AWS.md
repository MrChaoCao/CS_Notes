# AWS
most startups are working on AWS
google's cloud is on AWS hardware
AWS is most common provider

AWS versions of the services mentioned in the overview

aside:
EC2: elastic cloud computing
RDS: Relationship database service

all of the other services are built on top of ec2

Amazon has worldwide data servers
it will not automatically check what region you deploy to, you must choose.
We will be using us-west-2 Oregon

volumes are like external hard drives that you can plug into any instance that you want

volumes can only be plugged into one instance at a time

# EC2 Load balancers

Health check, every 30 seconds it will check machine for health (200 level responses)
listeners
  if port 80 (http), send it to another machine, also on port 80
  if port 443 (https), handle SSL then everything behind it is on port 80

# EC2 Security Groups

security group rules are very similar to firewalls
we will often need to change the defaults they give us
frequent source of headache. Often you think it's a connection issue, but it's actually a sec group rule


On a Jenkins server we don't run on port 80 (port 8080)
By default 8080 isn't available to the outside world

Inbound requests tab
select specific rules for the types of requests we expect

aside: 0.0.0.0/0 - means anybody


# RDS - relational database service


# Cloudfront
Distributed CDN
