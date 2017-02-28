# <span class="fa fa-hashtag" aria-hidden="true"></span> 脚本命令:Linux Bash

<ol class="breadcrumb"><li><a href="/">Home</a></li><li><a href="/operation/shell/overview.md">Shell</a></li><li class="active">Linux Bash</li></ol>

## 文件操作
* 更改当前目录 `cd`
* 获取当前目录 `pwd`
* 删除文件/目录 `rm -f` or `rm -rf` or `rmdir`
* 创建文件 `touch` or `cat > xxx`
* 创建临时文件 `mktemp testing.XXXXXX`, 文件名末尾加6个X
* 创建临时目录 `mktemp -d dir.XXXXXX`, 目录名末尾加6个X
* 创建目录 `mkdir`
* 移动文件/文件重命名 `mv`
* 复制 `cp`
* 硬链接/软链接 `ln` or `ln -s`
* 显示文件列表 `ls`
* 实际搜索硬盘查询文件名称 `find`
* 别名 `alias`
* 查看文件所在路径 `dirname`
* 查看文件名(过滤路径) `basename`
* 查看可执行文件的位置 `which`
* 查看文件的位置 `whereis`
* 配合数据库查看文件位置 `locate`

## 文件查看
* 文件内容查看 `cat`
* 按页查看文件内容 `more` or `less`
* 查看文件前几行 `head`
* 查看文件后几行 `tail`
* 查看文件统计信息 `stat`
* 查看文件类型 `file`

## 文本编辑
* 字符流编辑器 `sed`
* 模式匹配的程序设计语言 `awk` and `gawk`
* 行编辑器 `ed`
* 排序 `sort`
* 编辑工具 `vim` or `emacs`

## 查询/统计
* 统计文件中数量 `wc -c` or `wc -l` or `wc -w`
* 计算行号 `nl`
* 搜索数据 `grep`

## 文件权限
* 系统用户 `cat /etc/passwd` or `cat /etc/shadow`
* 添加用户 `useradd`
* 删除用户 `userdel`
* 修改用户 `usermod` or `chsh` or `chfn` or `chage`
* 修改密码 `passwd` or `chpasswd`
* 系统用户组 `cat /etc/group`
* 添加用户组 `groupadd`
* 删除用户组 `groupdel`
* 添加用户到用户组 `usermod`
* 修改用户组 `groupmod`
* 设置创建文件默认权限 `umask`
* 修改权限 `chmod`
* 修改所属关系 `chown` or `chgrp`
* 执行root命令 `sudo`
* 显示用户id和所属组信息 `id`

## 压缩/归档
* 归档 `tar`
* zip压缩 `zip` or `unzip` or `zipcloak` or `zipnote` or `zipsplit`
* bzip2压缩 `bzip2` or `bunzip2` or `bzcat`
* gzip压缩 `gzip` or `gunzip` or `gzcat`

```bash
# 仅打包，不压缩
tar -cvf /usr/local/test.tar /usr/local/test
# 解包
tar –xvf test.tar

# 打包后，用bzip2压缩
tar -jcvf /usr/local/test.tar.bz2 /usr/local/test
# 解压bzip2包
tar -jxvf /usr/local/test.tar.bz2

# 打包后，用gzip压缩
tar -zcvf /usr/local/test.tar.gz /usr/local/test
# 解压gzip包
tar -zxvf /usr/local/test.tar.gz
```

## 程序安装
* Debian & Ubuntu `apt-get`
* Redhat & CentOS `yum` or `rpm`
* 查询rpm包是否安装 `rpm -q xxx`
* 列出所有被安装的rpm包 `rpm -qa`
* 安装RPM包 `rpm -ivh xxx`
* 查看yum安装后，机器里都装了哪些东西 `rpm -ql xxx`
* 手动安装 `./configure` then `make -j & make install`
* 系统服务 `chkconfig`

```bash
# 列出所有服务
chkconfig --list
# 增加httpd服务
chkconfig --add httpd
# 删除httpd服务
chkconfig --del httpd
```
* 创建、删除、修复、软连接，还能显示出已存在软连接的信息 `update-alternatives`

```bash
# 列出系统中所有安装java程序的路径，并选择默认程序
update-alternatives --config java
```

## 后台运行
* 控制台下后台模式运行脚本 `command &`
* 非控制台下后台模式运行脚本 `nohup command &`
* 查看shell当前处理的作业 `jobs`
* 重启停止的作业 `bg`
* 计划执行作业 `at [-f filename] time`
* 列出等待的作业 `atq`
* 删除作业 `atrm`
* 调整命令的调度优先级 `nice` and `renice`
* 计划定期执行脚本 `cron min hour dayofmonth month dayofweek command`
* 列出当前用户所有cron时间表 `crontab -l`
* 列出cron目录 `ls /etc/cron.*ly`
* 运行服务器问题错过的的计划 `anacron`
* 后台新窗口 `screen`
* 创建新shell后台执行，完成后退出 `sh -c "cd /home; ls"`

