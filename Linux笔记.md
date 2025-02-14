### FinalShell中的快照功能

FinalShell是一款功能强大的SSH客户端软件，它提供了方便的快照功能，用于备份和恢复Linux系统的状态、文件和数据。

### 上传文件到Linux系统

要将文件上传到Linux系统，可以按照以下步骤进行：

1. 找到本地计算机上需要上传的文件。
2. 打开FinalShell，并连接到目标Linux系统。
3. 在FinalShell窗口中，找到目标Linux系统的目录，可以使用`cd`命令切换目录。
4. 将本地文件拖拽到FinalShell窗口中的Linux系统目录中，文件将自动上传到相应目录。

### 下载文件从Linux系统

要从Linux系统下载文件，可以按照以下步骤进行：

1. 在FinalShell中连接到目标Linux系统。
2. 使用`ls`命令查看目标Linux系统中的文件列表，找到需要下载的文件名。
3. 在FinalShell窗口中选中需要下载的文件。
4. 点击下载按钮，文件将保存到本地计算机的桌面或指定的目录中。

### 快照的用途

快照功能可以记录Linux系统的状态、配置和文件信息，用于备份或恢复系统、文件和数据。通过创建快照，您可以在未来的某个时间点还原系统到该快照的状态。

快照的用途包括但不限于以下几点：

1. 系统备份与恢复：创建系统快照可以备份整个系统的状态，以便在系统崩溃或遭受攻击时快速恢复到备份状态。

2. 文件备份与恢复：通过快照功能可以备份重要的文件和数据，以防止数据丢失或损坏，并在需要时恢复到指定时间点的状态。

3. 系统配置更新：在更新系统配置或进行软件安装前，可以先创建一个快照，以备份当前系统的状态，以防更新或安装过程中出现问题。

4. 软件测试与调试：在进行软件测试和调试时，可以创建一个快照，方便在测试过程中回滚到初始状态。

5. 环境复制与部署：如果有多台相似的Linux系统环境需要部署，可以创建一个标准的快照，并在其他系统中恢复该快照，从而快速部署相同的环境。

总而言之，快照功能在系统维护和故障恢复中是非常有用的工具，可以确保系统的稳定性和数据的安全性，同时也方便了系统管理员在操作过程中的备份和恢复操作。

### 文件和目录操作

1. `cd`: 切换目录
   - `cd /path/to/directory`: 切换到指定目录
   - `cd ..`: 返回上一级目录
   - `cd ~`: 切换到用户主目录

2. `pwd`: 显示当前所在路径
   - `pwd`: 显示当前所在路径

3. `ls`: 查看文件和目录
   - `ls`: 查看当前目录的文件和目录
   - `ls /path/to/directory`: 查看指定目录的文件和目录
   - `ls -l`: 以列表形式显示文件和目录的详细信息
   - `ls -a`: 显示所有文件和目录，包括隐藏文件
   - `ls -h`: 以程序员可读的格式显示文件大小

4. `touch`: 创建文件
   - `touch test.txt`: 创建一个名为test.txt的文件

5. `cp`: 复制文件
   - `cp test.txt Develop/`: 将test.txt复制到Develop目录下

6. `mv`: 移动或重命名文件
   - `mv test.txt Develop/test_1.txt`: 将test.txt移动到Develop目录下并重命名为test_1.txt

7. `rm`: 删除文件或目录
   - `rm test.txt`: 删除文件test.txt
   - `rm -r test/`: 删除目录test及其内容

### 文件内容查看和编辑

1. `cat`: 查看文件内容
   - `cat test.txt`: 查看文件test.txt的内容
2. `less`: 分页查看文件内容
   - `less test.txt`: 逐页查看test.txt的内容
3. `nano`: 使用文本编辑器编辑文件
   - `nano test.txt`: 使用nano编辑文件test.txt

### 系统信息查看

1. `uname`: 显示系统信息
   - `uname -a`: 显示所有系统信息

2. `df`: 查看磁盘使用情况
   - `df -h`: 查看磁盘使用情况并以人类可读格式显示

3. `free`: 查看内存使用情况
   - `free -h`: 查看内存使用情况并以人类可读格式显示

### 网络命令

1. `ping`: 测试网络连接
   - `ping www.baidu.com`: 测试与百度的网络连接

