# Day one - 7/10
Marcus W. Beck, beck.marcus@epa.gov  

### Week 1 

Fundamental data and collab skills - command line, comunicating science, R, meta-analysis and data management

### Code of conduct

A community document, review, contribute, etc. good for collaborative work.

### Networks and Servers

Network - physical or other connection between computers.

Local network - physical connection, area network is > 2 comps. All computers are equally connected. Broadcast - sending a message, 

Routing network, e.g., connecting networks through routers, routers know how to send info across networks. Router network may not be linear.

Each host (e.g., personal comp) has an IP address, we use NCEAS address for workshop (it changes)

```r
system('ipconfig', intern = T)
```

```
##  [1] ""                                                                   
##  [2] "Windows IP Configuration"                                           
##  [3] ""                                                                   
##  [4] ""                                                                   
##  [5] "Ethernet adapter Local Area Connection* 5:"                         
##  [6] ""                                                                   
##  [7] "   Connection-specific DNS Suffix  . : epa.gov"                     
##  [8] "   Link-local IPv6 Address . . . . . : fe80::c88c:4ba1:f1bc:8693%25"
##  [9] "   IPv4 Address. . . . . . . . . . . : 10.145.12.15"                
## [10] "   Subnet Mask . . . . . . . . . . . : 255.255.255.255"             
## [11] "   Default Gateway . . . . . . . . . : "                            
## [12] ""                                                                   
## [13] "Ethernet adapter Ethernet:"                                         
## [14] ""                                                                   
## [15] "   Media State . . . . . . . . . . . : Media disconnected"          
## [16] "   Connection-specific DNS Suffix  . : "                            
## [17] ""                                                                   
## [18] "Wireless LAN adapter Local Area Connection* 3:"                     
## [19] ""                                                                   
## [20] "   Media State . . . . . . . . . . . : Media disconnected"          
## [21] "   Connection-specific DNS Suffix  . : "                            
## [22] ""                                                                   
## [23] "Wireless LAN adapter Wi-Fi:"                                        
## [24] ""                                                                   
## [25] "   Connection-specific DNS Suffix  . : nceas.ucsb.edu"              
## [26] "   Link-local IPv6 Address . . . . . : fe80::30d0:992c:ae91:98d3%2" 
## [27] "   IPv4 Address. . . . . . . . . . . : 128.111.220.220"             
## [28] "   Subnet Mask . . . . . . . . . . . : 255.255.255.0"               
## [29] "   Default Gateway . . . . . . . . . : 128.111.220.1"               
## [30] ""                                                                   
## [31] "Ethernet adapter Bluetooth Network Connection:"                     
## [32] ""                                                                   
## [33] "   Media State . . . . . . . . . . . : Media disconnected"          
## [34] "   Connection-specific DNS Suffix  . : "                            
## [35] ""                                                                   
## [36] "Tunnel adapter Local Area Connection* 14:"                          
## [37] ""                                                                   
## [38] "   Media State . . . . . . . . . . . : Media disconnected"          
## [39] "   Connection-specific DNS Suffix  . : "
```

Connect to remote server (NCEAS):

```r
ssh myname@aurora.nceas.ucsb.edu
```

Then enter password.


