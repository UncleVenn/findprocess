<!--
 * @Author: 张文Uncle
 * @Email: 861182774@qq.com
 * @Date: 2019-08-28 10:16:39
 * @LastEditors: 张文Uncle
 * @LastEditTime: 2019-09-05 15:16:02
 * @Descripttion: 
 -->
# findprocess
记第一次写shell   纪念一下
用于查看端口被哪个程序占用,
```
# findprocess 80
PID        IP         PORT       SERVERNAME
5235       0.0.0.0    80         httpd

使用时将该文件放入/usr/bin目录下
并给于运行权限
chmod +x findprocess

如果使用命令报错如:
': not a valid identifiere 11: readonly: `PORT
/usr/bin/findprocess: line 18: syntax error near unexpected token `$'do\r''
'usr/bin/findprocess: line 18: `    do
则打开文件
vim findprocess
命令行模式
:set ff=unix
保存
:wq
即可
这是因为window下的末尾使用的是CRLF(\n\r)而liunx只能识别使用LF(\n)

```