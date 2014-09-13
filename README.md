bind9-generator
===============

Generates complete bind9 configuration files for a simple DNS setup. 

##Description
For a simple DNS setup on a recent Debian based system only three bind9 configuration files are involved:
* /etc/bind9/named.conf.local
* zones/rev.168.1.192.in-addr.arpa
* zones/tld.domain.db

The first two files are shared among all domains on the server. The third file is unique for a domain. 

The bash script in this repository will read the domains and their associated IP addresses from a file. This file is formatted as:

    # domain	  IP address
    my-url.com	  123.234.45.56
    my-url.me	  123.234.45.56




