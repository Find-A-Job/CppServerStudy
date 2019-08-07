# c++服务端学习


### 基本流程
+ 打开服务端代码
checkout一份代码
用VS打开D:\SVN_download\系统模块\PlatformServer.sln
在刚打开的解决方案里添加现有项目D:\SVN_download\游戏组件\官方正版\铃铛游戏\游戏服务器\GameServer_CHAOJISHUIGUOJI.vcxproj
选中新添加的解决方案，右键仅用于项目-仅生成

+ 配置服务器
在D:\SVN_download\运行\Release\Unicode\目录下
Collocate.exe---网狐棋牌系统配置工具
Correspond.exe---协调服务器
GameServer.exe---游戏服务器
LogonServer.exe---登录服务器

先配置ip，然后开启协调服务器，然后开登录服务器，然后开游戏服务器
在游戏服务器内，创建房间（选择游戏类型，更改房间名字，房间等级，填写服务端口，填写房间人数，填写税收比例50，），配置房间（

+ 联调
将代码附加到房间进程

+ 配置启动客户端
修改ip为调试服务器ip（也就是本机ip）


