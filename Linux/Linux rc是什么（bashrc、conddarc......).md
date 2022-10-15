在Linux中，最为常用的缩略语也许是“rc”，它是“runcomm”的缩写――即名词“run command”(运行命令)的简写。rc”是任何脚本类文件的后缀，这些脚本通常在程序的启动阶段被调用，通常是Linux系统启动时。如/etc/rc（连接到/etc/rc.d/rc）是Linux启动的主脚本，而.bashrc是当Linux的bash shell启动后所运行的脚本。

.bashrc的前缀“.”是一个命名标准，它被设计用来在用户文件中隐藏那些用户指定的特殊文件;“ls”命令默认情况下不会列出此类文件，“rm”默认情况下也不会删除它们。许多程序在启动时，都需要“rc”后缀的初始文件或配置文件，这对于Unix的文件系统视图来说，没有什么神秘的。
```Linux
[root@minimal test-rm]# pwd

/home/huage/test-rm

[root@minimal test-rm]# ls -Al

total 0

-rw-r--r--. 1 root root 0 Apr  2 11:50 001

-rw-r--r--. 1 root root 0 Apr  2 11:50 002

-rw-r--r--. 1 root root 0 Apr  2 11:43 .003

-rw-r--r--. 1 root root 0 Apr  2 11:43 .004

[root@minimal test-rm]# rm -rf *

[root@minimal test-rm]# ls -Al

total 0

-rw-r--r--. 1 root root 0 Apr  2 11:43 .003

-rw-r--r--. 1 root root 0 Apr  2 11:43 .004
```

"rc" (像是 ".cshrc" 或 "/etc/rc" 中的 rc 这两个字母) = "RunCom"　 

"rc" 是取自 "runcom", 来自麻省理工学院在 1965 年发展的 CTSS系统。相关文献曾记载这一段话："具有从档案中取出一系列命令来执行的功能；这称为 "run commands" 又称为 "runcom"，而这种档案又称为一个 runcom (a runcom)。"

 awk = "Aho Weinberger and Kernighan" 

This language was named by its authors, Al Aho, Peter Weinberger and Brian Kernighan. 

  

grep = "Global Regular Expression Print" 

grep comes from the ed command to print all lines matching a certain pattern g/re/p where "re" is a "regular expression".

  rc (as in ".cshrc" or "/etc/rc") = "RunCom" 

"rc" derives from "runcom", from the MIT CTSS system, ca. 1965. 'There was a facility that would execute a bunch of commands stored in a file; it was called "runcom" for "run commands", and the file began to be called "a runcom." "rc" in Unix is a fossil from that usage.' 

  

Perl = "Practical Extraction and Report Language" 

Perl = "Pathologically Eclectic Rubbish Lister" 

The Perl language is Larry Wall's highly popular freely-available completely portable text, process, and file manipulation tool that bridges the gap between shell and C programming (or between doing it on the command line and pulling your hair out). For further information, see the Usenet newsgroup comp.lang.perl.misc.