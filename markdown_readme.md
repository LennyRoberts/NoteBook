# Markdown

一级标题
================
二级标题
----------------
- - - 
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
- - -
# 文本格式
第一行文字（使用空行来实现换行/或在第一行末尾家两个空格键）

第二行文字

*斜体* (\*斜体\*)   
**粗体** (\**粗体\**)  
***粗斜体***  (\***粗斜体\***)  

~~使用删除线~~ (\~\~使用删除线\~\~)

<u>使用HTML形式的下划线<u>(\<u>使用HTML形式的下划线\<u>)

使用脚注创建一个脚注[^脚注]  
[^脚注]:这是一个脚注
***
# 列表
## 无序列表使用(*),(+)or(-)开头
* 无序列表1 (\* 无序列表1)  
+ 无序列表2 (\+ 无序列表2)  
- 无序列表3 (\- 无序列表3)  
- - -
## 有序列表使用 数字或字母 + '.'
1.有序列表1 (\1.有序列表1)  
2.有序列表2 (\2.有序列表2)  
a.有序列表a (\a.有序列表a )  
b.有序列表b (\b.有序列表b)  
### 嵌套列表（在子列表前加四个空格）
* 一级无序列表
    1.二级有序列表1
    2.二级有序列表2
+ 一级无序列表  
    a.二级有序列表a  
    b.二级有序列表b  
## 在列表中只用区块(在下一行前添加四个空格)
* 一级无序列表  
    > 无序列表区块1
    >> 无序列表区块2
+ 一级无序列表  
    a.二级有序列表a  
    > 二级区块 

    b.二级有序列表b  
    > 二级区块  
- - - 
# 区块引用（> + 空格）  
> 区块 (\> 区块)
## 区块嵌套（>> + 空格）
> 一级区块 (\> 区块)
>> 二级区块 (\>> 区块)
>>> 三级区块 (\>>> 区块)
## 区块中使用列表(在列表前添加区块声明符)  
> 列表区块  
> * 无序列表  
>   1. 有序列表1  
>   2. 有序列表2  

>> 二级区块  
>> * 无序列表  
>>    1. 有序列表1  
>>    2. 有序列表2 
- - -
# 代码  
## 方法一（每一行前面家四个空格）
    #!/usr/bin/python3.8

    import os
    import socket

    print("this is a python3 program!!!")

    serverAddr = "server.socket"

    while True:
        if os.path.exists(serverAddr):
            os.unlink(serverAddr)
        server_sock = socket.socket(socket.AF_UNIX,socket.SOCK_STREAM)
        server_sock.bind(serverAddr)
        server_sock.listen(20)
        client_sock,client_addr = server_sock.accept()
        print("客户端%s:%slinking.."%(client_sock,client_addr))
        while True:
            recv_data = client_sock.recv(2014)
            print("recevi data:",recv_data.decode())
            client_sock.send("thank you!\n".encode())

## 方法二（使用两个```包含）   
```
   #!/usr/bin/python3.8

    import os
    import socket

    print("this is a python3 program!!!")

    serverAddr = "server.socket"

    while True:
        if os.path.exists(serverAddr):
            os.unlink(serverAddr)
        server_sock = socket.socket(socket.AF_UNIX,socket.SOCK_STREAM)
        server_sock.bind(serverAddr)
        server_sock.listen(20)
        client_sock,client_addr = server_sock.accept()
        print("客户端%s:%slinking.."%(client_sock,client_addr))
        while True:
            recv_data = client_sock.recv(2014)
            print("recevi data:",recv_data.decode())
            client_sock.send("thank you!\n".encode())
``` 
# 链接  
## 方法一（格式：[链接名称](链接地址)）
[菜鸟教程](https://www.runoob.com/markdown)
## 方法二（格式：<链接地址>）
<https://www.runoob.com/markdown>  
## 高级链接方法（通过变量来设置一个链接）  
这个链接用1作为网址变量[Runoob][link1]  
[link1]: https://www.runoob.com/markdown  
# 图片
![alt 属性文本](图片地址 "可选标题")
# 表格  
| 表头 | 表头 |
| ---- | ---- |
| 单元格 | 单元格 |
| 单元格 | 单元格 |
## 表格属性  
-: 有对齐
:- 左对齐
:-: 居中对齐
- - -
| 表头 | 表头 | 表头 |
| ：-----  | ：-----： | -----： |
| 单元格 | 单元格 | 单元格 |
| 单元格 | 单元格 | 单元格 |
