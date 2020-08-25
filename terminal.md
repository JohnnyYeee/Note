Mac OS Terminal 基本指令（全）
 

Mac OS X 启用超级用户的方法
Root user，又名超级用户，是一个权力最高的Unix 账户，Root 的账户能在整个系统里任何部份进行任何“操作”，包括：拷贝档案、移动/移除档案、执行程序等。所以，通常 Root 的账户都只会指派给高级专业的用户使用。因此，苹果把Root user 隐藏在Mac
OS X 里。
但有时候我们不得不启用Root用户以便于实现某些操作，可以通过以下三种方法把启动Root账户。
方法一：
把Mac OS X 的安装光盘放入到光驱中，用光盘启动系统，在安装菜单里选择“Password Reset”选项，便能更改你的密码和启动超级用户模式。（把这工具拷贝到硬盘中是不能启动的，一定要从光盘启动才有效。）
方法二：
在Mac OS X里启动Terminal（在“应用程序/实用工具”的文件夹中），输入以下命令：
sudo passwd Root
系统会实时要求输入 Root user的新密码，然后再输入一次，以确保密码正确。
方法三：
启动NetInfo Manager应用程序（在“应用程序/实用工具”的文件夹中），再依照以 下步骤：
1. 从菜单中选择“域”→“用户”→“启动Root用户”
2. 点按窗口底部的“锁状”按钮，然后输入在安装过程中提供的用户名称和密码注册。
3. 从窗口下半部份的列表中选择 * 号一栏，再输入 Root user 已加密的新密码。可在 Terminal 里输入以下的「htpasswd」命令来产生加密的新密码：
[localhost:~] currentuser% htpasswd -nb anylogin yourpassword
[return]
[localhost:~] currentuser% anylogin : pu9fQgdzVHRB2
pu9fQgdzVHRB2 就是已加密的新密码
4. 点按窗口底部的“锁状”按钮，然后储存更改和离开 NetInfo Manager。
现在可以在 Terminal 里试试 Root user 的新密码如何通过终端命令删除Finder中无法删除的文件这里我先介绍一个经常性的问题。有人常常因为某种原因。比如死机、文件下载一半意外退，这时经 常有文件无法删除，系统提示你权限不够。这个时候我们就可以利用一行简单的命令进行删除。
当然有人会提出启动到os 9来删除，这样有两大问题。一是你需要重启两次机。先切到9。再切回x。还有就是对新机器来说，你根本就没办法从os 9启动。

 


言归正传，下面就举便说明：

  
1 打开终端应用程序

2 输入命令：sudo rm -r -f “你要删除的文件”
还要注意终端命令是区分大小写的，全部小写。

3 把你要删的文件或者文件夹用mouse拖进终端窗口，好多个也可以一起拖。

4 然后在终端中回车

5 输入当前管理员用户密码。如果没有密码就直接回车。注意不是root账号的密码。

6 终端中没有任何提示信息表明成功删除。

注意：如果用这个命令还无法删除，有两种可能性：一是你删除的是系统正在使用的临时文件之类的。二是有可能你的硬盘目录出现问题。这时请先用磁盘工具检查一下你的硬盘。

解释：
sudo 临时执行root账户操作，当你使用这个命令的时候等同于使用 root 用户进行操作，所以要当心。它后面一般是你要操作的其它命令。比如本例中的 rm。同时sudo 命令都要求你输入当前管理员用户密码。如果密码为空就直接回车。

rm 删除命令。即remove的缩写，它后面有两个参数。
-r 删除文件夹内的子文件夹及内容，一般情况下rm只能删 除文件或者空的文件夹。
-f 强制删除参数
如果需要了解rm命令的更多参数。请输入:man rm

其它常用命令
cd
进入某个目录

cp 原始文件 目标文件
复制文件，可带路径复制不到位置


kill -9 [PID]
結束指定的 PID 執行程式

ls
列出当前目录下所有文件

man [命令]
查询某个命令的使用方法

mkdir [目录]
新建目录

rmdir 目录
删除目录，注意只能是空目录

mv 原始文件 目录文件
移动或者重命名文件

passwd
更改密码


rm
删除文件
-f 强制删除
-i 删除前确认
-r 删除目录及子目录内容


