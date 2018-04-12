# DNS & SSL
## Security
security usually falls on architects or architects
even if it's just keys for ssh
Today is a theoretical primer on how it works
We're really only doing 2 commands, but the lecture is to figure out how they work


encryption in SSL - certificate signing
Route 53 and certificate manager


Today we give a readable URL to our website

DNS is hierarchical
once you buy a domain name, all you get is the right to change some settings

13 root servers throughout the world, [a-m]rootservers.net
buying a domain lets you put an entry on one of these 13 servers
Name server (NS) entry
  If you wanna find any subdomains that's somewhere else (like www.website.com)


Most common types
Alias - human readable name to an IP address
C-name - maps a name to anothr name


hierarchical nature of DNS
  manage domains
  edit DNS records

## Cryptography
cryptographic encoding
  not hashing!
    takes infinite possibilities and maps them to a fixed range
    hashing is one way, you cannot "unhash" something
    cryptographic functions are reversible
  takes (data, key) and produces encrypted message.
    using encrypted message + key can give you back the input data
  ideally it takes a message and gives cypher text that looks random

message -> cyphered message: e(x,k1)
cyphered message -> message: d(x,k2)

### types of encryption
#### Symmetric
  + key going forward is the same as the key to go backwards, k1 = k2
  + how do you get the key to the other party without exposing it
    + give everyone 2 keys, public and private
      + anyone can have the public key and send encrypted messages
      + only the owner of the private key can actually decrypt the message
      + SSL is all about public key / private key conversations
  + preferable to use symmetric key crypto
  + generating a key and performing encryption is very fast, key generation just takes making a random number and applying the technique
  + most encryption standards: do transposition and substitution a set number of times
  + the problem is though, that we cannot securely transmit this key, any means by which we would send it would be inherently insecure.

##### history
  substitution cyphers - key is the substitution
    letter replacement, same position
  transposition cyphers - key is the order
    same letters, position replacement


  polyalphabetic cypher, combat frequency analysis, use substitution and transposition cypher

#### Asymmetric
  + invented so we could share keys so we could then use symmetric encryption after we have our shared keys

  Trapdoor functions (not many of these exist)
  going forward is very easy
  going back is really hard
    examples:
      prime factorization -RSA -  (public key is a number, essentially the prime factorization of a large number)
      discrete logarithm problem - ECC

  RSA - (m^e)^d*mod(n) = m*mod(n)

  multiply 2 distinct prime numbers and then publish it
    + if anyone figures it out, then they can repeat the process


Server generates a public and private key
user connects to server
server sends user public key
user sends server random number encrypted with public key
now server has user's random number which can be used as a crypto key
Now that we have a common key, we can communicate with symmetric encryption

+ SSL is a public and private asymmetric keypair, we publish the public half
  + if someone is between server and client, then the entire system is compromised
  +
  + we will be giving both our halves to amazon
    + ELB takes a certificate
    + everything behind ELB is unencrypted


Create an SSL cert
  + RSA cert
  + give it to amazon
  + certificate manager will manage the cert

  + SSL is a "web of trust model", it's signed by a trusted entity
  + browser creators will hardcode the trusted certificate authorities in their browser
    + if everything checks out we're good to go
