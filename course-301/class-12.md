# *Course 301, Entry 12: CRUD*

## REST Status Codes

In your own words, describe what each group of status code represents:

+ 100’s = Pre-texual in nature. Gives the client information of what to expect.
+ 200’s = The request was successfully received.
+ 300’s = Location change of repository.
+ 400’s = Error codes. The input parameters did not match any server or its requirements, includes timeouts.
+ 500’s = Server errors. This is usually an indicator of a server-side issue.

### What is a status code 202?

Code 202 is a validation message for asynchronous processes. It simply means that validation requirements were met.

### What is a status code 308?

Permanent redirect. It points the client to another URL to access the resource. Similarly, 307 does the same but is temporary in nature.

### What code would you use if an update didn’t return data to a client?

In this case, assuming no errors, it would be code 204. An example of use would be saving a document.

### What code would you use if a resource used to exist but no longer does?

This would be code 410. This means the resource existed but was deleted or moved.

### What is the ‘Forbidden’ status code?

The forbidden status code is 403. This code means no authorizations are needed, but access is still denied.

## Build A REST API With Node.js, Express, & MongoDB

### Why do we need to pull our MongoDB database string out of our server and put it into our .env?

This is due to security issues. Otherwise a DOS attack is possible, or many other forms of attacks.

### What is middleware?

Middleware is the code that acts upon the resources between the database and the front-end server.

### What does app.use(express.json()) do?

This line of code allows for middleware to be used and applies JSON formatting.

### What does the /:id mean in a route?

The ":id" is a parameter. This can be access via `req.params.id`. 

### What is the difference between PUT and PATCH?

PUT is a complete update while PATCH is a partial update.

### How do you make a default value in a schema?

To set a default, use `default:` to set the parameter. Then, the default value can be entered thereafter.

### What does a 500 error status code mean?

This means the database had some kind of error. This is serparate from the user and client.

### What is the difference between a status 200 and a status 201?

Code 201 is used for CREATE. In the header response will be the location URL of the newly created resource.


## Things I want to know more about

Why would anyone feel the need to customize the error codes and extend them? Are 206 codes used for packet downloads?
