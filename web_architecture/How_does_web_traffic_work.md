# What happens when you go to google.com?

Browser checks the cache for a DNS record to find the IP address for google.com

+ Every URL has a unique IP address
+ IP address belongs to the computer which hosts the server for the website
+ You can reach the same website by visiting the IP address directly
+ DNS is a directory of URLs and IP addresses

To find the DNS record of a website your browser checks 4 caches:
1. browser cache
2. OS cache
3. router cache
4. ISP cache

# DNS Queries
If requested URL is not in the cache ISP's DNS server initiates a DNS query to find IP address for the server hosting google.com

DNS query searches multiple DNS servers until the correct IP address is found.

There are multiple domain levels for websites.
1. "."
2. edu, org, gov, com, au, etc.
3. openoffice.org, expedia.gov, microsoft.com, etc.
4. www.expedia.gov, download.microsoft.com, sales.microsoft.org

Example: maps.google.com
1. Root name server.
  * Redirects to the .com domain name
2. Top level domain
  * .com name server redirects to google.com name server
3. Second-level domain
  * google.com name server will find matching IP for maps.google.com in its DNS records and return it back to your browser
4. Third-level domain

These requests are sent using data packets which contian content of the request and the IP address it's destined for

# Browser initiates a TCP connection with the server
Once you have the correct IP address your browser builds a connection with the server. Internet protocols are used to build these connections. The most common protocol is TCP.

TCP connection is established using a TCP/IP three-way handshake. The client and server exchange SYN (synchronize) and ACK (acknowledge) messages.

1. Client sends SYN packet to server asking if it's open
2. Server sends SYN/ACK packet if it has open ports that can accept/initiate new connections
3. Client receive SYN/ACK packet and responds with an ACK packet

# Browser sends HTTP request to web server
Once TCP connection is established:
* browser sends HTTP request, GET, POST, PUT, DELETE, etc.
* request also contains additional information:
  * Browser identification
  * Accept header (types of requests it will accept)
  * Connection headers, request to keep connection alive
  * Information stored in the cookies for this domain

# Server handles request and sends back rseponse
Server contains a webserver (ie Apache, IIS)
Webserver gives the request to a request handler
Request handler reads the request, headers, cookies
  * determines what is being requested
  * updates the information on the server if required
  * assembles a response in appropriate format (JSON, SML, HTML)

# Server sends HTTP response
Server response contains
* the requested web webpage
* status code
* compression type (content encoding)
* how to cache the page (cache control)
* cookies to set
* privacy information

* status code comes in 5 types.
  1. 1xx informational message
  2. 2xx success
  3. 3xx redirect client to another URL
  4. 4xx client side error
  5. 5xx server level error

# Browser displays content (usually HTML)
* browser displays HTML content in phases
  1. HTML skeleton
  2. checks HTML tags and sends get requests for additional content (images, stylesheets, etc)
  3. Cache these static files in browser so you don't need to fetch them again next time
