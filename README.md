# Flask-SocketIo
flask-socketio赋予了flask程序支持服务端和客户端间双向低延迟通讯的能力，
客户端可以使用 SocketIO 库或任何支持与服务端建立长链接的兼容库。

安装：

    可以直接使用pip安装:pip install flask-socketio
    
依赖：
    自从1.0版开始，这个扩展完全兼容了python2.7和python3.3+版本。异步服务的支持基于下面3个选择中的一个：

    eventlet 是3个选项中性能最高的，同时支持长轮循(long-polling)和WebSocket。
    gevent 是在以前版本中使用的框架，支持长轮循，如果想支持WebSocket的话需要同时安装gevent-websocket 库。使用gevent和gevent-websocket结合性能也不错，但略低于eventlet。
    flask 基于Werkzeug的开发服务也能用，不过性能上不如上面2个选项，所以它应该只用于开发时使用。这个选项只支持长轮循。

本扩展将自动检测哪些异步框架被安装，默认首选eventlet，其次是gevent，最后是flask自带的开发服务。
对于客户端来说，可以使用官方的Socket.Io来建立于服务端的链接，也有使用swift和c++写成的客户端。非官方的客户端也能工作，只要它实现了Socket.IO 协议。
