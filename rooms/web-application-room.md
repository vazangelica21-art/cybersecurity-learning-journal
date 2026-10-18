# TryHackMe Lab Notes — Web Application Basics

## Room
Web Application Basics

## Topics Learned
- How web applications work
- HTTP and HTTPS
- URLs and their components
- HTTP request methods
- HTTP response status codes
- HTTP headers
- Client-server communication

## Practical Work

### 1. Understanding Web Applications
A web application is software that users access through a web browser. It works through communication between a client (browser) and a server.

**Basic flow:**
1. The user enters a URL or clicks a link.
2. The browser sends an HTTP request to the server.
3. The server processes the request.
4. The server returns an HTTP response.
5. The browser displays the result.

### 2. HTTP and HTTPS
- **HTTP (Hypertext Transfer Protocol):** A protocol used for communication between web clients and servers.
- **HTTPS:** HTTP secured using TLS encryption. It helps protect data while it travels between the client and server.

HTTPS does not automatically mean that a website is trustworthy; it secures the connection to the website.

### 3. Understanding URLs
A URL (Uniform Resource Locator) identifies a resource on the web.

Example:

`https://example.com:443/products?id=10#details`

- `https` — scheme or protocol
- `example.com` — hostname
- `443` — port
- `/products` — path
- `id=10` — query parameter
- `#details` — fragment

### 4. HTTP Request Methods
HTTP methods indicate the action a client wants to perform.

| Method | Purpose |
|---|---|
| GET | Retrieve information |
| POST | Submit data or request an action |
| PUT | Create or replace a resource, depending on the API |
| PATCH | Partially update a resource |
| DELETE | Request deletion of a resource |
| HEAD | Retrieve response headers without the response body |

**Security takeaway:** Improperly configured methods and insufficient authorization can expose web applications to security risks.

### 5. HTTP Response Status Codes
Status codes tell the client the result of its request.

| Code | Meaning |
|---|---|
| 200 OK | Request succeeded |
| 301 Moved Permanently | Resource has a permanent redirect |
| 302 Found | Temporary redirect |
| 400 Bad Request | Server cannot process the request due to a client error |
| 401 Unauthorized | Authentication is required or has failed |
| 403 Forbidden | Server refuses access |
| 404 Not Found | Resource was not found |
| 500 Internal Server Error | Server encountered an unexpected error |

**Security takeaway:** Error responses can sometimes reveal information about server configuration or application behaviour.

### 6. HTTP Headers
Headers carry additional information in HTTP requests and responses.

Examples:
- `Host` — identifies the target host.
- `User-Agent` — identifies information about the client software.
- `Content-Type` — describes the media type of the message body.
- `Authorization` — carries authentication credentials or tokens.
- `Cookie` — sends cookies associated with the request.
- `Set-Cookie` — instructs the browser to store a cookie.
- `Content-Security-Policy` — helps control which resources a browser may load.
- `Strict-Transport-Security` — tells browsers to use HTTPS for a specified period.

**Security takeaway:** Secure header configuration can help reduce risks such as cross-site scripting and clickjacking. Authentication cookies should use appropriate attributes such as `Secure`, `HttpOnly`, and `SameSite`.

## Key Takeaways
- HTTP enables communication between browsers and web servers.
- HTTPS protects data in transit using TLS.
- URLs contain different components that help locate web resources.
- HTTP methods define the requested action.
- Status codes indicate the result of a request.
- Headers provide important information about requests, responses, and security.
- Understanding HTTP is a foundation for web application penetration testing.

## Interview Practice

**Q1. What is the difference between HTTP and HTTPS?**

HTTP is a protocol for communication between clients and servers. HTTPS protects HTTP communication using TLS encryption.

**Q2. What is the difference between 401 and 403?**

401 indicates that valid authentication is missing or unsuccessful. 403 indicates that the server refuses access, typically because the client is not permitted to perform the action.

**Q3. What is the difference between GET and POST?**

GET is generally used to retrieve data, whereas POST is commonly used to submit data or trigger an operation.

**Q4. What is an HTTP header?**

An HTTP header is a field that carries additional information in a request or response, such as content type, authentication information, or security policy.

**Q5. Why is HTTP knowledge important in cybersecurity?**

It helps security professionals understand web traffic, inspect requests and responses, identify configuration issues, and test web applications for vulnerabilities.

## Status
Completed — revise the concepts and practical exercises before interviews.

## Further Practice
- Inspect HTTP requests and responses using browser Developer Tools.
- Explore requests in Burp Suite Community Edition or OWASP ZAP.
- Practise only on authorised labs and applications.

## Learning Reflection
This room introduced me to the basic communication mechanisms used by web applications. Understanding requests, responses, methods, status codes, and headers provides a foundation for learning web security testing.
