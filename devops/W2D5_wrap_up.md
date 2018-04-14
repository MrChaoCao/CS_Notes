# Wrapup

## General Dev ops
try to make your application as small as possible, use as few machines as we can
  we pay by the machine

ELB
  traffic from inbound port
  out to different servers
  terminates SSL certificates

Database
  one of the first problems

Q: if a webapp is running slowly what can we do?
  db queries
  often times we start at the database
  look at the slow queries, log slow queries
    see if we can improve the performance with indexing

  what if web servers are running slowly
  network performance

  caching, try to decrease distance between content and end user

## AWS
many many different services
some of them have overlap in functionality

EC2 is the heart of it, everything else is based off of that
  instances
  load balancers
  distributed servers
  CDN
  DNS manager
  cloudwatch (management)

## CI/CD


## RDS & Databases
Disk store as linked list or an array
Relational databases are like large binary search trees on a disk
each index is a binary search tree

INDEXES !

if you were releasing an API to render on a screen
it will look mostly like CSS

aside:
build your control flow before you write your code
junior engineers often think code first, but that's trivial
you should already know all the algorithms, the code is not a big deal

## Puppet, Chef & Opsworks
fleet management is the central authority that controls all the servers that are out there
puppet and chef are the two major fleet management softwares
  puppet uses an eventually consistent dependency graph
    ex: destination is lat/long, you eventually get there
    you know the final state, then you need to get there
  chef has more scripting, processes top to bottom
  ansible
    builds modules for you
    builds a script for each server and it sends it off to the fleet
opsworks wraps either puppet or chef


aside:
unicorn runs your app
nginx server in front of your app


## Chef Recipes
cookbooks have a set structure , recipes, attributes, templates



## DNS & SSL


## Caching - CDNs
get the content as close to the client as possible
they're as close to the end user as possible

all about validation and data
  if you have it too long you'll be serving old content
  if you make it too short it doesn't do anything

manual invalidation is a tool that acts as a failsafe
  when new stuff is made we just clear our cache

## Monitoring






learn one database in each category
Relational
Document
Key value
Graph
