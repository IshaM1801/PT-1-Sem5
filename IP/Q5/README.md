Describe the structure of the HTTP request and response message with format and example
HTTP (Hypertext Transfer Protocol) is the foundation of data communication for the World Wide Web. It works on a request–response model in which:

The client (for example, a web browser) sends an HTTP Request Message to the server.
The server processes this request and sends back an HTTP Response Message to the client.
Both request and response have a fixed structure so that they can be correctly interpreted by both sides.

1. Structure of HTTP Request Message
   The HTTP request message consists of four main parts:
   Request Line
   This is the first line of the HTTP request.
   It tells the server what action the client wants to perform.
   It contains three fields:
   • HTTP Method (GET, POST, PUT, DELETE, etc.) — defines the type of operation.
   • Request URI (Uniform Resource Identifier) — specifies the path of the resource on the server.
   • HTTP Version (HTTP/1.0, HTTP/1.1, HTTP/2.0) — specifies the version of the protocol being used.
   Format:
   Method Request-URI HTTP-Version
   Example:
   GET /index.html HTTP/1.1
   In the above example: “GET” is the method, “/index.html” is the URI, and “HTTP/1.1” is the protocol version.
   Header Fields
   These lines provide additional information about the request to the server.
   Each header line is written in the format: Name: Value
   Examples of common request headers:
   Host: www.example.com (specifies the domain)
   User-Agent: Mozilla/5.0 (tells the server the client’s software)
   Accept-Language: en-US (tells the server the preferred language)
   Headers help the server understand how to handle the request properly.
   Blank Line
   After the headers, there must be an empty line.
   This blank line marks the end of the headers and separates them from the message body.
   Without this blank line, the server cannot correctly distinguish between headers and body.
   Message Body
   This is optional and is mostly present in methods like POST or PUT.
   It contains the data sent to the server such as form data, JSON, or XML.
   Example: name=John&age=25
   In GET requests, this part is usually empty, but in POST requests it carries the main data.
   Complete Example of an HTTP Request:
   POST /submit-form HTTP/1.1
   Host: www.example.com
   User-Agent: Mozilla/5.0
   Content-Type: application/x-www-form-urlencoded
   Content-Length: 27
   (blank line)
   name=John&age=25

2. Structure of HTTP Response Message
   The HTTP response message also consists of four main parts:
   Status Line
   This is the first line of the HTTP response.
   It tells the client about the result of its request.
   It contains three fields:
   • HTTP Version — the version of HTTP used by the server.
   • Status Code — a numeric code that indicates the result (e.g., 200, 404, 500).
   • Reason Phrase — a short text describing the status code (e.g., OK, Not Found, Internal Server Error).
   Format:
   HTTP-Version Status-Code Reason-Phrase
   Example:
   HTTP/1.1 200 OK
   Header Fields
   These provide additional information about the response and the server.
   Examples:
   Date: Tue, 15 Aug 2025 10:30:00 GMT (when the response was generated)
   Server: Apache/2.4.1 (Unix) (software used by the server)
   Content-Type: text/html (format of the data being sent)
   Content-Length: 70 (size of the body in bytes)
   Blank Line
   A single empty line is placed after the headers.
   It separates the headers from the body of the response.
   Message Body
   This contains the actual content requested by the client.
   It could be HTML code, an image, JSON data, etc.

Example for HTML content:

<html> <body> <h1>Request Successful</h1> </body> </html>
Complete Example of an HTTP Response:
HTTP/1.1 200 OK
Date: Tue, 15 Aug 2025 10:30:00 GMT
Server: Apache/2.4.1 (Unix)
Content-Type: text/html
Content-Length: 70
(blank line)
<html> <body> <h1>Request Successful</h1> </body> </html>

Summary:
HTTP Request is sent from client to server and includes a request line, headers, a blank line, and an optional body.
HTTP Response is sent from server to client and includes a status line, headers, a blank line, and the body containing the resource.
Both messages follow a strict format so that web communication works reliably. Understanding their structure is important for web programming, API development, and debugging.