sudo rm -rf ~/.Trash/*
强制删除当前用户垃圾箱内所有项目

top
显示所有进程。

kill -9 [PID]
结束PID进程

open -a itunes
打开aqua 程序itunes
删除不了的文件可以在终端里用 rm -rf 来删。
打开 应用程序－－实用程序－－终端
输入   sudo rm -rf .然后把要删除的文件拖进来。回车－－输入系统用户密码－－回车就行了。
下面是一些unix常用的命令，MAC系统的终端基本都可以用

a. 关於档案/目录处理的指令: 

1. ls
这是最基本的档案指令。 ls 的意义为 "list"，也就是将某一个目录或是某一个档案的内容显示出来。

如果你在下 ls 指令後头没有跟著任何的档名，它将会显示出目前目录中所有档案。

也可以在 ls 後面加上所要察看的目录名称或档案的名称，如

% ls /home2/X11R5

% ls first

ls 有一些特别的参数，可以给予使用者更多有关的资讯，如下:

-a : 在 UNIX 中若一个目录或档案名字的第一个字元为 "." , 则使用 ls将不会显示出这个档案的名字，我们称此类档案为隐藏档。如 tcsh的初设档 .tcshrc；如果我们要察看这类档案，则必须加上参数 -a 。

-l : 这个参数代表使用 ls 的长( long )格式，可以显示更多的资讯，如档案存取权，档案拥有者( owner )，档案大小，档案最後更新
曰期，甚而 symbolic link 的档案是 link 那一个档等等。如下

% ls -l

drwx--x--x 2 jjtseng 512 Aug 8 05:08 18
drwx--x--x 2 jjtseng 512 Aug 8 22:00 19
-rw------- 1 jjtseng 566 Aug 8 05:28 makefile

2. cp
cp 这个指令的意义是复制("COPY") , 也就是将一个或多个档案复制成另一个档案或者是将其复制到另一个目录去。

cp 的用法如下:

cp f1 f2 : 将档名为 f1 的档案复制一份为档名为 f2 的档案。
cp f1 f2 f3 ... dir : 将档案 f1 f2 f3 ... 都以相同的档名复制一份放到目录 dir 里面。
cp -r dir1 dir2 : 将 dir1 的全部内容全部复制到 dir2 里面。

cp 也有一些参数，如下:

-i : 此参数是当已有档名为 f2 的档案时，若迳自使用 cp 将会将原来 f2的内容掩盖过去，因此在要盖过之前必须先询问使用者一下。如使用者的回答是y(yes)才执行复制的动作。

-r : 此参数是用来做递回复制用，可将一整颗子树都复制到另一个目录中。

3. mv
mv 的意义为 move , 主要是将一档案改名或换至另一个目录。如同 cp ，它也有三种格式:

mv f1 f2 : 将档名为 f1 的档案变更成档名为 f2 的档案。
mv dir1 dir2 : 将档名为 dir1 的目录变更成档名为 dir2 的目录。
mv f1 f2 f3 ... dir : 将档案 f1 f2 f3 ... 都移至目录 dir 里面。

mv 的参数有两个，-f 和 -i , 其中 -i 的意义与 cp 中的相同，均是 interactive询问之意。而 -f 为强迫( force ) , 就是不管有没有同名的档案，反正我就是要搬过去，所有其他的参数遇到 -f 均会失效。

4. rm
rm 的意义是 remove ，也就是用来杀掉一个档案的指令。在 UNIX 中一个被杀掉的档案除非是系统恰好有做备份，否则是无法像 DOS 里面一样还能够救回来的。所以在做 rm 动作的时候使用者应该要特别小心。

rm 的格式如下:

rm f1 f2 f3 .....

而 rm 的参数比较常用的有几个: -f , -i , 与 -r

-f : 将会使得系统在删除时，不提出任何警告讯息。
-i : 在除去档案之前均会询问是否真要除去。
-r : 递回式的删除。

小心不要随便使用 rm -rf , 否则有一天你会"欲哭无泪"......

5. mkdir
mkdir 是一个让使用者建立一个目录的指令。你可以在一个目录底下使用midir 建立一个子目录，使用的方法如下:

mkdir dirname1 [ dirname2 ... ]

如此你就可以建立一个或多个目录。

6. chdir ( cd )
这是让使用者用来转移工作目录用的。
chdir 的用法如下:

chdir dirname

如此你就可以将目前的目录转移到 dirname 这一个目录去。或使用 "chdir .." 来转移到上一层目录。

7. rmdir
相对於 mkdir ，rmdir 是用来将一个"空的"目录杀掉的。如果一个目录下面没有任何档案，你就可以用 rmdir 指令将其除去。rmdir 的使用法如下:

rmdir dirname1 [ dirname2 .... ]

如果一个目录底下有其他的档案， rmdir 将无法将这个目录杀掉，除非使用rm 指令的 -r 选项。

8. pwd
pwd 会将目前目录的路径( path )显示出来，例如:

9. cat/more/less
以上三个指令均为察看档案内容的指令。cat 的意义是猫....不不不，是concatenate ，在字典上的意思是"连结,将…串成锁状"( 语出资工电子词典 cdict )，其实就是把档案的内容显示出来的意思。 cat 有许多奇怪的参数，较常为人所使用的是 -n 参数，也就是把显示出来的内容加上行号。 cat 的用法如下:

cat [-n] :自标准输入读进内容，你可以用 pipe 将别的程式的输出转向给 cat .
cat [-n] filename : 将 filename 的内容读进来，显示在标准输出上。

问题在於 cat 它是不会停下来的，因此并不好用( 试想如果一个萤幕二十四行，而一个档案四百行，cat 一出来将会劈哩啪啦不断的卷上去，使用者很难据此得到他们所需的资讯。) 所以才有人又写了 more 出来。

more , 跟据蔡文能老师的说法是"再多一点就好"，more 可以将所观察的档案跟据终端机的形态一页页的显示出来，再根据使用者的要求换页或卷行。如果使用者要在某一个档案中搜寻一个特定的字串，则按 / 然後跟著打所要搜寻的单字即可进行搜寻。more 也可以找得到。more 的使用法如下:

more filename

如果你在使用中觉得已经看到了所要看的部份，可以按'q'离开 more 的使用。在使用中按'v' 亦可以使用编辑器来编辑所观看的档案。

less 的用法与 more 极类似，原先它就是为了弥补 more 只能往前方卷页的缺点而设计。 less 的用法如下:

less filename

其与 more 不同的是它可以按 y 来往上卷一行，并且可以用"?"来往回搜寻你所要找的单字。

10. chmod
chmod 为变更档案模式用( change mode ) . 这个指令是用来更改档案的存取模式( access mode )。在 UNIX 一个档案上有可读(r)可写(w)可执行(x)三种模式,分别针对该档案的拥有者( onwer )、同群者( group member )( 你可以 ls -lg来观看某一档案的所属的 group )，以及其他人( other )。一个档案如果改成可执行模式则系统就将其视为一个可执行档，而一个目录的可执行模式代表使用者有进入该目录之权利。chmod 就是用来变更一些档案的模式，其使用方式如下:

chmod [ -fR ] mode filename ...

其参数的意义如下:

-f Force. chmod 不会理会失败的动作。
-R Recurive. 会将所有子树下的所有子目录及档案改为你所要改成的模式。

mode 可以为一个三位或四位的八进位数字，来表示对某些对象的存取权。详情可参阅 chmod(1) 的 manual page 中有关 Absolute Modes 的说明。

或是用一个字串来表示，请参考 chmod(1) 的说明。



b. 关於 Process 处理的指令: 

1. ps
ps 是用来显示目前你的 process 或系统 processes 的状况。以下列出比较常用的参数:

其选项说明如下:
-a 列出包括其他 users 的 process 状况。
-u 显示 user - oriented 的 process 状况 。
-x 显示包括没有 terminal 控制的 process 状况 。
-w 使用较宽的显示模式来显示 process 状况 。

我们可以经由 ps 取得目前 processes 的状况，如 pid , running state 等。

2. kill
kill 指令的用途是送一个 signal 给某一个 process 。因为大部份送的都是用来杀掉 process 的 SIGKILL 或 SIGHUP ，因此称为 kill。kill 的用法为:

kill [ -SIGNAL ] pid ...
kill -l

SIGNAL 为一个 singal 的数字，从 0 到 31 ，其中 9 是 SIGKILL ，也就是一般用来杀掉一些无法正常 terminate 的讯号。其馀讯号的用途可参考 sigvec(2)中对 signal 的说明。

你也可以用 kill -l 来察看可代替 signal 号码的数目字。kill 的详细情形请参阅 man kill。

c. 关於字串处理的指令: 

1. echo
echo 是用来显示一字串在终端机上。□ echo -n 则是当显示完之後不会有跳行的动作。


2. grep/fgrep
grep 为一过滤器，它可自一个或多个档案中过滤出具有某个字串的行，或是自标准输入过滤出具有某个字串的行。

fgrep 可将欲过滤的一群字串放在某一个档案中，然後使用 fgrep 将包含有属於这一群字串的行过滤出来。

grep 与 fgrep 的用法如下:

grep [-nv] match_pattern file1 file2 ....
fgrep [-nv] -f pattern_file file1 file2 ....

-n 把所找到的行在行前加上行号列出
-v 把不包含 match_pattern 的行列出match_pattern 所要搜寻的字串
-f 以 pattern_file 存放所要搜寻的字串

d. 网路上查询状况的指令: 

1. man
man 是手册 ( manual ) 的意思。 UNIX 提供线上辅助( on-line help )的功能，
man 就是用来让使用者在使用时查询指令、系统呼叫、标准程式库函式、各种表格等的使用所用的。man 的用法如下:

man [-M path] [[section] title ] .....
man [-M path] -k keyword ...

-M path man 所需要的 manual database 的路径。我们也可以用设定环境变数 MANPATH 的方式来取代 -M 选项。title 这是所要查询的目的物。section 为一个数字表示 manual 的分类，通常 1 代表可执行指令，2 代表系统呼叫( system call ) ，3 代表标准函数，等等。

像下面 man 查询的片段:

SEE ALSO
apropos(1), cat(1V), col(1V), eqn(1), lpr(1), more(1),
nroff(1), refer(1), tbl(1), troff(1), vgrind(1), vtroff(1),
whatis(1), eqnchar(7), man(7), catman(8)

我们如要参考 eqnchar(7) 的资料，则我们就输入 man 7 eqnchar ，便能取得我们所要的辅助讯息。
-k keyword用来将含有这项 keyword 的 title 列出来。

man 在 UNIX 上是一项非常重要的指令，我们在本讲义中所述之用法均仅只是一个大家比较常用的用法以及简单的说明，真正详细的用法与说明还是要请你使用man 来得到。

2. who
who 指令是用来查询目前有那些人在线上。

3. w

w 指令是用来查询目前有那些人在线上，同时显示出那些人目前的工作。

4. ku
ku 可以用来搜寻整个网路上的 user ，不像 w 跟 who 只是针对 local host 的查询. 而且 ku 提供让使用者建立搜寻特定使用者名单的功能。你可以建立一个档案 information-file 以条列的方式存放你的朋友的资料，再建立一个档案hosts-file 来指定搜寻的机器名称。 ku 的指令格式可由 ku -h 得到。

E. 网路指令: 

UNIX 提供网路的连接，使得你可以在各个不同的机器上做一些特殊的事情，如你可以在系上的 iris 图形工作站上做图形的处理，在系上的 Sun 上读 News ，甚至到学校的计中去找别系的同学 talk 。这些工作可以利用 UNIX 的网路指令，在你的位子上连到各个不同的机器上工作。如此一来，即使你在寝室，也能轻易的连至系上或计中来工作，不用像以前的人必须泡在冷冰冰的机房面。

这些网路的指令如下所述:

1. rlogin 与 rsh
rlogin 的意义是 remote login , 也就是经由网路到另外一部机器 login 。
rlogin 的格式是:

rlogin host [ -l username ]

选项 -l username 是当你在远方的机器上的 username 和 local host 不同的时後，必须输入的选项，否则 rlogin 将会假设你在那边的 username 与 localhost 相同，然後在第一次 login 时必然会发生错误。

rsh 是在远方的机器上执行某些指令，而把结果传回 local host 。rsh 的格式如下:

rsh host [ -l username ] [ command ]

如同 rlogin 的参数 -l username , rsh 的 -l username 也是指定 remote host的 username 。而 command 则是要在 remote host 上执行的指令。如果没有指定 command ，则 rsh 会去执行 rlogin ，如同直接执行 rlogin 。

不过 rsh 在执行的时候并不会像一般的 login 程序一样还会问你 password , 而是如果你没有设定 trust table , 则 remote host 将不会接受你的 request 。

rsh 须要在每个可能会做为 remote host 的机器上设定一个档案，称为 .rhosts。这个档案每一行分为两个部份，第一个是允许 login 的 hostname , 第二个部份则是允许 login 的 username 。例如，在 ccsun7.csie.nctu.edu.tw 上头你的username 为 ysjuang , 而你的 home 下面的 .rhost 有以下的一行:

ccsun6.cc.nctu.edu.tw u8217529

则在 ccsun6.cc.nctu.edu.tw 机器上的 user u8217529 就可以用以下的方法来执行 rsh 程式:

% rsh ccsun7.csie.nctu.edu.tw -l ysjuang cat mbox

将 ysjuang 在 ccsun7.csie.nctu.edu.tw 上的 mbox 档案内容显示在 local host ccsun6.cc.nctu.edu.tw 上。

而如果 .rhost 有这样的一行，则 ccsun6.cc.nctu.edu.tw 上的 user u8217529将可以不用输入 password 而直接经由 rsh 或 rlogin login 到ccsun7.csie.nctu.edu.tw 来。

注意:

.rhost 是一个设定可以信任的人 login 的表格，因此如果设定不当将会让不法之徒有可以乘机侵入系统的机会。 如果你阅读 man 5 rhosts ，将会发现你可以在第一栏用 + 来取代任何 hostname ，第二栏用 + 来取代任何username 。

如一般 user 喜欢偷懒利用 " + username " 来代替列一长串 hostname ，但是这样将会使得即使有一台 PC 上跑 UNIX 的 user 有与你相同的username , 也可以得到你的 trust 而侵入你的系统。这样容易造成系统安全上的危险。因此本系禁止使用这样子的方式写你的 .rhost 档，如果发现将予以停机直到你找中心的工作人员将其改正为止。 同理，如果你的第二个栏位为 + ，如" hostname + " ,则你是允许在某一部机器上的"所有"user 可以不用经由输入 password 来进入你的帐号，是壹种更危险的行为。所以请自行小心。

2. telnet
telnet 是一个提供 user 经由网路连到 remote host。
telnet 的 格式如下:

telnet [ hostname | ip-address ] [ port ]

hostname 为一个像 ccsun1 或是 ccsun1.cc.nctu.edu.tw 的 name address，ip-address 则为一个由四个小於 255 的数字组成的 ip address ，如 ccsun1的 ip-address 为 140.113.17.173 ，ccsun1.cc.nctu.edu.tw 的 ip-address为 140.113.4.11 。你可以利用 telnet ccsun1 或 telnet 140.113.17.173 来连到 ccsun1。

port 为一些特殊的程式所提供给外界的沟通点，如资工系的 MUD 其 server 便提供一些 port 让 user 由这些 port 进入 MUD 程式。详情请参阅 telnet(1)的说明。


3. ftp
ftp 的意义是 File Transfer Program ，是一个很常应用在网路档案传输的程式。ftp 的格式如下:

ftp [ hostname | ip-address ]

其中 hostname | ip-address 的意义跟 telnet 中的相同。

在进入 ftp 之後，如果与 remote host 连接上了，它将会询问你 username与密码，如果输入对了就可以开始进行档案传输。

在 ftp 中有许多的命令，详细的使用方式请参考 ftp(1) ，这里仅列出较常用的 cd , lcd , mkdir , put , mput , get , mget , binary , ascii ,
prompt , help 与 quit 的使用方式。

ascii 将传输模式设为 ascii 模式。通常用於传送文字档。

binary 将传输模式设为 binary 模式，通常用於传送执行档，压缩档与影像档等。
cd remote-directory 将 remote host 上的工作目录改变。

lcd [ directory ] 更改 local host 的工作目录。

ls [ remote-directory ] [ local-file ] 列出 remote host 上的档案。

get remote-file [ local-file ] 取得远方的档案。

mget remote-files 可使用通用字元一次取得多个档案。

put local-file [ remote-file] 将 local host 的档案送到 remote host。

mput local-files 可使用通用字元一次将多个档案放到 remote host 上。

help [ command ] 线上辅助指令。

mkdir directory-name 在 remote host 造一个目录。

prompt 更改交谈模式，若为 on 则在 mput 与 mget 时每作一个档案之传输时均会询问。

quit/bye 离开ftp .

利用 ftp ，我们便可以在不同的机器上将所需要的资料做转移，某些特别的机器更存放大量的资料以供各地的使用者抓取，本校较著名的 ftp server有 NCTUCCCA 与系上的 ftp.csie.nctu.edu.tw 。这些 ftp server 均有提供一个 user 称为 anonymous ，一般的"外来客"可以利用这个 username 取得该 server 的公共资料。不过 anonymous 在询问 password 时是要求使用anonymous 的使用者输入其 email address，以往有许多台湾的使用者在使用国外的 ftp server 时并没有按照人家的要求输入其 email address，而仅是随便打一些字串，引起许多 internet user 和管理者的不满，对台湾的使用者的风评变得很差，因此遵循各 ftp server 的使用规则也是一件相当重要的事。


f. 关於通讯用的指令: 

1. write
这个指令是提供使用者传送讯息给另一个使用者，使用方式:
write username [tty]

2. talk/ytalk/cytalk/ctalk
UNIX 专用的交谈程式。会将萤幕分隔开为你的区域和交谈对象的区域，同时也可和不同机器的使用者交谈。使用方式:

talk username[@host] [tty]

3. mesg
选择是否接受他人的 messege , 若为 messege no 则他人的 messege 将无法传送给你，同时他也无法干扰你的工作。使用方法:

mesg [-n|-y]

4. mail/elm
在网路上的 email 程式，可经由此程式将信件 mail 给他人。 使用方式:

mail [username]
mail -f mailboxfile

如有信件，则直接键入 mail 可以读取你的 mail .

elm 提供较 mail 更为方便的介面，而且可做线上的 alias . 你可以进入 elm使用上下左右键来选读取的信件，并可按 h 取得线上的 help 文件。

使用方式:

elm [usernmae]
elm -f mailboxfile

g. 编译器( Compiler ):

Compiler 的用处在於将你所撰写的程式翻译成一个可执行档案。在资工系常用的程式语言是 C , pascal , FORTRAN 等。你可以先写好一个 C 或 Pascal或 FORTRAN 的原始程式档，再用这些 compiler 将其翻成可执行档。你可以用这个方法来制造你自己的特殊指令。

1. cc/gcc (C Compiler)
/usr/bin/cc
/usr/local/bin/gcc

语法: cc [ -o execfile ] source
gcc [ -o execfile ] source

execfile 是你所希望的执行档的名称，如果没有加上 -o 选项编译出来的可执行档会以 a.out 做为档名。 source 为一个以 .c 做为结尾的 C 程式档。请参阅 cc(1) 的说明。

2. pc (Pascal Compiler)
/usr/local/bin/pc

语法: pc [ -o execfile ] source

execfile 是你所希望的执行档的名称，如果没有加上 -o 选项编译出来的可执行档会以 a.out 做为档名。 source 为一个以 .p 做为结尾的 Pascal 程式档。 请参阅 /net/home5/lang/man 中 pc(1) 的说明。

3. f77 (Fortran Compiler)
/net/home5/lang/f77

语法: f77 [ -o execfile ] source

execfile 是你所希望的执行档的名称，如果没有加上 -o 选项编译出来的可执行档会以 a.out 做为档名。 source 为一个以 .p 做为结尾的 FORTRAN 程式档。

h. 有关列印的指令: 
以下为印表所会用到的指令，在本系的印表机有 lp1 , lp2 ( 点矩阵印表机 )，lw , sp , ps , compaq ( 雷射印表机 )，供使用者使用。

1. lpr
lpr 为用来将一个档案印至列表机的指令。

用法:
lpr -P[ printer ] file1 file2 file3 ....

或
lpr -P[ printer ] < file1

例子:
lpr -Plp1 hello.c hello.lst hello.map
lpr -Plp1 < hello.c

前者以参数输入所要印出的档案内容，後者列印标准输入档案( standard input )的内容，因已将 hello.c 转向到标准输入，故会印出 hello.c 的档案内容。

2. lpq
lpq 是用来观察 printer queue 上的 Jobs 。

用法:
lpq -P[ printer ]


3. lprm
lprm 是用来取消列印要求的指令。 通常我们有时会印错，或是误送非文字档资料至 printer , 此时就必须利用 lprm 取消列印 request ，以免造成资源的浪费。

用法:
lprm -P[ printer ] [ Jobs id | username ]

lprm 用来清除 printer queue 中的 Jobs , 如果你使用 Job Id 作为参数，则它将此 Job 自printer queue 清除，如果你用 username作为参数，则它将此 queue中所有 Owner 为此 username 的 Jobs 清除。

i. 更改个人使用资料:

1. passwd
passwd 是用来更改你的使用密码，用法为:

passwd [ username ]

在使用 passwd 的时候，它会先问你的旧密码，然後询问两次要更改的密码，确定无误後才将你的密码改掉。

2. chsh
chsh 是提供使用者更换 login shell 的指令，你可经由此更换自己使用的 shell 。



//////////////////////////////////////////
 1、cd 进入到某个文件路径下

 格式：cd 需要访问的文件夹路径

 1）cd .. 进入用户文件夹位置

 2）cd ~/Desktop 进入桌面位置

2、ls 查看当前目录下的文件夹/文件

格式：ls -l                  参数：-l 详细信息，-a 包括隐藏文件

3、mkdir 新建文件夹   touch  新建文件

格式：mkdir 文件夹名称

            touch 文件名称

4、cp 拷贝文件

cp 参数 源文件 目标路径

参数：

-a：此参数的效果和同时指定"-dpR"参数相同； 

-d：当复制符号连接时，把目标文件或目录也建立为符号连接，并指向与源文件或目录连接的原始文件或目录； 

-f：强行复制文件或目录，不论目标文件或目录是否已存在； 

-i：覆盖既有文件之前先询问用户； 

-l：对源文件建立硬连接，而非复制文件； 

-p：保留源文件或目录的属性； 

-R/r：递归处理，将指定目录下的所有文件与子目录一并处理；

-s：对源文件建立符号连接，而非复制文件； 

-u：使用这项参数后只会在源文件的更改时间较目标文件更新时或是名称相互对应的目标文件并不存在时，才复制文件； 

-S：在备份文件时，用指定的后缀“SUFFIX”代替文件的默认后缀； 

-b：覆盖已存在的文件目标前将目标文件备份； 

-v：详细显示命令执行的操作。

例：cp -R ~/Desktop/folder/test.txt ~/Desktop     把 test.txt 拷贝到左面

5、rm 删除文件    rmdir 删除文件夹

格式：rm 参数 文件

           rmdir 参数 文件夹

参数：

-d：直接把欲删除的目录的硬连接数据删除成0，删除该目录； 

-f：强制删除文件或目录； -i：删除已有文件或目录之前先询问用户； 

-r或-R：递归处理，将指定目录下的所有文件与子目录一并处理； 

--preserve-root：不对根目录进行递归操作； 

-v：显示指令的详细执行过程。

例：rm -rf ~/Desktop/folder/test.txt        删除 test.txt 文件

6、mv 移动文件

mv 源文件 目标路径

例：mv ~/Desktop/folder/test.txt ~/Desktop    把 test.txt 移动到桌面

7、chmod 更改文件权限

格式：chmod 参数 权限 文件

参数：

-c : 若该档案权限确实已经更改，才显示其更改动作

-f : 若该档案权限无法被更改也不要显示错误讯息

-v : 显示权限变更的详细资料

-R : 对目前目录下的所有档案与子目录进行相同的权限变更(即以递回的方式逐个变更)

--help : 显示辅助说明

--version : 显示版本

权限：

r=4，w=2，x=1

若要r-w-x属性则4+2+1=7

若要r-w属性则4+2=6

若要r-x属性则4+1=5

例：chmod -R 777 ~/Desktop/folder/test.txt         给 test.txt 赋予 root 权限

8、man 查看详细的命令帮助

例：man ls          查看 ls 命令的详细帮助。

9、clear 清除屏幕或窗口内容 

10、pwd 显示当前目录的路径名

11、file 显示文件类型

格式：file 文件名

12、ps 显示进程当前状态

格式：ps 参数

-A 显示所有进程（等价于-e）(utility)

-a 显示一个终端的所有进程，除了会话引线

-N 忽略选择。

-d 显示所有进程，但省略所有的会话引线(utility)

-x 显示没有控制终端的进程，同时显示各个命令的具体路径。dx不可合用。（utility）

-p pid 进程使用cpu的时间

-u uid or username 选择有效的用户id或者是用户名

-g gid or groupname 显示组的所有进程。

U username 显示该用户下的所有进程，且显示各个命令的详细路径。如:ps U zhang;(utility)

-f 全部列出，通常和其他选项联用。如：ps -fa or ps -fx and so on.

-l 长格式（有F,wchan,C 等字段）

-j 作业格式

-o 用户自定义格式。

v 以虚拟存储器格式显示

s 以信号格式显示

-m 显示所有的线程

-H 显示进程的层次(和其它的命令合用，如：ps -Ha)（utility）

e 命令之后显示环境（如：ps -d e; ps -a e）(utility)

h 不显示第一行

例：ps aux          查看正在运行进程所占PID、CPU、内存、PID、进程开始时间

13、kill 终止进程

格式：kill 进程号

14、date 显示系统的当前日期和时间

15、telnet 远程登录

格式：telnet 主机地址

16、ping 给一个网络主机发送回应请求

格式：ping 主机地址

17、history 列出最近执行过的 几条命令及编号

18、ifconfig 查看本机 IP 等配置信息

19、unrar 解压 rar           unzip 解压 zip 

格式：unrar e rar文件

            unzip zip文件

20、mv 重命名

格式：mv 旧名称 新名称

例：mv test.txt demo.txt 把名为todaym的txt文件重命名为nie



# VIM
vi/vim 基本使用方法
本文介绍了vi (vim)的基本使用方法，但对于普通用户来说基本上够了！i/vim的区别简单点来说，它们都是多模式编辑器，不同的是vim 是vi的升级版本，它不仅兼容vi的所有指令，而且还有一些新的特性在里面。例如语法加亮，可视化操作不仅可以在终端运行，也可以运行于x window、 mac os、 windows。

vi编辑器是所有Unix及Linux系统下标准的编辑器，它的强大不逊色于任何最新的文本编辑器，这里只是简单地介绍一下它的用法和一小部分指令。由于对Unix及 Linux系统的任何版本，vi编辑器是完全相同的，因此您可以在其他任何介绍vi的地方进一步了解它。Vi也是Linux中最基本的文本编辑器，学会它后，您将在Linux的世界里畅行无阻。

[简单地，可以使用上下左右方向箭头和delete，backspace键来进行位置移动和删除，不管是命令模式还是插入模式]

1、vi的基本概念
基本上vi可以分为三种状态，分别是命令模式（command mode）、插入模式（Insert mode）和底行模式（last line mode），各模式的功能区分如下：
1) 命令行模式command mode）
控制屏幕光标的移动，字符、字或行的删除，移动复制某区段及进入Insert mode下，或者到 last line mode。
2) 插入模式（Insert mode）
只有在Insert mode下，才可以做文字输入，按「ESC」键可回到命令行模式。
3) 底行模式（last line mode）
将文件保存或退出vi，也可以设置编辑环境，如寻找字符串、列出行号……等。

不过一般我们在使用时把vi简化成两个模式，就是将底行模式（last line mode）也算入命令行模式command mode）。

2、vi的基本操作
a) 进入vi
在系统提示符号输入vi及文件名称后，就进入vi全屏幕编辑画面：$ vi myfile。不过有一点要特别注意，就是您进入vi之后，是处于「命令行模式（command mode）」，您要切换到「插入模式（Insert mode）」才能够输入文字。初次使用vi的人都会想先用上下左右键移动光标，结果电脑一直哔哔叫，把自己气个半死，所以进入vi后，先不要乱动，转换到「插入模式（Insert mode）」再说吧！

b) 切换至插入模式（Insert mode）编辑文件
在「命令行模式（command mode）」下按一下字母「i」就可以进入「插入模式（Insert mode）」，这时候你就可以开始输入文字了。

c) Insert 的切换
您目前处于「插入模式（Insert mode）」，您就只能一直输入文字，如果您发现输错了字！想用光标键往回移动，将该字删除，就要先按一下「ESC」键转到「命令行模式（command mode）」再删除文字。

d) 退出vi及保存文件
在「命令行模式（command mode）」下，按一下「：」冒号键进入「Last line mode」，例如：
: w filename （输入 「w filename」将文章以指定的文件名filename保存）
: wq (输入「wq」，存盘并退出vi)
: q! (输入q!， 不存盘强制退出vi)

3、命令行模式（command mode）功能键
1）. 插入模式
按「i」切换进入插入模式「insert mode」，按“i”进入插入模式后是从光标当前位置开始输入文件；
按「a」进入插入模式后，是从目前光标所在位置的下一个位置开始输入文字；
按「o」进入插入模式后，是插入新的一行，从行首开始输入文字。

2）. 从插入模式切换为命令行模式
按「ESC」键。

3）. 移动光标
vi可以直接用键盘上的光标来上下左右移动，但正规的vi是用小写英文字母「h」、「j」、「k」、「l」，分别控制光标左、下、上、右移一格。
按「ctrl」+「b」：屏幕往“后”移动一页。
按「ctrl」+「f」：屏幕往“前”移动一页。
按「ctrl」+「u」：屏幕往“后”移动半页。
按「ctrl」+「d」：屏幕往“前”移动半页。
按数字「0」：移到文章的开头。
按「G」：移动到文章的最后。
按「$」：移动到光标所在行的“行尾”。
按「^」：移动到光标所在行的“行首”
按「w」：光标跳到下个字的开头
按「e」：光标跳到下个字的字尾
按「b」：光标回到上个字的开头
按「#l」：光标移到该行的第#个位置，如：5l,56l。

4）. 删除文字
「x」：每按一次，删除光标所在位置的“后面”一个字符。
「#x」：例如，「6x」表示删除光标所在位置的“后面”6个字符。
「X」：大写的X，每按一次，删除光标所在位置的“前面”一个字符。
「#X」：例如，「20X」表示删除光标所在位置的“前面”20个字符。
「dd」：删除光标所在行。
「#dd」：从光标所在行开始删除#行

5）. 复制
「yw」：将光标所在之处到字尾的字符复制到缓冲区中。
「#yw」：复制#个字到缓冲区
「yy」：复制光标所在行到缓冲区。
「#yy」：例如，「6yy」表示拷贝从光标所在的该行“往下数”6行文字。
「p」：将缓冲区内的字符贴到光标所在位置。注意：所有与“y”有关的复制命令都必须与“p”配合才能完成复制与粘贴功能。

6）. 替换
「r」：替换光标所在处的字符。
「R」：替换光标所到之处的字符，直到按下「ESC」键为止。

7）. 回复上一次操作
「u」：如果您误执行一个命令，可以马上按下「u」，回到上一个操作。按多次“u”可以执行多次回复。

8）. 更改
「cw」：更改光标所在处的字到字尾处
「c#w」：例如，「c3w」表示更改3个字

9）. 跳至指定的行
「ctrl」+「g」列出光标所在行的行号。
「#G」：例如，「15G」，表示移动光标至文章的第15行行首。

4、Last line mode下命令简介
　　在使用「last line mode」之前，请记住先按「ESC」键确定您已经处于「command mode」下后，再按「：」冒号即可进入「last line mode」。

A) 列出行号
「set nu」：输入「set nu」后，会在文件中的每一行前面列出行号。

B) 跳到文件中的某一行
「#」：「#」号表示一个数字，在冒号后输入一个数字，再按回车键就会跳到该行了，如输入数字15，再回车，就会跳到文章的第15行。

C) 查找字符
「/关键字」：先按「/」键，再输入您想寻找的字符，如果第一次找的关键字不是您想要的，可以一直按「n」会往后寻找到您要的关键字为止。
「?关键字」：先按「?」键，再输入您想寻找的字符，如果第一次找的关键字不是您想要的，可以一直按「n」会往前寻找到您要的关键字为止。

D) 保存文件
「w」：在冒号输入字母「w」就可以将文件保存起来。

E) 离开vi
「q」：按「q」就是退出，如果无法离开vi，可以在「q」后跟一个「!」强制离开vi。
「qw」：一般建议离开时，搭配「w」一起使用，这样在退出的时候还可以保存文件。

5、vi命令列表
1) 下表列出命令模式下的一些键的功能：

h左移光标一个字符
l右移光标一个字符
k光标上移一行
j光标下移一行
^光标移动至行首
0数字“0”，光标移至文章的开头
G光标移至文章的最后
$光标移动至行尾
Ctrl+f向前翻屏
Ctrl+b向后翻屏
Ctrl+d向前翻半屏
Ctrl+u向后翻半屏
i在光标位置前插入字符
a在光标所在位置的后一个字符开始增加
o插入新的一行，从行首开始输入
ESC从输入状态退至命令状态
x删除光标后面的字符
#x删除光标后的＃个字符
X(大写X)，删除光标前面的字符
#X删除光标前面的#个字符
dd删除光标所在的行
#dd删除从光标所在行数的#行
yw复制光标所在位置的一个字
#yw复制光标所在位置的#个字
yy复制光标所在位置的一行
#yy复制从光标所在行数的#行
p粘贴
u取消操作
cw更改光标所在位置的一个字
#cw更改光标所在位置的#个字


2) 下表列出行命令模式下的一些指令
w filename储存正在编辑的文件为filename
wq filename储存正在编辑的文件为filename，并退出vi
q!放弃所有修改，退出vi
set nu显示行号
/或?查找，在/后输入要查找的内容
n与/或?一起使用，如果查找的内容不是想要找的关键字，按n或向后（与/联用）或向前（与?联用）继续查找，直到找到为止。
![](https://images.cnblogs.com/cnblogs_com/itech/192594/vim.jpg)
