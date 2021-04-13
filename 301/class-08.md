# Reading: Class 08

### [SuperAgent Documentation](https://visionmedia.github.io/superagent/)
*SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js*

- Test Documentation
- Request Basics
  * A request can be initiated by invoking the appropriate method on the **request** object, then calling `.then()` or `.end()` or `await` to send the request
  * HTTP method may also be passed as a string
  * Old-style callbacks are also supported, but not recommended - *instead of* `.then()` you can call `.end()`
  * Absolute URLs can be used, in web browsers absolute URLs work only if the server implements **CORS**
  * The **Node** client supports making requests to *Unix Domain Sockets*
  * **DELETE, HEAD, PATCH, POST,** and **PUT** requests can also be used, simply change the method name
  * **DELETE** can be also called as `.del()` for compatibility with old IE where `delete` is a reserved word
  * The HTTP method defaults to **GET**, so if you wish, the following is valid
- Setting Header Fields
  * Setting header fields is simple, invoke `.set()` with a field name and value
  * You may also pass an object to set several fields in a single call
- GET Requests
  * The `.query()` method accepts objects, which when used with the **GET** method will form a query-string, the following will produce the path `/search?query=Manny&range=1..5&order=desc`
  * Or as a single object
  * The `.query()` method accepts strings as well
  * Or joined
- HEAD Requests
  * You can also use the `.query()` method for HEAD requests, the following will produce the path `/users?email=joe@smith.com`
- POST / PUT Requests
  * A typical JSON **POST** request might look a little like the following, where we set the Content-Type header field appropriately, and "write" some data, in this case just a JSON string
  * Since JSON is undoubtedly the most common, it's the default
  * Or using multiple `.send()` calls
  * By default sending strings will set the `Content-Type` to `application/x-www-form-urlencoded`, multiple calls will be concatenated with `&`, here resulting in `name=tj&pet=tobi`
  * SuperAgent formats are extensible, however by default "json" and "form" are supported, to send the data as `application/x-www-form-urlencoded` simply invoke `.type()` with "form", where the default is "json"
  * Sending a `FormData` object is also supported
- Setting the Content-Type
  * The obvious solution is to use the `.set()` method
  * As a short-hand the `.type()` method is also available, accepting the canonicalized MIME type name complete with type/subtype, or simply the extension name such as "xml", "json", "png", etc
- Serializing Request Body
  * SuperAgent will automatically serialize JSON and forms, you can setup automatic serialization for other types as well
  * If you want to send the payload in a custom format, you can replace the built-in serialization with the `.serialize()` method on a per-request basis
- Retrying Requests
  * When given the `.retry()` method, SuperAgent will automatically retry requests, if they fail in a way that is transient or could be due to a flaky Internet connection
  * This method has two optional arguments: number of retries (default 1) and a callback, it calls `callback(err, res)` before each retry - the callback may return `true/false` to control whether the request should be retried but the maximum number of retries is always applied
  * Use `.retry()` only with requests that are idempotent: i.e. multiple requests reaching the server won't cause undesirable side effects like duplicate purchases
- Setting Accept
  * In a similar fashion to the `.type(`) method it is also possible to set the `Accept` header via the short hand method `.accept()`, which references `request.types` as well allowing you to specify either the full canonicalized MIME type name as `type/subtype`, or the extension suffix form as "xml", "json", "png", etc. for convenience
  * Facebook and accept JSON
- Query Strings
  * `req.query(obj)` is a method which may be used to build up a query-string. For example populating `?format=json&dest=/login` on a **POST**
  * By default the query string is not assembled in any particular order, an asciibetically-sorted query string can be enabled with `req.sortQuery()`.
  * You may also provide a custom sorting comparison function with `req.sortQuery(myComparisonFn)` - the comparison function should take 2 arguments and return a negative/zero/positive integer
- TLS Options
  * In Node.js SuperAgent supports methods to configure HTTPS requests - *visit link for these requests*
