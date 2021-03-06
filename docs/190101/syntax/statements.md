### 分支语句

```
if 逻辑表达式
  语句块
end
```

逻辑表达式的值为真则执行语句块

```
if 逻辑表达式
  语句块1
else
  语句块2
end
```

逻辑表达式的值为真则执行语句块1  
逻辑表达式的值为假则执行语句块2

```
switch 表达式
  case 常量标签
    语句块
  end
  default
    语句块
  end
end
```

执行与表达式的值相等的常量标签对应的`case`中的语句块  
当无匹配的常量标签时会执行`default`中的语句块，如`default`未找到则跳出  
常量标签的类型必须支持生成哈希值

### 循环语句

```
while 逻辑表达式
  语句块
end
```

当逻辑表达式的值为真时循环执行语句块

```
loop
  语句块
until 逻辑表达式
end
```

直到逻辑表达式的值为真时跳出循环

```
loop
  语句块
end
```

循环执行语句块直到用户手动跳出

```
for 变量名 = 表达式, 逻辑表达式, 后处理表达式
  语句块
end
```

定义一个变量，当逻辑表达式为真时循环执行语句块，在每个循环的最后执行后处理表达式

```
for 变量名 = 表达式, 逻辑表达式, 后处理表达式 do 表达式
```

定义一个变量，当逻辑表达式为真时循环执行表达式，在每个循环的最后执行后处理表达式

```
foreach 变量名 : 表达式
  语句块
end
```

表达式的值必须是一个支持 `foreach` 遍历的容器  
定义一个变量正序遍历容器，循环执行语句块

```
foreach 变量名 : 表达式1 do 表达式2
```

表达式1的值必须是一个支持 `foreach` 遍历的容器  
定义一个变量正序遍历容器，循环执行表达式2

### 控制语句

```
break
# 跳出循环
continue
# 进入下一轮循环
return
# 结束函数并返回 null
return 表达式
# 结束函数并返回表达式的值
```