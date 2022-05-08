Hypertext Transfer Protocol (HTTP) is a protocol that provides a standardized way for computers to communicate with each other. It has been the foundation for data communication over the internet since 1990 and is integral to understanding how client-server communication functions.

## Features:
* Connectionless:  
 When a request is sent, the client opens the connection; once a response is received, the client closes the connection. The client and server only maintain a connection during the response and request. Future responses are made on a new connection.
* Stateless: There is no dependency between successive requests.
* Not Sessionless: Utilizing headers and cookies, sessions can be created to allow each HTTP request to share the same context.
* Media Independent: Any type of data can be sent over HTTP as long as both the client and server know how to handle the data format. In our case, we'll use JSON.
## Elements:
  
* Universal Resource Identifiers (URIs): An example URI is http://www.example.com/tasks/term=homework. It has certain components:
* Scheme: specifies the protocol used to access the resource, HTTP or HTTPS. In our example http.
* Host: specifies the host that holds the resources. In our example www.example.com.
* Path: specifies the specific resource being requested. In our example, /tasks.
* Query: an optional component, the query string provides information the resource can use for some purpose such as a search parameter. In our example, /term=homework.
  
  ## Side Note: URI vs URL
You may be unsure what the difference is between a URI (Universal Resource Identifier) and a URL (Universal Resource Locator). These terms tend to get confused a lot, and are even frequently used interchangeably—but there is a distinction.

The term URI can refer to any identifier for a resource—for example, it could be either the name of a resource or the address of a resource (since both the name and address are identifiers of that resource). In contrast, URL only refers to the location of a resource—in other words, it only ever refers to an address.

So, "URI" could refer to a name or an address, while "URL" only refers to an address. Thus, URLs are a specific type of URI that is used to locate a resource on the internet when a client makes a request to a server.
