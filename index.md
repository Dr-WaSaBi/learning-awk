# My Awk learning guild

For me, one of the best ways to learn something, is to try to teach it.  So here is me, trying to learn AWK.

## What is Awk

Awk is a text, or data processing programming language created back in the mid to late 70's by some of the founders of the Unix operating system at Bell labs.  (Need details)

It's really good at processing a text file, line by line. Doing something with the data it finds on that line, and creating output of what it finds or sums up.

## The basics of Awk

### How to run Awk
---
You can run Awk commands in one of two ways.  As what is called an Awk 1 Liner, or by creating a awk script file, with what you want the awk program to do inside of it.

___The Awk 1 liner___
```bash
awk '/search/ {print $0}' datafile.txt
```
This is what as know as a awk 1 liner.  Here the awk program is called, and it reads a line of input in from datafile.txt. It searches that line for what ever is between the slashs '/ /', if it finds a match it prints out that whole line. $0 is the awk variable for the whole line read in. $1 would be the first item on the list, $2 the seconds, and so on.

___Awk scripts___

Awk scripts are just a text file with awk commands in side. Also these files are created in the awk format.

So you would have a file, maybe called it ***my-first-awk-script.awk***.

In that file, you could have awk commands like.
```bash
#! /usr/bin/awk

/what-Im-looking-for/ {print $0}
```
To run your little script, you can do it a couple of ways.  The simplest being
```bash
awk -f my-first-awk-script.awk datafile.txt
```

### Awk command line options
There are tons of command like options that you can pass into awk.  The most common are going to be
- -f = the awk script file to read, as seen above.
-  -F = the delimiter to look for, normaly this is a space or a tab. But you can change it to pretty much anything you want.

```bash
awk -F',' # break the line apart at commas, great for reading in csv files.

```
## The Details of Awk
---

### The format of Awk
---

### Variables in Awk
---
#### Awk's built in variables

#### User defined variables

### Operators
---
### Conditional / Flow controls
---
### Looping around in Awk
---
## End of File