## 系统监控
* 虚拟内存 `cat /proc/meminfo`
* 共享内存 `ipcs -m`
* 系统进程 `ps aux` or `ps -ef`
* 实时监测进程 `top`
* 结束进程 `kill` or `killall`
* 挂载媒体 `mount` or `umount`
* 查看磁盘使用情况 `df` or `du`
* 查看登录用户 `who`
* 查看所有进程和登陆用户 `lsof`
* 捕捉信息 `trap`
* 打印确切的系统信息 `uname -a`
* 打印操作系统信息 `cat /etc/redhat-release`

## 日期/时间
* 当前时间 `date`
* 休息暂停 `sleep`
* 打印出一条命令或一个程序的执行时间 `time`

## 打印/输出
* 打印 `printf` or `echo`
* 输出重定向(覆盖) `>`
* 输出重定向(底部追加) `>>`
* 输入重定向 `<`
* 内联输入重定向 `<<`
* 管道 `|`
* 标准键盘输入 `read`
* 退出状态码 `echo $?`
* shell脚本结束设置退出状态码 `exit return_number`
* 命令行参数数量 `echo $#`
* 命令行最后一个参数 `echo ${!#}`
* 命令行所有参数 `$*` or `$@`
* 命令行参数位移 `shift`

```bash
# ./testing -a -b test1 -d
# Found the -a option
# Found the -b option. with parameter value test1
# -d is not an option
# extracting command line options and values

while [ -n "$1" ]
do
    case "$1" in
    -a) echo "Found the -a option";;
    -b) param="$2"
        echo "Found the -b option, with parameter value $param"
        shirt 2;;
    -c) echo "Found the -c option";;
    --) shift
        break;
    *) echo "$1 is not an option";;
    esac
    shift
done

count=1
for param in "$@"
do
    echo "Parameter #$count: $param"
    count=$[ $count + 1 ]
done
```
* 命令行参数分析 `getopt`
* 结果输出到和标准错误一样 `command >&2`
* 重定向错误和数据 `return_number>`, 重定向所有输出 `&>`

```bash
# 文件或路径不存在的返回码是2
ls -al badfile 2> testfile
cat testfile
# ls: cannot access badfile: No such file or directory

ls -al test test2 test3 badtest 2> testfile 1> testfile2
cat testfile
# ls: cannot access test: No such file or directory
# ls: cannot access badtest: No such file or directory
cat testfile2
# -rw-rw-r--.   1 rich rich 158 2010-10-16 11:32 test2
# -rw-rw-r--.   1 rich rich   0 2010-10-16 11:33 test3
```
* 永久重定向 `exec return_number>` or `exec return_number<`
* 阻止命令输出 `command > /dev/null`
* 清空文件 `cat /dev/null > filename`
* 记录消息到日志文件 `tee filename`

```bash
date | tee testfile
# Sun Oct 17 18:56:21 EDT 2010
```
* 清屏 `clear`
* 创建脚本菜单 `select`

```bash
# smenu1
PS3="Enter option: "
select option in "Display disk space" "Display logged on users" "Display memory usage" "Exit program"
do
    case $option in
    "Exit program")
        break ;;
    "Display disk space")
        df -k ;;
    "Display logged on users")
        who ;;
    "Display memory usage")
        cat /proc/meminfo ;;
    *)
        clear
        echo "Sorry, wrong selection" ;;
    esac
done
clear
# ./smenu1
# 1) Display disk space       3) Display memory usage
# 2) Display logged on users  4) Exit program
# Enter option: 
```

## 数学运算
* 数学表达式 `expr xxx`
* 方括号数学表达式 `$[ xxx ]`
* bash计算器 `bc`

```bash
# 2个变量相除，结果为4位小数
var1=100
var2=45
var3=`echo "scale=4; $var1 / $var2" | bc`
echo The answer for this is $var3
# The answer for this is 2.2222
```

## 运算符
* 测试条件并返回退出状态码(常用在if里) `test condition` or `[ condition ]`
* 双尖括号(针对数学表达式, 常用在if里) `(( expression ))`
* 双方括号(针对字符串比较, 常用在if里) `[[ expression ]]`
* 数组 `( )`

```bash
# 数组遍历
array_name=(value0 value1 value2 value3 value4)
for value in ${array_name[@]}; do
    echo value
done
```

