### # InetAddress

**概念**

- IP地址

	网络设备的表示

- 端口号

	标识进程的逻辑地址，不同进程的标识

- 传输协议

	TCP UDP


**百度的IP和主机**

```java
InetAddress a = InetAddress.getByName("www.baidu.com");
/*打印主机与IP信息*/
System.out.println(a.getHostName()); //www.baidu.com
System.out.println(a.getHostAddress()); // 183.232.231.172
```

**本机的IP和主机**

```java
InetAddress i = InetAddress.getLocalHost(); //DESKTOP-8TQFVIG/192.168.1.100
System.out.println(i);
System.out.println(i.getHostName()); // DESKTOP-8TQFVIG
System.out.println(i.getHostAddress()); //192.168.1.100
```

#### 总结

- `static InetAddress getLocalHost()  `返回本机地址信息

- `static InetAddress[] getAllByName(String host)  `给定主机的名称，返回其IP地址数组与名称

- `String getHostAddress()  `返回主机名

- `String getHostName()  `返回IP地址信息

- `int hashCode()  ` 返回IP地址的HashCode

- `String toString()  `IP地址转换字符串

