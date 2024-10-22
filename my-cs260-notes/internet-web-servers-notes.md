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


# Domain Names
look up IP through `dig`
* some domain names are redundant - have multpile IPs that are valid (i.e. amazon.com)
* must follow namming convention and listed in the domain name registry

[subdomain]\***secondary.top**    ** bold is root domain **
* ICAAN controls list of possible TLDs
* any number of sub domains, each may resolve to different IP address

`whois` looks up info about a domain name in domain name registry

## DNS 
once domain is in registry it can be listed with a domain name system (DNS) server and associated with an IP address. Each DNS server in world referenice a few DNS servers that are 'authorative name servers' for associating domain name with an IP address

An `address (A)` record is a straight mapping from a domain name to IP address. A `canonical name (CNAME)` record maps one domain name to another domain name (CNAME for byu.com to same IP as byu.edu). 


### Entering domain in browser, getting back IP
browser checks cache to see if name already exists, broswer contacts a DNS server (also see if cached), DNS contacts a autorative name server. 

if authority does not know name, unkown domain name error.
Else, process resolves and browser makes HTTP connection to associated IP address

caching may cause problems with updating info with domain name. `time to live (TTL)` setting allows you to set time until all caching layers honor and clear cache after requested period


## Leasing  a domain name

Either buy (every year have to register from domain registrar) or sublease (from private party)
* buying gives you right to extended
