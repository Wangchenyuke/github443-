# github 443问题解决

***

## pull 或者 Fatch报错

```
fatal: unable to access 'https://github.com/ElemeFE/element.git/': Failed to connect to github.com port 443: Timed out
```

## 解决方法

1.获取访问github.com的动态ip

```shell
ping github.com
```

![{42A78B28-F07F-40E2-BC03-D9729FA6421A}](.\assets\{42A78B28-F07F-40E2-BC03-D9729FA6421A}.png)

这里获取到IP为`20.205.243.166`

2.修改hosts文件

```
C:\Windows\System32\drivers\etc\hosts
```

在文件中添加一行

```
20.205.243.166 github.com
```

3.在终端刷新本地DNS

```
ipconfig /flushdns
```


