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
  
### [TCP/IP](https://en.wikipedia.org/wiki/Internet_protocol_suite) layers
Layers top down
| Layer       | Example         | Purpose                               |
| ----------- | --------------- | ------------------------------------- |
| Application | HTTPS           | User Functionality like web browsing       |
| Transport   | TCP             | Moving connection information via packets |
| Internet    | IP              | Establishing and keeping connections              |
| Link        | Fiber, hardware | Physical connections                  |

other applications : web (HTTP), mail (SMTP), files (FTP), remote shell (SSH), and chat (IRC).


# Web Servers
Computing device that is hosting a web service that knows how to accept incomign internet connections and speak HTTP application protocol

## Monolithic Web Servers
* used to install massive, expensive software that spoke HTTP onto hardware server
* web server = server + software

# combining web and application services
* most programming languages include libraries to make connections and serve HTTP
* can easily build web servies into web application

# web service gateways - (see CADDY for our gateway)
multpile web services running on same device require different ports to connect to each one of them

port number is mapped to by a service gateway (reverse proxy) through common **HTTPS port 443**

a reverse proxy (gateway) listens at 443 and maps request to other services running on different ports

## microservices 
web services that provide a single functional purpose 
* partition functionality in small logical chuncks
* able to scale by running more and more stateless copies on multiple virtual services

## Serverless
functionality where server is conceptually removed from architecture and write a function that speaks HTTP

function is loaded through a gateway that maps web request to the function
* gateway scales the hardware needed to host serverless function based on demand
* Reduces what web app. developer needs to think about down to single independent function


