## REST Article

1. Who is Roy Fielding?
-He helped write the first web servers that sent documents across the internet and explained why the web works the way it does and he authored the protocol (HTTP) that is used to get pages from servers to your browser. 

2. Why don’t the techniques that we use in this class work well when we need to be able to talk to all of the machines in the world?
-Because they werent designed to be used in that way. When Fielding and his colleagues startedbuilding the web, being able to talk to any machine inthe world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didnt have those requirements and only needed to talk to a small group of computers. 

-We generally send human readable data to accross the web. Its not set up as a one to manu relationshop. 

3. What is the HTTP protocol that Fielding and his friends created?
-The HTTP protocal is all about applying "verbs to nouns". For example, when you go to a web page, the browser does an HTTP GET on the URl you typed in and back comes the webpage. Webpages usually have images which are separate resources and the webpages just specifies the URLs to the images and the browser does more GETs using the HTTP protocol on then until all the resources are obtained and the webpage is displayed. The key concept here is that different things -- text, images, video, mp3, can be treated the same. You can GEt all those things the same way. 

**Essentially is just a general purpose protocol applying verbs to nouns**

4. What does a GET do?
-When a machine GETs a resource it will ask the machine-readable one. When a browser GETs a resource for a human it will ask for the human-readable representation of that data. 

To retrieve information, a system would use HTTP GET.

5. What does a POST do?
-If one system needs to add something to another system it would use an HTTP verb of POST.

6. What does PUT do?
-If a system needs to replace something in another system it uses HTTP PUT. 

7. What does PATCH do?
-If a system wants to do a partial update, it needs to use PATCH. 

Geocoding API
Did you get your API key?
-

Weather Bit API
Did you get your API key?

Yelp API docs
Did you get your API key?

The Movie DB API Docs
Did you get your API key?