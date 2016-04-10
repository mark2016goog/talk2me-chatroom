# talk2me-chatroom
Automatically exported from code.google.com/p/talk2me-chatroom

 WebSocket+HTML5实现在线聊天室 
 
 最近在看HTML5的东西，我比较感兴趣的是WebSockets,WebWorker以及CORS。去官方过了下WebSockets的规范。WebSockets在Web层实现了TCP协议来进行双向通信，使得程序员们不用再苦逼苦的以各种方式模拟这种双向通信了。
这里用纯WebSockets+HTML5的一些新特性实现了一个在线聊天室的功能。
前端是我永远的痛，好在有Bootstrap:)
服务端基于mod_pywebsocket,客户端就一个html。
实现一个聊天室不难，实现一个稳定的聊天室就要多做些工作了。
使用心跳包定时kill掉无动作的客户端，解决了非正常退出聊天室造成的zombie连接。
数据对象以json的形式在客户端和服务端之间传送
 
当然还有页面上的一些细节：当前用户名粗体显示，头像识别性别等。 
没有实现太多其他的功能，实际体验下WebSockets就好了。
 
mod_pywebsocket的安装过程不说了,下载源码包然后执行install.py。
启动客户端,standlone,py位于mod_pywebsocket的源码包中。
 

    python standlone.py -p 2012 -d /root/Destop/talk2me/ 

 
然后浏览器直接访问127.0.0.1:2012/chatroom.html即可

模拟一段基友聊天场景作为YY：
