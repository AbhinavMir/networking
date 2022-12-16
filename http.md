## Persistent vs Non-Persistent HTTP

Persistent HTTP is a type of communication protocol that allows a single TCP connection to be used to send and receive multiple HTTP requests and responses between a web server and a client. A persistent connection is established once, and can remain open for multiple exchanges between the server and the client.

Non-Persistent HTTP is a type of communication protocol that requires a new TCP connection to be established for each HTTP request and response that is sent between a web server and a client. This means that a new connection must be opened for each transaction, making it slower and less efficient than persistent HTTP.

## Sample questions

Consider a web client requesting a base html page of size O = 5,000 bytes from a web server. This base html page contains one object of the same size of O bytes. This one embedded object (img01.jpg) reside on the same web server. The minimum round-trip (propagation) delay RTT = 100 msec, and the channel rate R = 1Mbps. Assume the client uses persistent HTTP (HTTP 1.1) to retrieve the embedded object. 

(a) How long is the response time—the time it takes to receive the base page and its one embedded object from the web server after the user requests the initial base html page? In answering this question, assume error-free transmission. Be sure to consider TCP connection establishment (1 RTT), and the data transmission delay for the base file and the embedded object. Ignore header / control bits, and assume that the sending rate is not limited by flow control, i.e., the server can send data at the channel rate R. To support your answer, include a timing diagram, and show all steps of your calculations along with associated expressions in terms of O, R, and RTT.