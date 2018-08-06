# What is REST
+ Stands for Representational State Transfer.
+ Design principles to make network communication more flexible/scalable
+ Generic set of principles not specific to the web


# REST Requirements
## Client-server
+ Networks are made up of clients and servers
+ Server are machines that have content
+ Clients are the machines that want to interact with content
+ Components can switch between being the client or the server
+ An example of a different paradigm is broadcast / receiver

## Stateless
+ Clients and servers do not track each others' state
+ Each interaction is standalone

## Uniform Interface
Clients and servers must share a common language. If the principles of uniform interface are obeyed. The entire system gains robustness and

### Identification of Resources
+ Resources must have a unique identifier
+ Identifiers must remain constant even if the resource itself changes
+ URI is the resource identifier

### Manipulation of resources through representations
+ Client manipulates resources through sending representations to the server
+ Server controls resources and is responsible for making changes
+ Client makes requests to the Server and Server decides how to respond

### Self descriptive messages
+ Messages sent between parties contain all information required by the recipient.
+ Servers do not need to send clients a message containing the response data and a second message explaining how to use that data.

### Hypermedia
+ Data sent from the server guides the actions of the client.
+ For example HTML is returned to clients from servers which informs the client what to display.

## Caching
+ Clients can save previous responses from the server to avoid repeating work
+ This is a derivative benefit from servers sending self descriptive messages
## Layered system
+ There can be more components than just servers and clients
+ Layers can be added, but each component can only see other components in the adjacent layers
+ Proxies are a layer that relays requests to servers or other proxies
+ Gateways translate requests between protocols, forward the request, then translate the response. Clients can treat gateways as if they are the server

## Code on demand
+ Optional constraint
+ Servers can send executable code to clients
+ Examples are HTML script tags

[Read More](https://codewords.recurse.com/issues/five/what-restful-actually-means)
