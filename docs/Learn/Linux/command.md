# Linux Command

## 文件的基本操作
- cat : 查看文件内容或连接文件
- less : 查看文本文件
- mv : 移动和重命名文件
- rm : 删除文件和目录
- cp : 复制文件和目录
- cd : 切换工作目录
- ls : 列出目录内容
- mkdir : 新建目录
- dd : 复制文件并对原文件的内容进行转换和格式化处理


## 文件的权限与属性
- umask : 设置默认权限
- chattr : 改变文件底层属性
- lsattr : 显示文件底层属性
- chgrp : 更改文件用户组
- chmod : 更改文件权限
- chown : 更改文件所有者和用户组


# 文件的备份与恢复
- dump : 备份文件系统
- restore : 还原备份文件


## 文件的压缩与解压
- bzip2 : 管理".bz2"格式的压缩文件
- bunzip2 : 解压缩".bz2"格式的压缩文件
- bzcat : 显示".bz2"格式的压缩文件内容
- gzip : 管理".gz"格式的压缩文件
- gunzip : 解压缩".gz"格式的文件
- zip : 管理".zip"格式的压缩文件
- unzip : 解压缩".zip"格式的文件
- zcat : 显示".zip"格式的压缩文件内容
- tar : 打包备份文件或目录


# 任务与进程
- bg : 将指定任务号的任务放到后台运行
- fg : 将指定任务号的任务放到前台运行
- jobs : 显示当前终端任务列表及状态
- ps : 查看进程
- pstree : 以树形图展现进程之间的派生关系
- top : 动态查看进程
- kill : 删除正在执行中的进程或任务
- killall : 删除指定名字的所有进程


# 软件包
- apt : APT软件包管理工具
- yum : YUM软件包管理工具
- dpkg : Debian Linux系统中安装、创建和管理软件包
- rpm : Redhat Liunx系统中安装、创建和管理软件包


# 编程开发工具
- gcc : 编译程序
- gdb : 调试程序
- make : 自动维护编译工作


# 常用工具命令
- cal : 显示日历
- date : 显示日期
- grep : 显示匹配行
- pwd : 显示当前目录


# 用户与工作组
- su : 切换身份
- sudo : 以另一个用户身份执行命令
- passwd : 更改用户密码
- chage : 密码时效管理
- useradd : 创建用户帐号
- userdel : 删除用户帐号
- usermod : 修改用户帐号信息
- gpasswd : 用户组管理
- groupadd : 创建用户组
- groupdel : 删除用户组
- newgrp : 当前用户临时登入到已有组


# 磁盘与硬件设备
- df : 显示磁盘空间使用情况
- du : 显示目录的磁盘空间使用情况
- fdisk : 分区表控制器
- fsck : 检查并试图修复文件系统中的错误
- mkfs : 在设备上创建文件系统
- mount : 加载文件系统到指定的挂载点
- umount : 卸载文件系统


# 系统的关机与重启
- halt : 关机
- poweroff : 关机
- shutdown : 关机
- reboot : 重启
- init : 切换运行级别


# 网络应用
- rsync : 同步远程数据