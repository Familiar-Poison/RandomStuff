#### What exactly happens when a browser tries to access a website?
1. DNS Lookup
* User Input: The user types a URL into the browser's address bar
* DNS Lookup: The browser checks it cache for the IP address associated with the domain name. If not found, it queries the DNS server to resolve the domain name into an IP address.
2. TCP Connection
* TCP/IP Connection: THe browser establishes a TCP connection to the server using the resolved IP address. This involves a three-way handshake (SYN, SYN-ACK, ACK).

3. HTTPS Handshake
4. HTTP Request
5. Server Response
6. Resource Rendering
7. Additional Request
8. User Interaction 