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
- Facebook and Accept JSON