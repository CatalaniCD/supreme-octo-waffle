# Shell

A shell is a computer program which exposes an operating system's services to a human user or other programs. In general, operating system shells use either a command-line interface (CLI) or graphical user interface (GUI), depending on a computer's role and particular operation.

Operating systems provide various services to their users, including file management, process management (running and terminating applications), batch processing, and operating system monitoring and configuration. 

source : https://en.wikipedia.org/wiki/Shell_(computing)

## Bourne Shell

The Bourne shell, sh, was a new Unix shell by Stephen Bourne at Bell Labs. Distributed as the shell for UNIX Version 7 in 1979, it introduced the rest of the basic features considered common to all the later Unix shells, including here documents, command substitution, more generic variables and more extensive builtin control structures. The language, including the use of a reversed keyword to mark the end of a block, was influenced by ALGOL 68. Traditionally, the Bourne shell program name is sh and its path in the Unix file system hierarchy is /bin/sh. But a number of compatible work-alikes are also available with various improvements and additional features

source : https://en.wikipedia.org/wiki/Unix_shell#Bourne_shell

## Bourne Again Shell (Bash)

Bash is a **Unix shell and command language** written by Brian Fox for the GNU Project as a free software replacement for the Bourne shell. First released in 1989, **it has been used as the default login shell for most Linux distributions**. A version is also available for Windows 10 via the Windows Subsystem for Linux. It is also the default user shell in Solaris 11. Bash was also the default shell in all versions of Apple macOS prior to the 2019 release of macOS Catalina, which changed the default shell to zsh, although Bash remains available as an alternative shell.

Bash is a **command processor that typically runs in a text window where the user types commands that cause actions**. Bash can also **read and execute commands from a file, called a shell script**. Like most Unix shells, it supports **filename globbing (wildcard matching), piping, here documents, command substitution, variables, and control structures for condition-testing and iteration**. The **keywords, syntax, dynamically scoped variables and other basic features of the language are all copied from sh**. Other features, e.g., history, are copied from csh and ksh. Bash is a POSIX-compliant shell, but with a number of extensions.

The shell's name is an acronym for **Bourne Again Shell(Bash)**, a pun on the name of the Bourne shell that it replaces and the notion of being "born again".

A security hole in Bash dating from version 1.03 (August 1989), dubbed Shellshock, was discovered in early September 2014 and quickly led to a range of attacks across the Internet. Patches to fix the bugs were made available soon after the bugs were identified. 

source : https://en.wikipedia.org/wiki/Bash_(Unix_shell)

**Compiling and Running C++, using pipes & arguments**

    #!/bin/bash
    g++ $1 | ./a.out
    echo "\nstatus : file compiled & executed"

**Conditional Execution**
    
    #!/bin/bash
    read name
    if [ -d $name ]
    then
        cd $name
        touch helloworld.cpp
        echo "File created"
    else
        echo "$name is not a directory"
    fi

**Loop Execution**

While

    #!/bin/sh
    read number
    counter=1
    while [ $counter -le 10 ]
    do
        multiply=$((number*counter))
        echo "$number x $counter = $multiply"
        counter=$(($counter+1))
    done

Until    

    #!/bin/sh
    read number
    counter=1
    until [ $counter -gt 10 ]
    do
       multiply=$(($number*$counter))
       echo "$number x $counter = $multiply"
       counter=$(($counter+1))
    done
    
**File System Recursive Tree Search**

    #!/bin/sh
    listR() # Case of in-order recursion : start on a, a1, a11, a111, a12, a13, a121, 
    {
            cd $1
            echo -e "\n Directory : $1"
            ls --color=auto
            list=`ls`
            for file in $list
            do
                    if [ -d $file ]
                    then
                            listR $file
                            cd ..
                    fi
            done
    }

    listR .

**Error Handling**

    #!/bin/bash

    function try()
    {
        [[ $- = *e* ]]; SAVED_OPT_E=$?
        set +e
    }

    function throw()
    {
        exit $1
    }

    function catch()
    {
        export ex_code=$?
        (( $SAVED_OPT_E )) && set +e
        return $ex_code
    }

    function throwErrors()
    {
        set -e
    }

    function ignoreErrors()
    {
        set +e
    }