2. `ifconfig`: 查看网络接口信息
   - `ifconfig`: 查看网络接口信息

3. `wget`: 下载文件
   - `wget [-b] URL`: 从指定的URL中下载文件，-b选项表示切换到后台下载，可以使用`tail -f`命令查看下载进度

4. `curl`: 发送网络请求
   - `curl URL`: 发送网络请求并打印响应结果

### 端口和进程

1. 端口
   - 端口是计算机和外部交互的出入口，可以分为公认端口、注册端口和动态端口。
   - 查看端口占用情况：`netstat -tuln`或`ss -tuln`

2. 进程
   - 查看进程信息：`ps -ef`
   - 结束进程：`kill 进程号`

### 压缩和解压缩命令

1. `tar`命令压缩
   - 压缩文件到tar归档文件：`tar -cvf test.tar 1.txt 2.txt 3.txt`
   - 使用gzip模式压缩文件到tar.gz归档文件：`tar -zcvf test.tar.gz 1.txt 2.txt 3.txt`

2. `tar`解压
   - 解压tar归档文件到当前目录：`tar -xvf test.tar`
   - 解压tar归档文件到指定目录：`tar -xvf test.tar -C /home/liangyang`
   - 使用gzip模式解压tar.gz归档文件到指定目录：`tar -zxvf test.tar.gz -C /home/liangyang`

3. `zip`命令压缩
   - 压缩文件到zip压缩包：`zip test.zip a.txt b.txt c.txt`
   - 压缩包含文件夹的压缩包：`zip -r test.zip test liangyang a.txt`

4. `unzip`命令解压
   - 解压zip压缩包到当前目录：`unzip test.zip`
   - 解压zip压缩包到指定目录：`unzip test.zip -d /home/liangyang`

### 环境变量

1. `env`: 查看环境变量信息
   - `env`: 查看所有环境变量信息

2. `export`: 设置临时环境变量
   - `export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64`: 设置临时环境变量JAVA_HOME

3. `echo`: 输出环境变量的值
   - `echo $JAVA_HOME`: 输出环境变量JAVA_HOME的值

### 管理进程命令

1. `ps`: 查看进程信息
   - `ps -ef`: 查看所有进程的详细信息

2. `kill`: 结束进程
   - `kill [-9] 进程号`: 结束指定进程，-9选项表示强制结束进程

3. `top`: 实时查看系统资源使用情况
   - `top`: 实时查看系统资源使用情况，按`q`退出

4. `htop`: 类似于top的任务管理器，需要先安装：`sudo apt install htop`

### 网络情况相关命令

1. `sar`: 查看系统

性能数据，包括网络情况
   - `sar`: 查看系统性能数据，包括网络情况

### Vim命令

Vim是一种文本编辑器，具有多种模式，包括普通模式、插入模式和底线命令模式。以下是Vim的基本使用命令：

- 进入Vim并打开文件：`vim 文件名`
- 普通模式下的快捷键：
  - 按`i`、`I`、`a`、`A`、`o`或`O`进入插入模式，在插入模式下可以输入文本内容。
  - 使用`h`、`j`、`k`、`l`移动光标。
  - 按`dd`删除当前行，按`yy`复制当前行，按`p`粘贴复制的内容，按`u`撤销修改，按`Ctrl + r`反向撤销修改。
  - 按`:`进入底线命令模式，可以进行保存、退出等操作。

### 用户和用户组管理命令

1. `su - [用户名]`: 切换用户的命令，带上横线会切换到目标用户的环境变量。
2. `groupadd [用户名]`: 创建一个新用户组。
3. `groupdel [用户名]`: 删除一个用户组。
4. `groupmod -n [用户名] [新用户组名]`: 重命名一个用户组。
5. `useradd [用户名]`: 创建一个新用户。
6. `userdel [-r] [用户名]`: 删除一个用户。`-r`为可选项，加上会删除用户的文件路径，不加只会删除用户对应的文件路径会保留。
7. `usermod -c [用户名] -g [用户组名] -d [文件路径] -s [文件路径]`: 创建一个属于指定用户组的用户，可以修改用户的相关信息。
8. `passwd`: 修改密码。

### 文件和目录权限管理

