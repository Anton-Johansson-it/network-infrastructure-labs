# Linux Internet Services – DNS, Web and Server Administration

Practical Linux server administration lab focused on deploying and securing
network services across two Linux servers.

## Technologies

- Linux
- BIND9
- Apache2
- iptables
- SSH
- rsyslog
- logrotate
- SNMP
- NetBox
- Python / Bash

## DNS

Configured an authoritative DNS environment using BIND9 with a primary and
secondary DNS server.

The configuration included:

- Primary and secondary DNS servers
- Forward and reverse DNS zones
- Zone delegation
- Automatic zone transfers between primary and secondary servers
- Restricted recursive DNS queries
- A, AAAA, PTR, CNAME, MX, SOA and LOC records
- DNS validation and troubleshooting using `dig`

## Linux Security and Firewall

Configured and verified Linux server security including:

- iptables firewall rules
- SSH access
- Disabled SSH root login
- Login protection using faillock
- Firewall packet counters for troubleshooting and traffic verification

## Web Server

Configured Apache2 with multiple virtual hosts.

The implementation included:

- Name-based virtual hosts
- Disabled default virtual host
- Disabled directory listing
- Reduced Apache version information in error responses
- Dynamic server-side scripts
- DNS aliases for web services

## Monitoring with SNMP

Used SNMP to retrieve system and network information from routers and Linux
servers, including:

- System uptime
- CPU load
- Available memory
- Network interface traffic

The information was displayed dynamically through scripts hosted on the
Apache web server.

## Logging

Configured centralized logging between the Linux servers.

This included:

- Forwarding BIND logs between servers
- Logging firewall connection attempts
- Dedicated connection log files
- Log rotation to prevent excessive disk usage
- Verification of available filesystem and log storage capacity

## Infrastructure Documentation

Documented the Linux servers in NetBox including hardware resources,
network interfaces, IP addressing and VLAN information.

## Skills Demonstrated

- Linux server administration
- DNS administration with BIND9
- Web server administration with Apache2
- Firewall configuration and troubleshooting
- Centralized logging
- Network monitoring with SNMP
- DNS troubleshooting
- Infrastructure documentation
