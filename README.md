# SignalR-ClientForMiniProgram-js
ASP.NET SignalR依赖JQ，故小程序不能直接使用。但是在ASP.NET Core SignalR中，官方去除了对JQ的依赖，所以存在可以被小程序直接使用的可能，但是客户端js中连接服务端的方法和实现WebSoket方式，跟小程序中的用法不同，也不能直接用。但是通过修改这两处的实现方式，可以让小程序使用。
# 修改处说明
位置：DefaultHttpClient/DefaultHttpClient.prototype.send
具体修改如图：
![](/img/webSocket小程序化.png)
![](/img/xmlRequest方式改变.png)
![](/img/固定通讯方式为webSocket.png)