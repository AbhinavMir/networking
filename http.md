## Persistent vs Non-Persistent HTTP

Persistent HTTP is a type of communication protocol that allows a single TCP connection to be used to send and receive multiple HTTP requests and responses between a web server and a client. A persistent connection is established once, and can remain open for multiple exchanges between the server and the client.

Non-Persistent HTTP is a type of communication protocol that requires a new TCP connection to be established for each HTTP request and response that is sent between a web server and a client. This means that a new connection must be opened for each transaction, making it slower and less efficient than persistent HTTP.