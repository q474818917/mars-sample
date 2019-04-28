# mars
只是客户端解决方案，不包括任何服务器端代码，其中客户端组件有：
+ Comm：基础库，包括socket、线程、消息队列、协程等基础工具；
+ Xlog：通用日志模块，充分考虑移动终端的特点，提供高性能、高可用、安全性、容错性的日志功能
+ SDT：网络诊断模块；
+ STN：信令传输网络模块，负责终端与服务器的小数据信令通道。包含了微信终端在移动网络上的大量优化经验与成果，经历了微信海量用户的考验。

主要处理自定义协议的STN，使用时设计服务器端协议需要和STN通信协议保持一致

## mars-server
这只是netty实现的自定义server，协议与mars对其。包含两个服务：netty长连接服务、和Jetty短连接服务

+ start-web-server.command
+ start-proxy-server.command

## 启动
python start_server.py

