**Tags**: [[Systems Thinking]]
- Throughput vs Latency - Throughput is how many requests the system can handle at once, and latency is the amount of time it takes to process one request. Focusing on one can lead to sacrificing the other
- IP header - Contains source and destination IP address, and the protocol for communication
- Application layer - Data specific to the application protocol is stored here (ex: HTTP request data)
- TCP and UDP - Transmission Control Protocol is safe and ensures packet delivery, because there is a three way handshake, but this can be slow. The header also has sequence number to ensure the correct order of packets. User Datagram Protocol does not ensure safety or packet order, but is pretty fast
- Domain Name System is a phonebook which converts the Domain name to IP address
- Public IP addresses are unique across the internet and private IP address are unique in the local network
- Ports are used to identify processes or services within one device.

Application Protocols
- Hyper Text Transfer Protocol - the server doesn't store context information, the request contains all of it, all the time
- Websockets provide a two way communication where a system requires constant data sharing - like stock market feeds
- SMTP - standard mail transmission protocol
- FTP - File transfer protocol