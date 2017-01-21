---
date: 2017-01-20 23:54
status: public
title: 'shell 接收输入参数'
---

```
光标定位
G    移至最后一行行首
nG    移至第n行行首
n+    下移n行，行首
n-    上移n行，行首
n$    下移n行(1表示本行)，行尾
0    所在行行首
$    所在行行尾
^    所在行首字母
h,j,k,l  左移，下移，上移，右移
H    当前屏幕首行行首
M    屏幕显示文件的中间行行首
L    当前屏幕最底行行首
```

# shell 接收输入参数
```
#!/bin/bash
 
 
#提示“请输入姓名”并等待30秒，把用户的输入保存入变量name中
read -t 30 -p "请输入用户名称:" name
echo -e "\n"
echo "用户名为:$name"
 
#提示“请输入密码”并等待30秒，把用户的输入保存入变量age中，输入内容隐藏
read -t 30 -s -p "请输入用户密码:" age
echo -e "\n"
echo "用户密码为:$age"
 
#提示“请输入性别”并等待30秒，把用户的输入保存入变量sex中，只接受一个字符输入
read -t 30 -n 1 -p "请输入用户性别:" sex
echo -e "\n"
echo "性别为$sex"
```