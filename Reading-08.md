# **APIs**

## **API Design Best Practices**

 *REST is an architectural style for building distributed systems based on hypermedia. REST is independent of any underlying protocol and is not necessarily tied to HTTP.*

 ### **What does REST stand for?**

  *Representational State Transfer.*

 ### **REST APIs are designed around a** *resources, which are any kind of object, data, or service that can be accessed by the client.*.

 ### **What is an identifer of a resource? Give an example.**

 *A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:*
```
 HTTP:
 https://adventure-works.com/orders/1
 ```

 ### **What are the most common HTTP verbs?**

 *The most common operations are GET, POST, PUT, PATCH, and DELETE.*

 ### **What should the URIs be based on?**

 *Should be based on nouns (the resource) and not verbs (the operations on the resource).*

 ### **Give an example of a good URI.**
```
 HTTP:
 https://adventure-works.com/orders
 ```

 ### **What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**

 *That expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires*

 ### **What status code does a successful GET request return?**

 *A successful GET method typically returns HTTP status code 200 (OK)*

 ### **What status code does an unsuccessful GET request return?**

 *If the resource cannot be found, the method should return 404 (Not Found).*

 ### **What status code does a successful POST request return?**

 *If the method does some processing but does not create a new resource, the method can return HTTP status code 200 and include the result of the operation in the response body. Alternatively, if there is no result to return, the method can return HTTP status code 204 (No Content) with no response body.*

 ### **What status code does a successful DELETE request return?**

 *If the delete operation is successful, the web server should respond with HTTP status code 204 (No Content), indicating that the process has been successfully handled, but that the response body contains no further information.*
 
 
 
 ## **Things I want to know more about**



[HOME](https://malkhaleel88.github.io/reading-notes)
