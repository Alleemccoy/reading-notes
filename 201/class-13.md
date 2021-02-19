# **Class 13 Reading Notes**

### No. 7 The Past, Present & Future Of Local Storage For Web Applications [Article](http://diveinto.html5doctor.com/storage.html)

- Diving In
  * Cookies have three potentially dealbreaking downsides:
    1. Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
    2. Cookies are included with every HTTP request, thereby sending data unencrypted over the internet - unless your entire web application is served over SSL
    3. Cookies are limited to about 4 KB of data — enough to slow down your application - *see above* - but not enough to be terribly useful
  * What we **really** want is:
    * A lot of storage space
    * On the client
    * That persists beyond a page refresh
    * Is not transmitted to the server

- A Brief History Of Local Storage Hacks Before HTML5
- Introducing HTML5 Storage
  * *HTML Storage* is specification names Web Storage
  * Certain browser vendors also refer to it as **Local Storage** or **DOM Storage**
  * HTML5 is a way for web pages to store named key/value pairs locally, within the client web browser
  * HTML5 Storage Supports:
    * IE 8.0+
    * FIREFOX 3.5+
    * SAFARI 4.0+
    * CHROME 4.0+
    * OPERA 10.5+
    * IPHONE 2.0+
    * ANDROID 2.0+
  * Check For HTML5 Storage
- Using HTML5 Storage
  * HTML5 Storage is based on named key/value pairs
- Tracking Changes To The HTML5 Storage Area
  * To keep track programmatically of when the storage area changes, you can trap the storage event
- Limitations In Current Browsers
- HTML5 Storage In Action
  * With HTML5 Storage, we can save the progress locally, within the browser itself
- Beyond Named Key-Value Pairs: Competing Visions
  * Most of the action resides in the string you pass to the executeSql method
  * This string can be any supported SQL statement, including SELECT, UPDATE, INSERT, and DELETE statements - it’s just like backend database programming, except you’re doing it from JavaScript
  * WEB SQL Database Supports
    * IE
    * FIREFOX
    * SAFARI 4.0+
    * CHROME 4.0+
    * OPERA 10.5+
    * IPHONE 3.0+
    * ANDROID 2.0+
- Further Reading Links