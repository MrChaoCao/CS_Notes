# Most common HTTP Status Codes

## 100 level Informational
* 100 continue
  + Client should continue request by sending the rest of the request (if there is more)
  + Server must send final response after the full request.

## 200 level Success
* 200 OK
  + request was successful
  + information returned depends on the method of the request
* 201 Created
  + request has been fulfilled and a new resource was created
* 204 No Content
  + Server has successfully processed the request but is not returning any content

## 300 level Redirect
* 304 Not Modified
  + Resource has not been modified since last requested

## 400 level Client Error
* 400 Bad Request
  + Server could not understand client request. Usually due to bad syntax from client
* 403 Forbidden
  + Server understands the request but refuses to fill it. Authorization will not help
* 404 Not Found
  + Server has found nothing matching the requested content
* 409 Conflict
  * Request could not be processed because of a conflict in the request. Ex: edit conflict.
## 500 level Server Error
* 500 Internal Server Error
  + The server has encountered an unexpected condition which has prevented it from filling the request. Generic server error.

  [Resources](http://www.restapitutorial.com/httpstatuscodes.html)