1. `chmod`命令：用于修改文件、文件夹的权限细节。
   - 语法：`chmod [-R] 权限 文件或文件夹`
   - 权限的数字序号：r表示4，w表示2，x表示1。rwx相互组合可以得到0到7的八进制权限组合，7表示rwx，5表示r-x，2表示-wx。
   - `-R`：对文件夹内的全部内容应用同样规则。

2. 更改文件和文件夹的所属用户、用户组
   - `chown`命令：用于修改文件、文件夹的所属用户、用户组。
   - 语法：`chown [-R] [用户]:[用户组] 文件或文件夹`
   - 冒号用于分隔用户和用户组。若不写用户和用户组，则默认不更改。
   - `-R`：对文件夹内的所有文件进行修改，不加`-R`只有文件本身被修改，文件内所属的文件夹没有被修改。

### 常用快捷键

- `CTRL + C`: 强制退出当前运行的程序。
- `CTRL + D`: 退出当前用户的登录会话。
- `CTRL + r`: 搜索历史命令。
- `CTRL + a | d`: 跳转至命令开头或者结尾。
- `CTRL + 左 | 右`: 跳过左边或者右边的单词。
- `CTRL + l`: 清屏。

### 历史命令和软件安装

- `history`命令：查看历史命令。
- `clear`命令：清屏。
- `!`命令前缀：用于匹配上一次使用的命令。

### 软件安装

- 在CentOS 7中使用`yum`命令联网安装软件，需要root用户执行或者使用`sudo`命令。
  - `yum [-y] [install | remove | search] 软件名`: 安装、卸载、搜索软件。

- 在Ubuntu中使用`apt`命令联网安装软件，同样需要root用户执行或者使用`sudo`命令。
  - `apt [-y] [install | remove | search] 软件名`: 安装、卸载、搜索软件。

### 使用`systemctl`控制服务

- `systemctl [start|stop|status|enable|disable] 服务名`
  - `start`: 启动指定的服务。
  - `stop`: 停止指定的服务。
  - `status`: 查看指定的服务状态。
  - `enable`: 设置指定的服务开机自启动。
  - `disable`: 关闭指定的服务开机自启动。

### 软连接

软连接是一种指向其他文件或文件夹的链接，类似于Windows的快捷方式。

- `ln -s 参数一 参数二`: 创建软连接。
  - `-s`: 创建软连接的参数。
  - `参数一`: 被链接的文件路径或文件夹路径。
  - `参数二`: 链接到的文件路径。

### `date`命令

`date`命令用于查看时间日期，并可以按指定格式显示日期。

语法：`date [-d] [+格式化字符串]`
- `%Y`: 年份。
- `%y`: 年份后两位数字。
- `%m`: 月份。
- `%d`: 日。
- `%H`: 小时。
- `%M`: 分钟。
- `%S`: 秒。
- `%s`: 时间戳。

### 修改Linux时区

- `rm -f /etc/localtime`: 删除当前的时区软连接。
- `sudo ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime`: 创建指向上海时区的软连接。

### IP地址和域名解析

- IP地址是联网计算机的网络

地址，格式为`a.b.c.d`，其中abcd是0~255的数字。
- 域名是对IP地址的别称，易于记忆。
- 域名解析将域名转换成IP地址。

- `ifconfig`: 查看本机IP地址。
- `ping 域名或IP`: 测试与目标主机的连通性。
- `nslookup 域名`: 查看域名对应的IP地址。

### 使用SSH连接远程服务器

SSH是一种网络协议，用于在不安全的网络上安全地执行命令和传输文件。要使用SSH连接远程服务器，需要在本地计算机上运行SSH客户端。

- `ssh 用户名@服务器IP`: 连接远程服务器，需要输入远程服务器的密码。

### 文件传输

可以使用`scp`命令在本地计算机和远程服务器之间传输文件。

- 从本地上传文件到远程服务器：
  ```
  scp /本地路径/文件 用户名@服务器IP:/远程路径/
  ```
- 从远程服务器下载文件到本地：
  ```
  scp 用户名@服务器IP:/远程路径/文件 /本地路径/
  ```

```
使用FinalShell对linux系统进行上传和下载操作,选中需要下载的文集点击下载会保存到桌面。把想要上传的文件找到想要保存的目录中直接把文件进行拖拽进去,建议使用文件拖拽的方式效率会高很多
```