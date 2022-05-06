## What are APIs?  

If you look up the term API, you'll probably find a number of definitions—some of which are rather difficult to understand. But the key underlying idea is in the name—Application Programming Interface. An API is an interface. It's something that has been created to help two different systems interact with one another.  

  
  A key idea to remember is that API functionality is defined independently of the actual implementation of the provider. Essentially, you don't need to understand the entirety of the application implementation in order to interact with it through the API. This has multiple benefits:

  
  It doesn't expose the implementation to those who shouldn't have access to it
  
  The API provides a standard way of accessing the application
  
  It makes it much easier to understand how to access the application's data
  
  Some frequently used APIs include:

  
  Google Maps API allows users to access a large amount of data related to maps, routes, and places around the world.
  
  Stripe API allows users to accept payments, send payouts, and manage businesses online.
  
  Facebook API allows developers to integrate directly with the Facebook platform.
  
  Instagram Basic Display API allows users of your app to get basic profile information, photos, and videos in their Instagram accounts.
  
  Spotify API allows users to access a large amount of data related to music artists, albums, and tracks, directly from the Spotify Data Catalogue.
  
  If you check out any of the above links, you'll find some extensive documentation for the relevant API. Creating good API documentation is an important consideration all to itself, and we'll be discussing it in some detail later in this course.
    

  
  ## Client-Server Communication
  
  When you got to a bank, the bank teller acts as an intermediary or interface between you and the bank vault. And this is the same type of relationship we see in   
  client-server communication: The user or client makes a request to the API server, which parses the requests, queries the database, formats a response and then   
  sends it back.

  
  Here is the process listed out:

  
  Client sends a request to the API server
  
  The API server parses that request
  
  Assuming the request is formatted correctly, the server queries the database for the information or performs the action in the request
  
  The server formats the response and sends it back to the client
  
  The client renders the response according to its implementation  
  ## Internet Protocol (IP)   
is the protocol for sending data from one computer to another across the internet. Each computer must have a unique IP address that identifies it from all other   
computers connected to the internet. It's likely that you've heard the term IP address before, even if you didn't know exactly what it meant.

  
  There are many other internet protocols including:

  
  Transmission Control Protocol (TCP) which is used for data transmission
  
  Hypertext Transmission Protocol (HTTP) which is used for transmitting text and hyperlinks
  
  File Transfer Protocol (FTP) which is used to transfer files between server and client
  
  Our API will transmit data to our client via HTTP so we will primarily focus on that protocol.
  
     
   ## RESTful API.   
   REST stands for Representational State Transfer, which is an architectural style introduced by Roy Fielding in 2000.

  
  Here's a short summary of the REST principles:

  
  Uniform Interface: Every rest architecture must have a standardized way of accessing and processing data resources. This includes unique resource identifiers   
  (i.e., unique URLs) and self-descriptive messages in the server response that describe how to process the representation (for instance JSON vs XML) of the data   
  resource.

  
  Stateless: Every client request is self-contained in that the server doesn't need to store any application data in order to respond to subsequent requests

  
  Client-Server: There must be both a client and server in the architecture

  
  Cacheable & Layered System: Caching and layering increases networking efficiency

  
  Why RESTful are stateless?
  
  It might appear easier to design a server that isn't stateless. There is a reason why RESTful web servers are not allowed to remember anything about the previous   
  requests that the user has sent. In short, stateless servers make your applications scalable.
