# Introduction

Have you ever wondered about how git does all the version control magic? Today we're going to implement the algorithm behind git, by the end of the tutorial, you will have a working version control system like git.

Before starting this tutorial you should have a basic understanding of git usage (init, commit etc), you can follow this tutorial in any OOP language.

I'll give you a brief overview of what we're going to write
- How to handle CLI commands
- How to represent git object internally
- Write unit tests for your code

We don't want to reinvent too many wheels, that's why we're calling help from third party libraries. I'm writing this program in Java 17. 

You should have a solution for:  
- **CLI Parser**: In my case I'm using [PicoCLI](https://picocli.info/), there are other alternatives like [JCommander](https://jcommander.org/) and [Apache Commons CLI](https://commons.apache.org/proper/commons-cli/), I didn't use them because the support for sub-commands is weak, I think PicoCLI really shine in this aspect. Your choice of CLI parser should be able to support flag, optional argument, help message and sub-commands.
- **Compression & Decompression**: Your compression library should be able to support [ZLib compression](https://en.wikipedia.org/wiki/Zlib), which is what git uses internally. Java has built in Deflater class in this case.
- **INI file parser**: We're using [ini4j](http://ini4j.sourceforge.net/), git stores config file in this format

My final implementation will be available at [my repo](https://github.com/LeeTeng2001/my-git). Feel free to check it out if you're stuck!