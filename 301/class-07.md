# Reading: Class 07

### [What Google Learned From Its Quest to Build the Perfect Team](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)
*New research reveals surprising truths about why some work groups thrive and others falter*

### [How I Explained REST to My Brother](https://gist.github.com/brookr/5977550)
*A conversation explaining REST*

- Roy Fielding helped write the first web servers, that sent documents across the internet and then he did a ton of research explaining why the web works the way it does
- Roy's name is on the specification for the protocol that is used to get pages from servers to your browser
- http tells the browser what protocol to use
- That stuff you type in there is one of the most important breakthroughs in the history of computing
- It is capable of describing the location of something anywhere in the world from anywhere in the world
- It's the foundation of the web, think of it like GPS coordinates for knowledge and information
- The whole world wide web is built on an architectural style called “REST”
- REST provides a definition of a “resource”, which is what those things point to
- A web page is a “representation” of a resource, resources are just concepts like URLs
- URLs tell the browser that there's a concept somewhere, a browser can then go ask for a specific representation of the concept - specifically, the browser asks for the web page representation of the concept
- There's this concept that people are calling “Web Services” or "APIs", it means a lot of different things to a lot of different people but the basic concept is that machines could use the web just like people do
- Computers can use those same protocols to send messages back and forth to each other
- Machines don't have a universal noun - that's why they suck, every programming language, database, or other kind of system has a different way of talking about nouns - that's why the URL is so important, it let's all of these systems tell each other about each other's nouns
- There's a powerful concept in programming and CS theory called “polymorphism”
  * That's a geeky way of saying that different nouns can have the same verb applied to them
  * Take a look at your coffee table. What are the nouns? Laptop, bottle, book, paper. Now, what are some things you can do to all of these things?
  * You can "get" them, right? You can pick them up. You can knock them on the floor. You can burn them. You can apply those same exact verbs to any of the objects sitting there
  * What if instead of me being able to say to you, "get the bottle," and "get the magazine," and "get the book"; what if instead we needed to come up with different verbs for each of the nouns? I couldn't use the word "get" universally, but instead had to think up a new word for each verb/noun combination. "shmet the bottle", "mandle the magazine", "zorp the book"
  * Our brains are somehow smart enough to know that the same verbs, like GET, can be applied to many different nouns, some verbs are more specific than others and apply only to a small set of nouns - for instance, I can't drive a cup and I can't drink a car but some verbs are almost universal like GET, PUT, and DELETE
- HTTP—this protocol Fielding and his friends created—is all about applying verbs to nouns, for instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page
- Web pages usually have images, right? Those are separate resources
- The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed but the important thing here is that very different kinds of nouns can be treated the same
- Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL
- GET is specially important when you're using a web browser because browsers pretty much just GET stuff
- They don't do a lot of other types of interaction with resources, this is a problem because it has led many people to assume that HTTP is just for GETing but HTTP is actually a general purpose protocol for applying verbs to nouns
- Think about when you're browsing around amazon.com looking for things to buy for Christmas, imagine each of the products as being nouns - Now, if they were available in a representation that a machine could understand, you could do a lot of neat things
- Machines cant understand a normal webpage because web pages are designed to be understood by people, a machine doesn't care about layout and styling, machines basically just need the data
- Ideally, every URL would have a human readable and a machine readable representation. When a machine GETs the resource, it will ask for the machine readable one
- When a browser GETs a resource for a human, it will ask for the human readable one
- How about we take a real example:
  * Imagine you are a teacher - at school you probably have a big computer system, or three or four computer systems more likely, that would let you manage students: what classes they're in, what grades they're getting, emergency contacts, information about the books you teach out of, etc. If the systems are web-based, then there's probably a URL for each of the nouns involved here: student, teacher, class, book, room, etc. Right now, getting the URL through the browser gives you a web page. If there were a machine readable representation for each URL, then it would be trivial to latch new tools onto the system because all of that information would be consumable in a standard way. It would also make it quite a bit easier for each of the systems to talk to each other. Or, you could build a state or country-wide system that was able to talk to each of the individual school systems to collect testing scores. The possibilities are endless!
- Each of the systems would retrieve information from each other using a simple HTTP GET, if one system needs to add something to another system, it would use an HTTP POST, if a system wants to replace something in another system, it uses an HTTP PUT, or, to do a partial update, it'll hopefully use PATCH - The only thing left to figure out is what the data models should look like
- Software developers work on deciding how to best model the data, this is what engineers do in the web development world, thanks almost entirely to the popularity of RESTful web frameworks like Ruby on Rails
- Just a few years ago, the large majority of developers were busy writing layers of complex specifications for how to access data in a different way that isn't nearly as useful or eloquent
- Nouns weren't universal and verbs weren't polymorphic, they basically ignored throwing out decades of real field usage and proven technique and kept starting over with something that looks a lot like other systems that have failed in the past - They used HTTP but only because it let them talk to our network and security people less, it was like trading simplicity for flashy tools and wizards
- Now, we just tell Rails what we want our data to look like, and it takes care of all of the communication pieces for us. It's a huge boost for productivity!


#### API Keys
*I requested the API keys prior to lecture*