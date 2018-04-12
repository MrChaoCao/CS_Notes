# CDN Integration
+ So far:
  + CI/CD
  + pushes production ready assets to s3
  + our assets are being served directly from the server
  + web server is serving the files from the HD not the application server
    + nginx - receives request, sends it to unicorn
    + unicorn - is your app

  + worst case, go through the web server hit unicorn, load bytes from file send them back through nginx
    but nginx could have just done that itself
    the closer we can get the content to the user the better, fewer machines required!

+ Today we will setup Cloudfront with S3


## Caching
+ a way to avoid unnecessary work
+ application cache vs HTTP cache

+ main caching services: Memcached and Redis


aside: there's only 2 hard things in computer science: "naming variables, caching validations, and off by 1 errors"


### cache control / expiry - cache control
cache control header determines how to cache data
no-store is the default, don't cache it anywhere, don't store it on the client

CDN can DRAMATICALLY improve performance of your site.


## Cloudfront
it's built off of open source tech called squid