## 网络通信
* 输出邮件发送 `mail`
* 输出网络接口配置 `ifconfig` or `ip addr`
* 显示网络接口信息 `netstat` or `ss`
* 文件下载 `wget`
* http请求 `curl`, 此命令也包含文件下载功能
* 验证服务器是否连通 `ping`
* 跟踪网络访问路由 `tracepath` or `traceroute`
* 结合`ping`和`tracepath`功能的工具 `mtr`
* DNS查询 `host`
* 查询指定站点的whois记录 `whois`
* 网线是否插到在网络接口上 `ifplugstatus`
* 网卡禁用和开启 `ifdown` and `ifup`
* 释放IP地址并从DHCP服务器上获得一个新的 `dhclient -r`

```bash
## 常用ss命令
ss -l #显示本地打开的所有端口
ss -pl #显示每个进程具体打开的socket
ss -t -a #显示所有tcp socket
ss -u -a #显示所有的UDP Socekt
ss -o state established '( dport = :smtp or sport = :smtp )' #显示所有已建立的SMTP连接
ss -o state established '( dport = :http or sport = :http )' #显示所有已建立的HTTP连接
ss -x src /tmp/.X11-unix/* #找出所有连接X服务器的进程
ss -s #列出当前socket详细信息
```

## 结构化命令
* 条件判断 `if-then-else`

```bash
if command1
then
    commands
elif command2
then
    more commands
else
    more commands
fi
# or
if command1; then
    commands
elif command2; then
    more commands
else
    more commands
fi
```
* 条件分支 `case`

```bash
case variable in
pattern1 | pattern2)
    commands1;;
pattern3)
    commands2;;
*)
    default commands;;
esac
```
* 循环 `for`

```bash
for var in list
do
    commands
done
# or
for var in list; do
    commands
done
# or
for (( variable assignment ; condition ; iteration process )); do
    commands
done
```
* 循环 `while`

```bash
while test command
do
    commands
done
# or
while test command; do
    commands
done
# or 读取文件
while read line; do
    echo "$line"
done
```
* 循环 `until` 与`while`条件判断刚好相反，command返回非0才执行commands

```bash
until test command
do
    commands
done
# or
until test command; do
    commands
done
```
* 控制循环 `break` and `continue`

## 函数
* 基本脚本函数

```bash
function name {
    commands
}
# or
name() {
    commands
}
```
* 退出函数并返回退出状态码 `return`，范围0~255
* 函数返回真实数据

```bash
function db1 {
    read -p "Enter a value: " value
    echo $[ $value * 2 ]
}
result=`db1`
echo "The new value is $result"
```
* 函数参数 `func value1 value2`
* 函数内局部变量 `local`
* 脚本中调用另一个脚本 `. ./myfuncs`

## 环境变量
* 显示全局环境变量 `printenv`
* 显示环境变量(局部+全局) `set`
* 设置全局环境变量 `export xxx`
* 删除环境变量 `unset xxx`

## 附录:默认shell环境变量
|变量|描述|
|-------|-------|
|CDPATH|冒号分隔的目录列表，作为cd命令的搜索路径|
|HOME|当前用户的主目录|
|IFS|shell用来分隔文本字符串的一列字符|
|MAIL|当前用户收件箱的文件名；bash shell会检查这个文件来看有没有新邮件|
|MAILPATH|冒号分隔的当前用户收件箱的文件名列表；bash shell会检查列表中的每个文件来看有没有新邮件|
|OPTARG|getopts命令处理的最后一个选项参数值|
|OPTIND|getopts命令处理的最后一个选项参数的索引号|
|PATH|冒号分隔的shell查找命令的目录列表|
|PS1|shell命令行界面的主提示符|
|PS2|shell命令行界面的次提示符|

## 附录:Linux本地开机文件位置
|发行版|文件位置|
|:------:|------|
|debian|/etc/init.d/rc.local|
|Fedora|/etc/rc.d/rc.local|
|Mandriva|/etc/rc.local|
|openSuse|/etc/init.d/boot.local|
|Ubuntu|/etc/rc.local|

## 附录:登录shell文件处理顺序
|编号|交互式login shell|交互式non-login shell|
|------|------|------|
|1) 系统全局环境变量|/etc/profile|/etc/bashrc|
|2) 私有环境变量|$HOME/.bash_profile|-|
|3) 私有环境变量|$HOME/.bash_login|-|
|4) 私有环境变量|$HOME/.profile|$HOME/.bashrc|

