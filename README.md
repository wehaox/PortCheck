# PortCheck
一个检测ip和端口是否可以访问的小工具
初学golang制作的小玩意  所以代码比较烂就不放出源码了
## 使用场景  
当你的服务器搭建服务之后,发现竟然无法访问，淦
可以使用此工具快速建立一个http服务以测试tcp连接的端口是否可用  
使用浏览器打开 http://ip:port 即可  
### Linux快速启动
```bash
wget https://raw.githubusercontents.com/wehaox/PortCheck/main/PortCheck && chmod +x ./PortCheck && ./PortCheck_Linux -p 8001
```
### Windows下载
https://raw.githubusercontents.com/wehaox/PortCheck/main/PortCheck.exe  
似乎是因为使用upx压缩，启动时可能会报毒(误报)  
## 参数  
1.自定义端口（默认8000）
```shell
./PortCheck -p 端口
```
2.不获取公网ip以快速启动
```shell
./PortCheck -fast 
```
3.可以同时使用
```shell
./PortCheck -p 端口 -fast
```

# 更新
2022.10.26  
增加错误提示，ip按正常循序显示  

2022.10.20  
现在ip直接从网卡读取，以fast启动时，应该也可以直接获取公网IP