- Parsing Response Bodies
  * SuperAgent will parse known response-body data for you, currently supporting `application/x-www-form-urlencoded`, `application/json`, and `multipart/form-data`, you can setup automatic parsing for other response-body data as well
  * You can set a custom parser that takes precedence over built-in parsers with the `.buffer(true).parse(fn)` method, if response buffering is not enabled `(.buffer(false))` then the response event will be emitted without waiting for the body parser to finish, so response.body won't be available
  * JSON / Urlencoded
  * Binary
- Response Properties
  * Many helpful flags and properties are set on the `Response` object, ranging from the response text, parsed response body, header fields, status flags and more
  * Response text
  * Response body
  * Response header fields
  * Response Content-Type
  * Response status
- Aborting Requests
  * To abort requests simply invoke the `req.abort()` method
- Timeouts
  * Sometimes networks and servers get "stuck" and never respond after accepting a request, set timeouts to avoid requests waiting forever
    * `req.timeout({deadline:ms})` or `req.timeout(ms)` where ms is a number of milliseconds > 0 sets a deadline for the entire request (including all uploads, redirects, server processing time) to complete, if the response isn't fully downloaded within that time, the request will be aborted
    * `req.timeout({response:ms})` sets maximum time to wait for the first byte to arrive from the server, but it does not limit how long the entire download can take
    * Response timeout should be at least few seconds longer than just the time it takes the server to respond, because it also includes time to make DNS lookup, TCP/IP and TLS connections, and time to upload request data
  * You should use both `deadline` and `response` timeouts, this way you can use a short response timeout to detect unresponsive networks quickly, and a long deadline to give time for downloads on slow, but reliable, networks
  * Timeout errors have a `.timeout` property
- Authentication
  * In both Node and browsers auth available via the `.auth()` method
  * In the *Node* client Basic auth can be in the URL as "user:pass"
  * By default only `Basic` auth is used. In browser you can add `{type:'auto'}` to enable all methods built-in in the browser
  * The `auth` method also supports a `type` of `bearer`, to specify token-based authentication
- Following Redirects
  * By default up to 5 redirects will be followed, however you may specify this with the `res.redirects(n)` method
  * Redirects exceeding the limit are treated as errors, use `.ok(res => res.status < 400)` to read them as successful responses
- Agents for Global State
  * Saving cookies
  * Default options for multiple requests
- Piping Data
  * The Node client allows you to pipe data to and from the request, please note that `.pipe()` is used instead of `.end()/.then()` methods
- Multipart Requests
  * SuperAgent is also great for building multipart requests for which it provides methods `.attach()` and `.field()`
  * When you use `.field()` or `.attach()` you can't use `.send()` and you must not set Content-Type - **the correct type will be set for you**
  * Attaching files
  * Field values
- Compression
  * The node client supports compressed responses, best of all, you don't have to do anything! It just works
- Buffering Responses
  * To force buffering of response bodies as `res.text` you may invoke `req.buffer()`, to undo the default of buffering for text responses such as "text/plain", "text/html" etc you may invoke `req.buffer(false)`
- CORS
  * For security reasons, browsers will block cross-origin requests unless the server opts-in using CORS headers, browsers will also make extra OPTIONS requests to check what HTTP headers and methods are allowed by the server
  * The `.withCredentials()` method enables the ability to send cookies from the origin, however only when `Access-Control-Allow-Origin` is **not** a wildcard ("*"), and `Access-Control-Allow-Credentials` is "true"
- Error Handling
  * Your callback function will always be passed two arguments: error and response, if no error occurred, the first argument will be null
  * An "error" event is also emitted, with you can listen for
- Progress Tracking
  * SuperAgent fires `progress` events on upload and download of large files
- Testing on Localhost
  * Forcing specific connection IP address
  * Ignoring broken/insecure HTTPS on localhost
- Promise and Generator Support
  * SuperAgent's request is a "thenable" object that's compatible with JavaScript promises and the `async/await` syntax
  * If you're using promises, **do not** call `.end()` or `.pipe()` - any use of `.then()` or `await` disables all other ways of using the request
- Browser and Node Versions
  * SuperAgent has two implementations: one for web browsers **using XHR** and one for Node.JS using core http module, by default Browserify and WebPack will pick the browser version
  * Using browser version in electron


### Bookmarked the following examples/tutorials
[RegExr](https://regexr.com/)
[Regex Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
[Regex 101](https://regex101.com/)