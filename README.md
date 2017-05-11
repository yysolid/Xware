# Xware
Xware1.0.31
# Xware
迅雷远程下载插件 	

固件命名结构： Xware版本号\_（cpu架构\_指令集_c库类型｜产品名称）.zip  
### 说明：  
 
 1. Xware 指 迅雷固件代号  
 2. CPU架构 指 CPU类型和大小端（l 小、b大）  
 3. 指令集 指 CPU的指令集，如v5te、v5t、603e 等  
 4. 产品名称 指 如果有产品名称则指该产品专用，专用不再在版本名称体现 cpu构架 与指令集  
 5. 如果没有产品名称则表示在该CPU架构下通用  
 
### 支持列表：
![png](https://github.com/prozyy/Xware/blob/master/Img/1.png)


###  安装方法：  
下面以Xware1.0.31_mipsel_32_uclibc.zip安装在MT7620上为例  
解压Xware1.0.31_mipsel_32_uclibc.zip压缩包，发现只有4个文件  
将这四个文件通过winscp都复制到路由器下  
 putty  登录，切换目录到存放上边四个文的目录,执行下边的命令
 
```
 chmod 777 *  
 ./portal  
```
执行行完出现下边这段信息    
```
ETMDaemon            portal
EmbedThunderManager  vod_httpserver
[root@xiazaibao:/xl]#chmod 777 *
[root@xiazaibao:/xl]#./portal
initing...
try stopping xunlei service first...
killall: ETMDaemon: no process killed
killall: EmbedThunderManager: no process killed
killall: vod_httpserver: no process killed
setting xunlei runtime env...
bind(3): errno = 125.
port: 9001 is usable.

YOUR CONTROL PORT IS: 9001

starting xunlei service...
etm path: /xl
execv: /xl/lib/ETMDaemon.

getting xunlei service info...
Connecting to 127.0.0.1:9001 (127.0.0.1:9001)
the active key is not valid.

try again...(has tried 1 time(s)).
getting xunlei service info...
Connecting to 127.0.0.1:9001 (127.0.0.1:9001)

THE ACTIVE CODE IS: fkpswf

go to http://yuancheng.xunlei.com, bind your device with the active code.
finished.
```  
看到上面的THE ACTIVE CODE IS: fkpswf得到这个code就可以去[http://yuancheng.xunlei.com](http://yuancheng.xunlei.com)绑定这个设备了  
![png](https://github.com/prozyy/Xware/blob/master/Img/21.jpg)

 绑定成功就可以愉快的享受远程下载了 

 绑定成功后停止服务命令：
 
 
```
./portal -s
```
开启服务的命令  
```
./portal
```
