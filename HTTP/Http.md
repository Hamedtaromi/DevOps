 # HTTP Concepts
--------------

**HTTP --> easy transfer HTML files**


# HTML



**Request Header**

**Request Body**

**Response Header**

**Response Body**
-----------------


#Request Header: 
**(VERB=Request Method)**
------------------------

*GET ---> Request the specified resource

*POST --> send specific data to the server for processing

PUT  ---> send specific data to the server

DELETE -> delete the specified resource

HEAD  --> request the title of specified resource

OPTION -> retrieve the HTTP requests that the server supports

PATCH --> modify the specified resource


TTFB ---> Time To First Bytes


Response Header
-----------------
Status Code : 

1.1XX ---> Informational Message
 
2.2XX ---> Success

3.3XX ---> Redirect
   
4.4XX ---> Client error

5.5XX ---> Server error



1.	100 ---> Continue 
2.	101 ---> Switch Protocol (HTTP ----> WS , HTTPS ---> WSS)
3.	200 ---> OK
4.	201 ---> Created
5.	301 ---> Move Permanently
6.	302 ---> Move Temporary
7.	307 ---> Temporary ????
8.	400 ---> Bad Request
9.	401 ---> Unauthorized
10.	403 ---> Forbidden
11.	404 ---> not found
12.	405 ---> Method not allowed
13.	407 ---> Proxy Authentication Required
14.	408 ---> request timeout
15.	500 ---> internal server error
16.	501 ---> not implemented
17.	502 ---> bad gateway
18.	503 ---> service unavailable
19.	504 ---> gateway timeout
