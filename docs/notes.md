### REST API

##### When using a REST API with a GET request, the process typically follows these steps:

##### 1. Client Initiates Request

* The client, often a web browser or an application (Postman), initiates an HTTP GET request to a specific URL. This URL identifies the resource the client wants to retrieve.

##### 2. URL Construction
* The URL may include query parameters to specify filters or criteria for the request. For example: `http://example.com/api/resource?param1=value1&param2=value2`

##### 3. DNS Resolution
* The client's system resolves the domain name in the URL to an IP address using DNS (Domain Name System).

##### 4. Establishing a Connection:
* The client establishes a TCP connection with the server at the resolved IP address. If the URL uses HTTPS, an SSL/TLS handshake occurs to establish a secure connection.

##### 5. Sending the Request:
* The client sends the HTTP GET request to the server. This request includes headers such as `Host`, `User-Agent`, `Accept` and possibly authentication tokens or other custom headers.

##### 6. Server Processing:
* The server receives the request and processes it. This involves:
    * Parsing the URL and query parameters.
    * Authenticating the client (if required).
    * Validating the request.
    * Fetching the requested resources from a database or other storage.

##### 7. Generating a Response:
* The server generates an HTTP response. This response includes:
    * Status line (e.g, `HTTP/1.1 200 OK`)
    * Response headers (e.g, `Content-Type`, `Content-Length`)
    * Response body (the actual resource data in JSON, XML, HTML or other formats)

##### 8. Sending the Response:
* The server sends the HTTP response back to the client over the established connection

##### 9. Client Receives the Response:
* The client receives the HTTP response. The client's application processe the response, which may involve:
    * Parsing the response headers and body.
    * Handling different status codes (e.g, 200 OK, 404 Not Found, 500 Internal Server Error)
    * Displaying data to the user or further processing it.

##### 10. Closing the Connection:
* Depending on the connection settings and protocols used, the connection may be closed after the response is received, or it may be kept alive for further requests (HTTP Keep-Alive)

---

##### [Back to Main](./index.md) 