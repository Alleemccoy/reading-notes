# Reading: Class 13

### [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)
**The HTTP specification defines many status codes we can use when responding to our clients. Some APIs only use the most basic codes and define their own error signaling mechanisms on top of it; others want to make full use of HTTPs collection of codes to tell their clients what’s going on.**
- HTTP Status CodesPermalink
  * A status code is a number higher than 100 and smaller than 600 that is part of a HTTP response. The first digit defines the class of the status. A status code comes with a reason phrase. The code is for programmatic recognition the phrase is for humans to understand what happened.
  * Every status code has to follow these two rules, even custom ones.
- Status Classes
  * 100 - 199 - These are informational status codes; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.
  * 200 - 299 - These are the success codes. They tell the client that its request was accepted. In case of asynchronous processing of a request (202), this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending.
  * 300 - 399 - These are redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore. This can have multiple reasons, be temporary or permanent, but the client has to issue a request to the new location.
  * 400 - 499 - These are the client error codes. They are all about invalid requests a client sent to a server. There are several causes to this, timeouts, wrong URI, missing authentication, etc. A client is sending incorrect input and should confirm the input parameters are correct before retrying the request.
  * 500 - 599 - These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server. These errors can be temporary or permanent. Usually it’s best for the client to retry the same request.
  * Custom Classes - Custom classes, that is, classes above 599 aren’t permitted but used by some services anyway. For API designers, they are relevant as bad examples. API client creators, however, have to deal with them.
- CRUD (Create, Read, Update, Delete)
  * The CRUD model defines the most basic API actions for persistent storage. Create, read, update, and delete. They make up the lions-share of API endpoints. Let’s see which status codes meet their requirements.
- CREATE
  * The create action is usually implemented via HTTPs POST method. In RESTful APIs, these endpoints are used to create new resources or access tokens.
  * Status Codes
- READ
  * The read action gets implemented via HTTPs `GET` method and used to fetch resource representations. Asynchronous responses aren’t much of a thing here, because the reason for asynchronous processing is often that the resource doesn’t exist yet and has to be created, so it’s a create action anyway.
  * Status Codes
- UPDATE
  * An update can be implemented with an HTTP `PUT` or `PATCH` method. The difference lies in the amount of data the client has to send to the backend.
  * `PUT` requires the client to send an entire representation of a resource to update it. (Replace the old one with the new one)
  * `PATCH` requires the client only send parts of the representation of the resource to update it. (Add, update or delete these parts in the old version)
  * Status Codes
- DELETE
  * The delete action can be implemented with the HTTP `DELETE` method.
  * Status Codes
- API Changes
  * If our API lives long enough, sooner or later it will change its structure. It’s best practice to avoid breaking changes and the redirection class of status codes can help with this because some clients follow their Location header automatically.
  * Status Codes
- Multiple Endpoints for One ResourcePermalink
  * If we opt-in to use nested or sub-resources in our API it can help to only deliver representations from root (non-nested) resources to keep the implementation DRY. Redirect status codes help with this.
  * Status Codes
- Errors
  * The next important part of an API is its errors. Many API frameworks use 500 and 404 status codes by default when something went wrong, but depending on the situation, often there are more descriptive ones.
- Wrong URL
  * When a client sends a URL, we don’t know. This can have multiple different reasons, so we have to check which of them applies here.
  * Status Codes
- No Permissions
  * Often clients can’t access every resource on the backend, so we need a way to tell them about it.
  * Status Codes

**Prompted Reading Questions**
1. In your own words, describe what each group of status code represents:
  * 100's = These is an informational codes, the request will fail  before they even start sending the body.
  * 200's = These are success codes, the request met all validation requirements.
  * 300's = These are redirection codes, the request sent is not available.
  * 400's = These are the client error codes, The client is sending incorrect information.
  * 500's = These are the server error codes, these are problems with overwhelmed or unreachable servers.
2. What is a status code 202? Accepted
3. What is a status code 308? Permanent Redirect
4. What code would you use if an update didn't return data to a client? I think 204
5. What code would you use if a resource used to exist but no longer does? I think 410
6. What is the *Forbidden* status code? 403


### [https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)
1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
2. What is middleware? 
3. What does `app.use(express.json())` do? This lets our server accept our JSON as a body.
4. What does the `/:id` mean in a route? This is a parameter , this gives us access to whatever they enter before the first `/`.
5. What is the difference between `PUT` and `PATCH`? **Patch** only want to update based on what the user passes, **Put** update all the information at once, not just the information that was passed.
6. How do you make a default value in a schema? Still unclear to me but I also found out information [here](https://mongoosejs.com/docs/defaults.html)
7. What does a **500** error status code mean? Internal Server Error server error response code.
8. What is the difference between a status **200** and a status **201**? 200 is the basic code to tell the client that everything went good, 201 should signal the backend-side resource creation and come along with a `Location` header that defines the most specific URL for that newly created resource.


## Things I want to know more about:
1. All the things