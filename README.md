# Full Stack FrontEnd
Full stack is someone who can build an application from start to finish, including front end and backend.

**Why Fullstack**

You can master all the techniques involved in a development project. You can make a prototype very rapidly. You can provide help to all the team members.
Full stack developers ensure the openness of application and they also work alongside graphic designers as well for features of web design and many other tasks. They are necessary to look into web projects from the start to its final form.


# Understanding the Internet
It works by using a packet routing network that follows Internet Protocol (IP) and Transport Control Protocol (TCP) [5]. TCP and IP work together to ensure that data transmission across the internet is consistent and reliable, no matter which device you're using or where you're using it. Basically a series of system globally interconnected devices. Not to be confused with intranet, which basically internet but private.

Some list to understand the internet better :
-   internet - A system of globally interconnected devices
-   intranet - Private internet
-   IP - Internet Protocol
-   IP Address - A label assigned to an internet connected device
-   IPv4 - It is the underlying technology that makes it possible for us to connect our devices to the web. Whenever a device accesses the Internet, it is assigned a unique, numerical IP address such as  `8.8.8.8`.
-   IPv6 - is the most recent version of the Internet Protocol (IP), the communications protocol that provides an identification and location system for computers on networks and routes traffic across the Internet. IPv6 addresses are represented as eight groups of four hexadecimal digits each, separated by colons such as  `2001:4860:4860:8888`
-   TCP - Transmission Control Protocol
-   UDP - User Datagram Protocol
-   DNS - Domain Name System
-   Nameservers - Map domains to IP addresses
-   ICMP - Internet Control Message Protocol is a network layer protocol used by network devices to diagnose network communication issues.
-   Packets - a packet that contain the smallest bit of information you can transmit.

# Servers
It serves content and also respond request, it serves something back.

**VIM**
Vim is a free and open-source, screen-based text editor program for Unix. It is an improved clone of Bill Joy's vi. Some more vim  [command cheat sheets](https://linuxmoz.com/vi-commands-cheat-sheet/)

**Data centers and the cloud**
Servers generally live in place called data center, a place full or racks of machine in a really cold environments. So a data center is just this colletions of computers, often shared between application and/or different companies.


# Server Setup
Example where you can buy a  [domain](http://www.namecheap.com/)

**DNS Record**

DNS records (aka zone files) are instructions that live in authoritative DNS servers and provide information about a domain including what IP address is associated with that domain and how to handle requests for that domain. These records consist of a series of text files written in what is known as DNS syntax.

**Domain Setup**

Add 2 A Records with your IP address
- @
- www
- use digitall ocean to add domain
- update nameserver on namecheap
 
 **Server Setup**
Some thing that you might want to do to setup the server :
-   Update software
-   Create a new user
-   Make that user a super user
-   Enable login for new user
-   Disable root login

Some command line example : Update software
```
# apt update
```

Upgrade software
```
# apt upgrade
```
Add new user
```
# adduser $USERNAME
```
Add user to “sudo” group
```
# usermod -aG sudo $YOUR_USERNAME
```
Switch user
```
# su $YOUR_USERNAME
```
Check sudo access
```
$ sudo cat /var/log/auth.log
```
Change to home directory
```
$ cd ~
```
Create a new directory if it doesn’t exist
```
$ mkdir -p ~/.ssh
```
Create authorized_keys file and paste PUBLIC key
```
$ vi ~/.ssh/authorized_keys
```
Exit
```
$ exit
# exit
```
Login with new user
```
$ ssh $USERNAME@IP_ADDRESS
```
Change file permissions
```
$ chmod 644 ~/.ssh/authorized_keys
```
Disable root login
```
$ sudo vi /etc/ssh/sshd_config
```
Restart ssh daemon
```
$ sudo service sshd restart
```

# Nginx

Nginx, stylized as NGINX, nginx or NginX, is a web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache. The software was created by Igor Sysoev and publicly released in 2004. Nginx is free and open-source software, released under the terms of the 2-clause BSD license. it can do or act as :

-   Reverse proxy
-   Web server
-   Proxy server

**Nginx Setup**
Some of nginx command line : Install nginx
```
$ sudo apt install nginx
```
Start nginx
```
$ sudo service nginx start
```
Show nginx configuration
```
$ sudo less /etc/nginx/sites-available/default
```
Create and edit index.html
```
$ sudo vi /var/www/html/index.html
```

