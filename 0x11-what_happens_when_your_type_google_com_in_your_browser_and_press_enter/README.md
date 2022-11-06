A typical user only requests a browser, receives a response, and is unaware of what transpired. The user needs to enter some text in the browser and press Enter to get the results. However, you can typically do many things by typing google.com into a browser. We will examine all of the processes before you see the outcome.

When you type Google.com, your browser immediately runs an IP address query for the domain (DNS).
It then creates a (TCP/IP) connection with the web server's host.
The server is then given an HTTP request (HTTPS/SSL).
The server responds by responding (HTTPS/SSL) in response to this.
Finally, the requested data is shown by your browser.
The procedure parts are as follows:

 Operating system,
User Agent (such as a browser),

Server (host website server).

Internet Service Provider,

Parts of URL

The sample of the URL is given below.



https -: this is the scheme or the protocol.
www -: It is the subdomain.
google -: domain nam
com -: top level.

DNS Request

DNS is a system that converts domain names into computer-readable IP addresses. Because your browser needs the domain's IP address to connect to the server, a DNS request is required.

The Process Involved

The user enters Google.com.
The ISPS DNS resolver receives the request.
The DNS root name server receives the request from the resolver.
The root server provides the IP for a TLD DNS.
The domain name server receives the request after being forwarded by the resolver.
The resolver receives the IP address for "google.com" from the domain name server.
The resolver then gives the browser the IP address for "google.com."
TCP/IP

With the help of the TCP/IP protocol, data (packets) can be sent from client to server to enable end-to-end conversations and delivery. The client-server architecture is used, in which a server offers a service to a networked user. Because previous network paths are constantly being freed, TCP/IP is said to be stateless, allowing network paths to be recycled or reused (i.e., released). Every request a client makes is taken to be distinct from all prior requests; each request is a new request.

Browser:

The browser must find the server-with-IP-found before it can establish a connection. Routing infrastructure employs data from Layer 3 of the OSI model (Network Layer) to route the browser's packets through the ISP to the internet to locate the server with the discovered IP address.

After finding the server, it must establish a TCP connection with the server-with-IP-found. The three-way handshake is then performed:

 The User Agent (browser used by users) transmits a synchronization packet to the server with IP found across the internet.
The user agent learns that the server with the IP discovered can accept new connections when it receives a synchronize-acknowledgment packet from the server.
After the User Agent answers by transmitting an acknowledgment packet, the connection is established. 
A TLS handshake is carried out to ensure the security of the communication if the requested URL is "HTTPS."

HTTPS/SSL

The client (browser) and server develop cryptography (public and private key) algorithms after mutually checking and acknowledging one another. They choose session keys as well.

The process

The necessary TLS version is offered.
The cipher suites (algorithms used for encrypted connections) are also agreed upon, and the client uses the servers' SSL certificates to verify their authenticity.
A client delivers the premaster secret and retrieves the public key from the server's SSL certificate (a random encrypted string).
The server decrypts the premaster secret. Both the client and the server offer session keys.
The server and client use session keys to encrypt "finished" messages during communication.
A firm handshake and secure communication.
The browser sends an HTTP request to the server when the connections have been made to request a webpage. SEARCH FOR "http://www.google.com"

Load balancing

A load balancer, essentially another server, distributes the traffic to the numerous web servers on your domain. It directs traffic to the available or accessible web server in high demand. Free in the sense that it takes little to no effort.

Webserver

On the domain, servers are web servers and a database. Web servers are used to provide the requested material. A load balancer routes traffic to one or more web servers with access to the same database as all other web servers.

Firewall

Web servers utilize firewalls called "ufw" to protect the system from threats. To use a firewall, you must confirm that your web server is outfitted with one. By quickly searching for "How to configure up on [Ubuntu, Windows, etc.]," you can find information on how to set up a firewall.

Application server

This is used exclusively to run applications. It is a server that creates a setting that enables the use of applications.

Database

Comprises the web pages and files for the website. Examples of file extensions include.html,.css,.php, and more. These web pages are stored in the server's database.

Web servers have request handlers that respond to client queries, hence the name "request handler." A request handler is a program written in a particular programming language, such as PHP. It performs a duty of creating a response to a query.

In conclusion

The server delivers the requested content to the browser as part of the http response. The browser will then show the website you requested, in this case, a page with a bar, a search icon, and the word "google."

The browser makes its display decisions based on the Content-Type header from the http response. Everything happens in less than a second.
