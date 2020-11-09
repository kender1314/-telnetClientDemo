TelnetClient实际是通过socket实现的。

通过InputStream读取服务器返回的数据，自己根据数据判断什么时候可以命令。

通过OutputStream向服务器发送命令，由于每次写完命令后，需要写入一个换行符，所以使用printStream会省事点（println方法写入命令后自动加入换行符）。

 在不清楚命令返回结果时，可以使用windows telnet连接到设备，输入命令，观察结果，程序根据结果去修改就ok。

TelnetClient实际上是模仿一个Telnet客户端，命令输入和获取和客户端输入命令返回结果是一样的。

应用场景:  
操作交换机时