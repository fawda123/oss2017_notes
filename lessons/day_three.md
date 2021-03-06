# Day three - 7/12
Marcus W. Beck, beck.marcus@epa.gov  

### Unix command line tools

Use this for bash commands in Rmd ` ```bash ` ` ``` `

Text editors for Unix systems - vim, emacs, or nano, all run from CLI.  For example, run this to start the text editor: 

```bash
~$ nano myfile.txt
```

Then use `Ctrl + ` something to run commands, `^` is for ctrl.  

RStudio can also be used on aurora to edit files.  

Other useful unix commands:

* `wc` count lines, words, characters
* `diff` compare files
* `sort` sort lines in a file
* `uniq` report/filter repeated lines in a file (`sort` must be used first)

Unix commands are `stdin` for input data, then two streams out for `stdout` for normal output and `stderr` for error output (`std` is standard).  There are operators to manipulate those in/as a pipe `|`.  You can choose to do different things with the output.

For example, redirect the standar error (second pipe) to some null place: 

```bash
$ ls fakefile.txt 2> dev/null
```

Don't forget to check manual for options: 
```bash
man grep
```

Nest functions in Unix: `<(sort paleo-mammals.txt)`

To go up a directory `../../mydir` goes up two directories to `mydir`

For unix, git options, `-l` single hyphen for abbreviated options, `--list` double hyphen for options in full.

`cut` functions let you pull out columns from a delimited text file.  

`join` files is like the join functions in dplyr, sorta.  

`sed` filters lines in a file. 

### Bash loops

Programming philosophy - don't repeat yourself (DRY)

The basic loop syntax in bash:

```bash 
$ for filen in paleo*
  do echo $filen
done
```
This just prints file names to the CLI. 

In bash, `>` is equivalent to `+` in R, prints this when it expects something else after a command. 

You can use `;` to put more than one command on the same line in bash (different from piping, like as in a loop).

To put the output (`stdout`) as input (`stdin`) to something else you can use this symbol below tilde to enclose the input:
```bash
for i in `seq 1 10`
  do echo "this is my $i"
done
```

### Simple bash scripts

To create a shell script, top line starts with a `#1/bin/bash` to tell the shell which language the script is written for.  Hash-bang is `#1`.

To execute a script from CLI, precede with `./`. `@` is a generic variable that the system uses?  

An example bash script:
```bash
#!/bin/bash

# Example of a simple shell script
# Do not really use this for backup!
PREFIX="backup-"
FILES=$@
for file in $FILES
do
    cp $file $PREFIX$file
done
```

This can be executed from CLI:
```bash
./crazy-back.sh paleo*
```
where all paleo* files are executed with the script, used within the script as `@`. 

### Data management and data repositories

Big data - volume, velocity, and variation

Data entropy - loss of data specificity with time from publication.  

Synthesis research concerned with discovery, integration, and analysis of data as subsets of the data life cycle.  But these steps are wholly dependent on the others.  

Barriers to synthesis research:
* data have not been preserved
* if preserved, data are present in very dispersed, isolated repositories
* lake of software interoperability
* heterogeneity of data formats

Solutions to synthesis research:
* preserve
* adopt standards
* create networks
* create interoperable software

Examples of data repos: tdar, usgs, dryad, knb, ncei, arctic data center

[re3data.org](https://www.re3data.org) - database of over 3000 data repositories - indexed by subject, domain, data type, etc. 
