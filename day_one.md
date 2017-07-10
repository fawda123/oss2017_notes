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

Then enter password. Run `exit` to disconnect from server. 

Get a password manager- one password, last pass (free).

Cloud computing - like networking but you don't own the hardware. 

### Thinking preferences

Intellectual, rational, instinctive, intuitive - you have all of these, know how to use them. I am not big-picture, holistic or emotional/intuitive by nature but I can access these. This is a tool though, it raises awareness of different modes of thinking.

### Introduction to command-line computing

Look [here](https://nceas.github.io/oss-lessons/servers-networks-command-line/2-commandline-intro.html)

Repeatibility and Efficiency - that's what it's all about. 

The standard OS model - software as applications and operating system, hardware as CPU, RAM, I/O 

Unix - everyone has their own user space, focuses on one tool/one command which can be chained together.

Unix commands (file moving, creating, etc):

* `cp` copy, `mv` move
* `mkdir` makes a directory
* `echo` put something in a file > myfile.txt
* `cat` concatenate or print something from a file
* `>` redirection operator to make a file
* `cd` change directory, `cd ..` goes up to the parent directory
* `ls` list or show files in a directory
* `pwd` prints the workign directory, `tree .` shows file tree in current directory
* `mv` moving a file or just changing a name of a file
* `rm` remove/delete a file, use `rm -r mydir` removes a directory with files recursively
* `rmdir` removes directories, but it's not recursive
* `|` is a pipe that sends output from one command to another
* `man` says find a help file (manual) for a command, e.g., `man grep`

Reading text files in Unix:

* `cat` print a file
* `head` show top of file
* `tail` show bottom of file
* `grep` search for matching lines, e.g., `grep findme data/plotobs.csv`
* `less` view file interactively


File folders are shown in blue in Unix CLI (command line interface)

Aurora server uses Ubuntu.

Every directory has one parent but a parent might have several children.

tab completion works in unix for typing files. 
