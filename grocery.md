## 命令行&Git
### <font color=red>Attention: 使用管理员权限运行命令行！</font>
#### 打开指定文件或文件夹：explorer
如：`C:\Users\15862>explorer D:\`
#### 卸载软件
1. 命令行中输入`wmic`
2. 弹出`wmic:root\cli>`后输入`product get name`
3. 在列表中找到要卸载的软件名后输入`product where name="program name" call uninstall`
4. 弹出的选项中选择`Y`确认卸载
5. 卸载完成后输入`quit`退出
#### 重启计算机
1. 命令行中输入`shutdown -r -t 0`
2. 等待几分钟后按任意键重启计算机
#### 关闭计算机
1. 命令行中输入`shutdown -s -t 0`
2. 等待几分钟后按任意键关闭计算机
#### 退出命令行
1. 输入`exit`或按`Ctrl+Z`
2. 按`Enter`键退出命令行
#### 切换到其他盘
不用逐级退回，直接输入`D:`即可
#### 目录
创建目录最好用下划线替代空格，Windows比较抽风
#### 拷贝文件
1. 拷贝单个文件：输入`copy src\*.* dst`，如：`copy D:\Markdown_files\learn.txt D:\mygit`
2. 拷贝文件夹中所有文件：输入`copy src dst`,如：`copy d:\src d:\dst`
#### 版本回退
需要输入`git reset --hard Head^^`——要多一个`^`
#### 文本文件打印
Windows下用`type`而非`cat`
#### 退出git log状态
输入`q`
#### 以管理员身份运行命令行
键入"cmd"或"git",同时按下ctrl+shift+enter，然后dialog框出现时，选择"以管理员身份运行"
#### 上传
1. 要上传哪个文件或文件夹，就切换到它所在的目录，然后输入`git add.`，再输入`git commit -m "commit message"`，最后输入`git push`
2. 远程库克隆到本地：输入`git clone git@github.com:username/repository.git`
3. 同步远程库：输入`git pull origin main`