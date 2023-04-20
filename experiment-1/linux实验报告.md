
[表达式运算符](#表达式运算符)
[流程控制结构](#流程控制结构)
[Shell脚本基础实验](#shell脚本基础实验)


## 表达式与运算符

### 基本算数运算
expr.sh文件内容
```bash
#!/bin/bash
a=10
b=20
ret=`expr $a + $b`
echo "a + b : $ret"
ret=`expr $a - $b`
echo "a - b : $ret"
ret=`expr $a \* $b`
echo "a * b : $ret"
ret=`expr $b / $a`
echo "b / a : $ret"
ret=`expr $b % $a`
echo "b % a : $ret"
exit 0
```

[expr.sh运行结果](expr.jpg)

### 基本逻辑运算

初始expr2.sh
[expr2运行错误截图](expr2w.jpg)
```bash
#!/bin/bash
a=10
b=20
ret=`expr $a < $b` #语法错误 原因 <号要用反斜杠引用
echo "a < b : $ret"
ret=`expr $a = $b`
echo "a = b : $ret"
ret=`expr $a != $b`
echo "a != b : $ret"
ret=`expr $b >= $a` #语法错误 原因 >号要用反斜杠引用
echo "b >= a : $ret"
```
[expr2成功运行截图](expr2c.jpg)

### string命令

[expr3代码](expr3.jpg)

[expr3运行结果](expr3c.jpg)

### test 命令

[expr4代码](expr4.jpg)

[expr4运行结果](expr4c.jpg)

## 流程控制结构

### if分支结构
安装 anacron 的代码（首先检测有无anacron 文件存在，若无则安装，读入用户指令，时限为5秒，若超时，则退出）
[expr5代码](expr5.jpg)
运行结果
1. 检测无且输入超时:
[expr5c1](expr5c1.jpg)
2. 检测无且安装情况:
[expr5c2](expr5c2.jpg)
3. 检测有情况:
[expr5c3](expr5c3.jpg)

### 循环控制语句

select 退出代码
[select](expr6.jpg)

运行结果
[selectc](expr6c.jpg)

## Shell脚本基础实验

### 优雅退出
同上循环控制语句

### 阶乘
实现比较简单

###杨辉三角
代码
[13-3](13-3.jpg)
运行结果
[13-3c](13-3c.jpg)

### 模拟进度条
[13-4](13-4.jpg)

### 模拟登录
[13-5](13-5.jpg)
[13-5c](13-5c.jpg)
