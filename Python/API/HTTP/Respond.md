After the request has been received by the server and processed, the server returns an HTTP response message to the client. The response informs the client of the outcome of the requested operation.

## Elements:
* Status Code & Status Message
* HTTP Version
* Headers: similar to the request headers, provides information about the response and resource representation. Some common headers include:
** Date
** Content-Type: the media type of the body of the request
* Body: optional data containing the requested resource
  
Status Codes:
As an API developer, it's important to send the correct status code. As a developer using an API, the status codes—particularly the error codes—are important for understanding what caused an error and how to proceed.

## Codes fall into five categories:
* 1xx Informational
* 2xx Success
* 3xx Redirection
* 4xx Client Error
* 5xx Server Error
## Common Codes:
* 200: OK
* 201: Created
* 304: Not Modified
* 400: Bad Request
* 401: Unauthorized
* 404: Not Found
* 405: Method Not Allowed
* 500: Internal Server Error
