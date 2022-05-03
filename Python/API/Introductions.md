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
