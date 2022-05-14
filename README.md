# 需要注意的点
1. 客户端的message 监听的是服务器发过来的数据
2. 服务端
    - new Ws.Server({ port: 8000 }); 创建一个服务器
    - connection 监听是否连接上了
    - ws.on('message', handleMessage); 监听客户端发送的数据
    - server.clients.forEach(function (c) {
        c.send(msg);
      }) 
      服务端向客户端发送数据