## 附录:expr命令操作符
|操作符|描述|
|-------|-------|
|ARG1 &#124; ARG2|如果没有参数是null或零值，返回ARG1；否则返回ARG2|
|ARG1 & ARG2|如果没有参数是null或零值，返回ARG1；否则返回0|
|ARG1 < ARG2|如果ARG1小于ARG2，返回1；否则返回0|
|ARG1 <= ARG2|如果ARG1小于或等于ARG2，返回1；否则返回0|
|ARG1 = ARG2|如果ARG1等于ARG2，返回1；否则返回0|
|ARG1 != ARG2|如果ARG1不等于ARG2，返回1；否则返回0|
|ARG1 >= ARG2|如果ARG1大于或等于ARG2，返回1；否则返回0|
|ARG1 > ARG2|如果ARG1大于ARG2，返回1；否则返回0|
|ARG1 + ARG2|返回ARG1和ARG2的算术运算和|
|ARG1 - ARG2|返回ARG1和ARG2的算术运算差|
|ARG1 * ARG2|返回ARG1和ARG2的算术运算乘积|
|ARG1 / ARG2|返回ARG1被ARG2除的运算商|
|ARG1 % ARG2|返回ARG1被ARG2除的算术余数|
|STRING : REGEXP|如果REGEXP匹配到了STRING中的某个模式，返回该模式匹配|
|match STRING REGEXP|如果REGEXP匹配到了STRING中的某个模式，返回该模式匹配|
|substr STRING POS LENGTH|返回起始位置为POS(从1开始计数)、长度为LENGTH个字符的子字符串|
|index STRING CHARS|返回在STRING中找到CHARS字符串的位置；否则，返回0|
|length STRING|返回字符串STRING的数值长度|
|+ TOKEN|将TOKEN解释成字符串，即使是个关键字|
|(EXPRESSION))|返回EXPRESSION的值|

## 附录:Linux退出状态码
|状态码|描述|
|:------:|------|
|0|命令成功结束|
|1|通用未知错误|
|2|误用shell命令|
|126|命令不可执行|
|127|没找到命令|
|128|无效退出参数|
|128+x|Linux信号x的严重错误|
|130|命令通过Ctrl+C终止|
|255|退出状态码越界|

## 附录:test命令的数值比较功能
|比较|描述|
|-------|-------|
|n1 -eq n2|检查n1是否与n2相等|
|n1 -ge n2|检查n1是否大于或等于n2|
|n1 -gt n2|检查n1是否大于n2|
|n1 -le n2|检查n1是否小于或等于n2|
|n1 -lt n2|检查n1是否小于n2|
|n1 -ne n2|检查n1是否不等于n2|

## 附录:test命令的字符串比较功能
|比较|描述|
|-------|-------|
|str1 = str2|检查str1是否和str2相同|
|str1 != str2|检查str1是否和str2不同|
|str1 < str2|检查str1是否比str2小|
|str1 > str2|检查str1是否比str2大|
|-n str1|检查str1的长度是否非0|
|-z str1|检查str1的长度是否为0|

## 附录:test命令的文件比较功能
|比较|描述|
|-------|-------|
|-d file|检查file是否存在并是一个目录|
|-e file|检查file是否存在|
|-f file|检查file是否存在并是一个文件|
|-r file|检查file是否存在并可读|
|-s file|检查file是否存在并非空|
|-w file|检查file是否存在并可写|
|-x file|检查file是否存在并可执行|
|-O file|检查file是否存在并并属当前用户所有|
|-G file|检查file是否存在并且默认组与当前用户相同|
|file1 -nt file2|检查file1是否比file2新|
|file1 -ot file2|检查file1是否比file2旧|

## 附录:通用的Linux命令选项
|选项|描述|
|-------|-------|
|-a|显示所有对象|
|-c|生成一个计数|
|-d|指定一个目录|
|-e|扩展一个对象|
|-f|指定读入数据的文件|
|-h|显示命令的帮助信息|
|-i|忽略文本大小写|
|-l|产生输出的长格式版本|
|-n|使用非交互模式(批量)|
|-o|指定将所有输出重定向到输出文件|
|-q|以安静模式运行|
|-r|递归地处理目录和文件|
|-s|以安静模式运行|
|-v|生成详细输出|
|-x|排除某个对象|
|-y|对所有问题回答yes|

## 附录:Linux信号
|信号|值|描述|
|:------:|:------:|------|
|1|SIGHUP|挂起进程|
|2|SIGINT|终止进程|
|3|SIGQUIT|停止进程|
|9|SIGKILL|无条件终止进程|
|15|SIGTERM|可能的话终止进程|
|17|SIGSTOP|无条件停止进程，但不是终止进程|
|18|SIGTSTP|停止或者暂停进程，但不终止进程|
|19|SIGCONT|继续运行停止的进程|

