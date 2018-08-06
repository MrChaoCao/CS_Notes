# What is REST
+ Stands for Representational State Transfer.
+ Design principles to make network communication more flexible/scalable
+ Generic set of principles not specific to the web

## Where did REST come  from
Roy Fielding coined the term in 2000 when describing the set of traits that made the web more successful than competing web protocols. REST is not a protocol as it does not have rules for implementation.
Fielding Constraints:

## REST Requirements
### Client-server
+ Networks are made up of clients and servers
+ Server are machines that have content
+ Clients are the machines that want to interact with content
+ Components can switch between being the client or the server
+ An example of a different paradigm is broadcast / receiver

### Stateless
+ Clients and servers do not track each others' state
+ Each interaction is standalone

### Uniform Interface
Clients and servers must share a common language. If the principles of uniform interface are obeyed individual clients and servers can be swapped out without breaking the system
  1. Identification of Resources
    + Resources must have stable unique identifiers
      + Identifiers remain constant across interactions
      + Identifiers remain constant even if the resource itself changes
    + The web uses URI(URL) as the resource identifier
  2. Manipulation of resources through representations
    + Client manipulates resources through sending representations to the server
      + The client sends a vision of the final product. Not explicit instructions on how to make it.
    + Server controls resources and is responsible for making changes
    + Client makes requests to the Server and Server decides how to respond
  3. Self descriptive messages
    + Messages sent should contain all information required by the recipient to understand the message.
      + Servers do not need to send clients a message containing the response data and a second message explaining how to use that data.
      + In practice the self-descriptive messages are http responses containing a message in html. The client (your browser) knows how to read an html page.
      + If not for this constraint servers might send multiple responses and if the instructions get lost, the main message is unreadable.
  4. Hypermedia
    + Data sent from the server guides the actions of the client.
    + For example HTML is returned to clients from servers which informs the client what to display.

  The uniform interface constraint allows for clients to intelligentl adapt to changes. Servers can change how things work without breaking all clients that come into contact with them.

### Caching
+ Clients can save previous responses from the server to avoid repeating work
+ Because each message is self-descriptive, cached responses will represent the entire resource that was being served.

### Layered system
+ There can be more components than just servers and clients
+ Layers can be added, but each component can only see other components in the adjacent layers.
  + Thanks to the client - server relationship, complex layers will be treated the same as any other client or server in any given interaction  
+ Proxies are a layer that relays requests to servers or other proxies
+ Gateways translate requests between protocols, forward the request, then translate the response. Clients can treat gateways as if they are the server

### Code on demand
+ Optional constraint
+ Servers can send executable code to clients. The code is stored serverside and run clientside.
+ Examples are HTML script tags

# Wrapup
The three main fielding constraints:
1. Client-Server interactions. Different machines are in 1 to 1 client server relationships where machine only wants information and the other machine only delivers it.
2. Stateless. Clients and servers do not track each others states.
3. Uniform interface. All messages between clients and servers are in a uniform predictable language.

[Read More](https://codewords.recurse.com/issues/five/what-restful-actually-means)
