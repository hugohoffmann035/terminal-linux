# **Linux terminal command line**

## **Sobre**
### ss is used to dump socket statistics. It allows showing information similar to netstat.  It can display more TCP and state information than other tools.
[Documentation](https://man7.org/linux/man-pages/man8/ss.8.html)

### **Listing**
### Copy and past in terminal
```
// Network Connections
ss

// Listing Listening Sockets
ss -l

// Listing All Sockets
ss -a

// Listing TCP Sockets
ss -a -t

// Listing UDP Sockets
ss -a -u

// Listing Unix Sockets
ss -a -x

// Listing Raw Sockets
ss -a -w

// Listing IP Version 4 and 6 Sockets
ss -a -4
ss -a -6

// Listing Sockets By Protocol
ss -a state established ‘( dport = :https or sport = :https )’
ss -a ‘( dport = :ssh or sport = :ssh )’
ss -a ‘( dport = :22 or sport = :22 )’

// Listing Connections to a Specific IP Address
ss -a dst 192.168.4.25

// Listing Connections to a specific process
ss -tulpn | grep node 
```