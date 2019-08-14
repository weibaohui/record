java -jar xxx.jar
```java -Dcom.sun.management.jmxremote \
-Dcom.sun.management.jmxremote.authenticate=false \
-Dcom.sun.management.jmxremote.ssl=false \
-Dcom.sun.management.jmxremote.port=35005 \
-Dcom.sun.management.jmxremote.rmi.port=35005 \
-Djava.rmi.server.hostname=remotehost \
-jar xxx.jar
```
其中hostname需设置为remotehost
端口通过Service开放35005，其中targetPort:35005保持一致
经过测试VisualVm可以直接使用Service开放的IP进行访问，比如NodePortIP.
但是JConsole只能通过remotehost来访问，可以通过设置hosts文件来实现解析NodePortIP。

