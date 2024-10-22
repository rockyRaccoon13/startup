# Technology Stack

the collection of technologies used to create or deliver web application

our Stack : 

![essentialsTechStack260](https://github.com/user-attachments/assets/f3f068a3-434b-4bc8-9769-e2f92394e32c)

 - React for the web framework
 - talking to Caddy as the web server hosted on AWS
 - running web services on Node.js
 - and MongoDB as the databse hosted on MongoDB atlas



## AWS 

### EC2 service -- renting a server (and its IP address)
Used to rent a server -- access by IP address, make elastic IP

### Route 53
AWS service that handles everything DNS-related (buy domain name, host your domain on their DNS servers, create DNS records)
Why Domain name:
* referring to server by IP address is fine for development, but not for most users
* HTTPS requires a Domain name

##### DNS Records
http://www.google.com
protocol sub domain. **domain name. top-level domain  (Root Domain, part you register)**

- `A` record maps domain names to IP addresses  (we create 2 A records.  to our root domain as well as * wild card for sub domains)
- `CNAME` maps domain names to other domain names
-  The name server `(NS)` record contains the names of the authoritative name servers that authorize you to place DNS records in this DNS server
-  The start of authority `(SOA)` record provides contact information about the owner of this domain name.


## Caddy -- our gateway aka reverse proxy
* handles creation and rotation of web certificates -- allows us to support HTTPS easily
* web service that listens for incoming HTTP requests
* serves up requested static files
* **or** routes to another service (multiple services reverse proxied by a single web service (Caddy))

Caddy is preinstalled on our server through the class mirror. just need to configure root domain name

 ![cadddy](https://github.com/user-attachments/assets/a8659f09-ac09-4e38-865c-5786707b208e)

### caddy files

note ports 80, 443 are HTTP and HTTPS for web requests

Configuration file: ~/Caddyfile
* definitions of  routing HTTP requests

  
HTML files: ~/public_html
* directory of files that caddy serves up when requests are made to root (this is set up in the CaddyFile config file)
  

