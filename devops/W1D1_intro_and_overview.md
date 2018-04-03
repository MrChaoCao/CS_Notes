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
Internet engineering task force doles out addresses to the ISPs
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
