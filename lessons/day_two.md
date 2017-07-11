# Day two - 7/11
Marcus W. Beck, beck.marcus@epa.gov  


### Version control: git basics

Distributed - you have the entire history of a git project on your local machine, applies to everyone working separately on a the same project. 

See the git manual:

```r
system('git', intern = TRUE)
```

```
##  [1] "usage: git [--version] [--help] [-C <path>] [-c name=value]"                     
##  [2] "           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]"      
##  [3] "           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]"       
##  [4] "           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]"         
##  [5] "           <command> [<args>]"                                                   
##  [6] ""                                                                                
##  [7] "These are common Git commands used in various situations:"                       
##  [8] ""                                                                                
##  [9] "start a working area (see also: git help tutorial)"                              
## [10] "   clone      Clone a repository into a new directory"                           
## [11] "   init       Create an empty Git repository or reinitialize an existing one"    
## [12] ""                                                                                
## [13] "work on the current change (see also: git help everyday)"                        
## [14] "   add        Add file contents to the index"                                    
## [15] "   mv         Move or rename a file, a directory, or a symlink"                  
## [16] "   reset      Reset current HEAD to the specified state"                         
## [17] "   rm         Remove files from the working tree and from the index"             
## [18] ""                                                                                
## [19] "examine the history and state (see also: git help revisions)"                    
## [20] "   bisect     Use binary search to find the commit that introduced a bug"        
## [21] "   grep       Print lines matching a pattern"                                    
## [22] "   log        Show commit logs"                                                  
## [23] "   show       Show various types of objects"                                     
## [24] "   status     Show the working tree status"                                      
## [25] ""                                                                                
## [26] "grow, mark and tweak your common history"                                        
## [27] "   branch     List, create, or delete branches"                                  
## [28] "   checkout   Switch branches or restore working tree files"                     
## [29] "   commit     Record changes to the repository"                                  
## [30] "   diff       Show changes between commits, commit and working tree, etc"        
## [31] "   merge      Join two or more development histories together"                   
## [32] "   rebase     Reapply commits on top of another base tip"                        
## [33] "   tag        Create, list, delete or verify a tag object signed with GPG"       
## [34] ""                                                                                
## [35] "collaborate (see also: git help workflows)"                                      
## [36] "   fetch      Download objects and refs from another repository"                 
## [37] "   pull       Fetch from and integrate with another repository or a local branch"
## [38] "   push       Update remote refs along with associated objects"                  
## [39] ""                                                                                
## [40] "'git help -a' and 'git help -g' list available subcommands and some"             
## [41] "concept guides. See 'git help <command>' or 'git help <concept>'"                
## [42] "to read about a specific subcommand or concept."                                 
## attr(,"status")
## [1] 1
```

See your global configurations:

```r
system('git config --global --list', intern = TRUE)
```

```
## [1] "user.email=mbafs2012@gmail.com" "user.name=fawda123"
```

Save your user credentials:

```r
# forever
system('git config --global credential.helper cache', intern = TRUE)

# for an hour
system("git config --global credential.helper 'cache --timeout=3600'", intern = TRUE)
```

Show hidden files using `ls -a`, show files recursively `ls -R`. Look into cygwin or commander for a good windows shell.  

`git clone` copy a remote repo to your local machine.  

`vim favorite_desserts.csv` creates a file and enters the interactive text editor.  Enter text as needed.  To exit, press esc, `:w` to save, `:q` to quit.  
 
 Or enter text from command line. 
 ```
 echo 'line 1, line 1' > favorite_desserts.csv
 ```
 To append to a file, use two carets `>>`.
