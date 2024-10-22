# Internet
Globally connects independent networks and computing devices
(Effectively redundant collection of wires connecting all computers (some wires are wireless: wifi, satellite, cell))

## Making connections
IP (internet protocol) address is how devices talk to each other.
Domain names found in lookup in Domain Name System (DNS)

`dig` console utility finds ip address for any domain name

once you have IP address you can connect by hoping caross netowrk until destination is dynamically established. 
* dynamic discovery makes internet resilient when devices fail or disappear 

## Traceroute
`traceroute` console utility is used to determine hops in connection
* from requesting device through router (and non ID connections) to ISP (more non IDd) to destination

## Network internals - sending data by TCP/IP Model
  TCP - transmission control protocol
  

* ### [TCP/IP](https://en.wikipedia.org/wiki/Internet_protocol_suite) layers
Layers top down
| Layer       | Example         | Purpose                               |
| ----------- | --------------- | ------------------------------------- |
| Application | HTTPS           | User Functionality like web browsing       |
| Transport   | TCP             | Moving connection information via packets |
| Internet    | IP              | Establishing and keeping connections              |
| Link        | Fiber, hardware | Physical connections                  |

other applications : web (HTTP), mail (SMTP), files (FTP), remote shell (SSH), and chat (IRC).
