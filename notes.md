# Notes Overview
Notes for cs 260 -- Benson Rowley


[my startup README.md ](README.md)

## Class Resources
[Class schedule](https://github.com/webprogramming260/.github/blob/main/profile/schedule/VenturaF2024.md)

[Class simon iterations](https://github.com/webprogramming260/.github/blob/main/profile/essentials/simon/simon.md)


#My AWS Server/ Website/ IP
**TODO**
- when done with class terminate instance 
- release elastic IP (else will bill $3 per month)

My AWS Server:
command to SSH into server remote

`ssh -i [key path] ubuntu@52.73.160.154`

or

`ssh -i [key path] ubuntu@kbrbyucs260.click`


my elastic IP: `52.73.160.154`   
website: [https://kbrbyucs260.click/](https://kbrbyucs260.click/)
- ~[http://52.73.160.154/](http://52.73.160.154/)~ ip website no longer valid due to setting up https 



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

#### DNS Records
http://www.google.com
protocol sub domain. **domain name. top-level domain  (Root Domain, part you register)**

- `A` record maps domain names to IP addresses  (we create 2 A records.  to our root domain as well as * wild card for sub domains)
- `CNAME` maps domain names to other domain names
-  The name server `(NS)` record contains the names of the authoritative name servers that authorize you to place DNS records in this DNS server
-  The start of authority `(SOA)` record provides contact information about the owner of this domain name.



