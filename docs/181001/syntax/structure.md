# 结构
## 定义一个结构
```
struct 结构名
    # 结构体
end
```

结构定义后结构名就可以作为类型名使用  
结构体中只允许变量定义和函数定义  
结构体中的变量或函数称为结构体的成员  
编译器会为成员函数插入一个隐式的`this`参数  
`this`指的是调用成员函数的结构实例本身  
`this`只在成员函数中可用  
可用class代替struct关键字编写程序，两者无实质区别
## 定义一个派生结构
```
struct 结构名 extends 父类结构名
    # 结构体
end
```
派生结构将引入父类结构的所有成员并自动插入一个名为`parent`的成员  
`parent`成员是结构实例本身的父类实例  
如果派生类想要重新实现父类函数，可使用`override`关键字覆写  
```
function 函数名(参数列表（可选）) override
    # 语句块
end
```
## 控制结构的行为  
```
function initialize()
    # 语句块
end
```
构建函数，结构被构建时调用，返回值无意义  
```
function duplicate(orig)
    # 语句块
end
```
复制函数，结构被复制时调用，参数为被复制的实例，返回值无意义  
```
function equal(orig)
    # 语句块
    return true
end
```
比较函数，结构被比较时调用，参数为等号右边的实例，必须返回`true`（代表相等）或`false`（代表不相等）
```
function finalize()
    # 语句块
end
```
析构函数，结构被回收时调用，返回值无意义