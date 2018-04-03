# Processes - OS
+ Allow multiple processes to run "simultaneously"
  * a processes is the execution of one particular thing
  * context switching
  * takes entire state of program and swaps it out for whatever program of interest is
    * if you minimize and switch programs, that's the OS at work
    * puts whole program into ram to use later
+ Restrict processes based on user permissions
+ OS allows you to share
  * time (cpu)
  * space (memory)
+ Allow these processes to share resources:
RAM (memory) with “colliding”
Hard drive access, according to user permissions
Network usage - Ports
Other devices

### Aside
* What does your CPU do?
  1. fetches command from memory
  2. decodes it, knows what circuits to turn on
  3. executes
  4. stores results in memory

# Processes - a single process
we are not directly accessing memory in ruby
system calls are made from ruby to be able to manipulate the actual RAM through the OS
m-alloc = memory allocation

system call: implementation of interface
glibc => core of C , just an interface
different OSs implement this interface differently

# Processes - as a tree
ps aux - figure out what this is
pstree will allow you see your tree visually


# Processes - Interaction
starts a process with some extra information
once a process is running the environment is set and cannot change


piping, stdin in, stderr and stdout out

STDIN - typing from user, usually
STDOUT
STDOUT

how do you stop a running process?
ctrl + c
OS is sending signals

OSI stack - common internet stack (presentation and session not really used anymore) <==== check this out
each layer is a different problem in networking


# Networking - Sockets
IP - internet protocol
physical layer -> physical representations of 1s and 0s in the medium
MAC address, physical address
Network layer - hierarchical network address

ports are the thing which decides [something] what assign a process to
TCP - stateful, needs to see if it makes it there, used for everything but streaming, keeps data reliable
UDP - will continue to transmit regardless if it's received, really good for streaming

IP address comes from the router

# Networking - IP routing
somewhat hierarchical
gives proximal location, kinda
your IP address (within the same ISP) will be pretty close to your neighbors
Internet engineering task force (IETF) doles out addresses to the ISPs
ISPs are given a range of IPs that they can dole out
ISPs split them up and give them to consumers
ISPs will have localized routers to serve customers in the same geographic area
Your modem connects to the local hub
Your router assigns your machine an IP address

special IPs
192.168.-
10.-
excluded from the range, reserved for private networks only
At the router level you get 1 IP, like a front door
Behind that each device gets a chunk of the internet
NAT (network address traversal)
NAT hole-punching

# Networking - DNS
DNS maps a human readable name to an IP address
You ask for an IP address, they're assigned. Same with domain names.
13 servers on the planet that you get your domain name registered on.
multiple names mapped to the same ip address
but only one ip address per name
  technically this can be split up by geographic location

# Networking - URLs
normal style:
https://www.appacademy.io/immersive/courses

protocol - language we're talking in (http, https, etc. -this also gives the port number)
subdomains
DNS name
path

this style:
postgres://myuser:mypass@db.coolsite.com:5432/mydb
fullest url you can see - defines what content your server is delivering to the client

format of the communication is called a protocol
  email is different from a webpage

# Scaling a web application
What do you look for for a bottleneck in a large application
  usually the database is the bottleneck

for any given piece of datum there should be a single source of truth => database is the hardest part to scale

# Application servers
rails s will lose scalabilty very very fast, it is single threaded
Rack Middleware lends scalability to rails s
Rack standard way for a web request to come into a rack server and then sends it to a rack application


Layer before your application that is resonsible for simple system level routing
so you can use https instead of http
manipulate web traffic only pass the stuff we care about to our server
web server can do it way better than your application
web server handles what goes to what port, don't try to do this at home, use apache or nginx

Next step:
Move DB to its own server.
RDS - one amazon server for databases
heroku/postgres does it for you

# Database
to speed up databases
  add indexes
  clean up your queries
  add master/slave interfacing
  split the data - shard
  asyncronous database management

# Load Balancer
Network layer - takes 1 packet in and send it to one of the different servers
For huge applications you use a hardware load balancer, anything that shaves time is incredibly valuable
  less time -> less cycles -> less hardware required

Load balancer is the point of security, if you have encryption at each layer it's inefficient
Load balancer faces the public so its the end of security, if you get past it you're in the money


separate the web server and the web application.
Allows you to optimize them independently
Server can direct traffic to the appropriate web application (think microservices)

# CDN - content delivery network
images don't change much, tell browser to keep a copy of the image locally
many steps along the way can cache the static content so the user doesn't need to wait for it
cache control headers


## check video here, losing grasp
jobrunners
these guys run seldom used processes in the background and move them around

queue

cache
keep something local so you don't need to go make another api call

# summary
