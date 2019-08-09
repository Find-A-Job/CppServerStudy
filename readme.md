# c++服务端学习


### 基本流程
+ 打开服务端代码
```
checkout一份代码
用VS打开D:\SVN_download\系统模块\PlatformServer.sln
在刚打开的解决方案里添加现有项目D:\SVN_download\游戏组件\官方正版\铃铛游戏\游戏服务器\GameServer_CHAOJISHUIGUOJI.vcxproj
选中新添加的解决方案，右键仅用于项目-仅生成（生成的文件名不能为中文，且需要与旧版dll同名）
```
+ 配置服务器
```
在D:\SVN_download\运行\Release\Unicode\目录下
Collocate.exe---网狐棋牌系统配置工具
Correspond.exe---协调服务器
GameServer.exe---游戏服务器
LogonServer.exe---登录服务器

先开系统配置工具并配置好ip，然后开启协调服务器，然后开登录服务器，然后开游戏服务器
在游戏服务器内，创建房间（选择游戏类型，更改房间名字，房间等级，填写服务端口，填写房间人数，填写税收比例50，），配置房间（
```

+ 联调
```
将代码附加到房间进程
```

+ 配置启动客户端
```
修改ip为调试服务器ip（也就是本机ip）
```

+ 添加机器人
```
修改完服务端程序后，需要重新生成机器人项目（生成时需要结束子游戏服务器进程）,
```

+ 完整流程
```
//修改服务端程序
打开D:\SVN_download\系统模块\PlatformServer.sln
在该解决方案中添加现有项，如D:\SVN_download\游戏组件\官方正版\铃铛游戏\游戏服务器\GameServer_CHAOJISHUIGUOJI.vcxproj
修改完子游戏后，选中该项目（解决方案下的一级子目录就是项目，项目下的一级子目录是分类，。。），
重新生成(需要先停止子游戏服务器的服务，否则会报错不让替换)，
其中dll文件名需要和之前该子游戏生成的dll文件同名，
（修改文件名的方法，选中该项目-属性-常规-目标文件名），
这个操作会自动将dll生成至D:\SVN_download\运行\Release\Unicode目录下，
//启动服务器
首先启动协调服务器（只需要开一个）
再启动登录服务器（只需要开一个）
然后是子游戏服务器（一个子游戏服务器对应一款游戏），多个游戏需要开多个服务器，同一个游戏的不同场次也需要开多个服务器
创建房间-选择一款游戏类型-配置房间信息-启动服务
如果修改了子游戏的dll，需要停止服务然后再开启，才会使新的dll生效
//开启客户端
配置客户端连接的服务器ip
路径是D:\nwtDownload\client\trunk\client\base\src\app\models\AppDF.lua
这个路径不能包含中文，否则会失败
修改appdf.SERVER_LIST字段，第五个ip
D:\nwtDownload\client\trunk\run.bat运行

//添加陪玩机器人
```


### 常用函数
+ 1
```
//获取系统时间
GetTickCount()

//将日志重定向到控制器
CString str;
int time=10;
str.Format(_T("%d"), time);
CTraceService::TraceString(str, TraceLevel_Exception);

//输出char*, const char*, char[]类型
char *cpFunctionNameLog = __FUNCTION__;
TCHAR lpMsgzmx1[256];
MultiByteToWideChar(CP_ACP, 0, cpFunctionNameLog, -1, lpMsgzmx1, 256);

CString str2;
str2.Format(_T("%s"),msgzmx1);
CTraceService::TraceString(str2, TraceLevel_Debug);
```
### 注意事项
+ 1
```

```

