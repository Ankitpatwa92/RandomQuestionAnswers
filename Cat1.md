#### Q1 What is OPTIONS in HTTP methods?

When your browser makes a request to a host it might receive a script asking it to make HTTP requests to another host. 
For security reasons browsers restrict HTTP requests not originating from original host within scripts. 
Using OPTIONS http request the script can ask what headers/content-type it can make to the non-original host. 
Once the non-original host responds with the OPTIONS response the browser will allow it to make further HTTP 
requests to this secondary host with the allowed headers/content-type.

Request has body	No
Successful response has body	Yes
Safe	Yes
Idempotent	Yes

curl -X OPTIONS http://example.org -i

HTTP/1.1 200 OK
Allow: OPTIONS, GET, HEAD, POST
Cache-Control: max-age=604800
Date: Thu, 13 Oct 2016 11:45:00 GMT
Expires: Thu, 20 Oct 2016 11:45:00 GMT
Server: EOS (lax004/2813)
x-ec-custom-error: 1
Content-Length: 0

