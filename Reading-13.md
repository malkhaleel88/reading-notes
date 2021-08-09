# **CRUD**
 
## **Status Codes Based On REST Methods**

 
 ### **In your own words, describe what each group of status code represents:**

 * 100’s = These are informational status codes.

 * 200’s = These are the success codes.
 
 * 300’s = These are redirection codes.
 
 * 400’s = These are the client error codes.
 
 * 500’s = These are the server error codes.

 ### **What is a status code 202?**
 
 *202 Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.*
 
 ### **What is a status code 308?**

 *308 Permanent Redirect - This is the right code if the resource will now be available at a new URL and the client should directly access it via the new URL in the future. The current endpoint can’t control the clients’ behavior after the request and a subsequent redirect if the resource URL changes again have to be issued from the new URL.*

 ### **What code would you use if an update didn’t return data to a client?**
 
 *204 No Content*
 
 ### **What code would you use if a resource used to exist but no longer does?**

 *404 Not Found *

 ### **What is the ‘Forbidden’ status code?**
 
 *403 Forbidden - The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.*

## **Build A REST API With Node.js, Express, & MongoDB - Quick**


 ### **Why do we need to pull our MongoDB database string out of our server and put it into our .env?**
 
 *For easier scripting, you can specify configuration settings by using environment variables.*
 
 ### **What is middleware?**

 *For easier scripting, you can specify configuration settings by using environment variables.*

 ### **What does app.use(express.json()) do?**
 
 *Bind application-level middleware to an instance of the app object by using the app.use() function.*

 ### **What does the /:id mean in a route?**

 *However, you may want to create only one route path where the id parameter is optional.*


 ### **What is the difference between PUT and PATCH?**

 *PUT is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely.*

 *PATCH applies a partial update to the resource, This means that you are only required to send the data that you want to update, and it won’t affect or change anything else.*


 ### **How do you make a default value in a schema?**

 *Schema type default value as blank and make the field optional.*

 ### **What does a 500 error status code mean?**

 ***Internal Server Error** server error response code indicates that the server encountered an unexpected condition that prevented it from fulfilling the request.*

 ### **What is the difference between a status 200 and a status 201?**
 
 *The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed.*

 *A 201 status code indicates that a request was successful and as a result, a resource has been created (for example a new page).*
 

 
 ## **Things I want to know more about**



[HOME](https://malkhaleel88.github.io/reading-notes)

