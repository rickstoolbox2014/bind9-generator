bind9-generator
===============

Generates relevant bind9 configuration files for a simple DNS setup (for Debian).

##Description
For a simple DNS setup on a recent Debian based system only three bind9 configuration files are involved:
* /etc/bind9/named.conf.local
* /etc/bind9/zones/rev.168.1.192.in-addr.arpa
* /etc/bind9/zones/tld.domain.db

The first two files are shared among all domains on the server. The third file is unique for a domain. 

The bash script in this repository will read the domains and their associated IP addresses from a file. This file is formatted as:

    # domain	  IP address
    com.my-url	  123.234.45.56
    me.my-url	  123.234.45.56
    org.my-url	  123.234.45.56

Please note that domains are listed in the **zone** notation (*tld first*).

The script has been tested with bind9 rev. 1:9.8.4.dfsg.P1-6+nmu2+deb7u1.
