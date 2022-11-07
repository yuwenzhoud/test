# 初始Node.js

## 浏览器中的JavaScript运行环境

运行环境是指代码正常运行所需的必要环境。



总结：
1.V8引擎负责解析和执行JavaScript代码。

2.内置API是由运行环境提供的特殊接口，只能在所属的运行环境中被调用。





## 在Nodejs环境中执行JavaScript代码

1.打开终端

2.输入 node  （要执行的js文件的路径）



或者：

shift+鼠标右键，会直接出现打开powershell窗口的选项。

### 终端里的快捷键

​	使用↑，可以快速定位到上次命令。

​	使用tab键，可以补全路径

​	使用esc键，可以快速清空已经输入的命令。

​	输入cls，可以清空输入的命令。 （windows）（mac用clear）

​	

## 读取文件内容

### fs文件系统模块

fs模块时Nodejs官方提供的，用来操作文件的模块，他提供了一系列的方法和属性，用来满足用户对文件的操作需求。

例如：
fs.readFile()方法，是用来读取指定文件中的内容。

fs.writeFile()方法，用来向指定的文件中写入内容。



先导入fs模块：

```js
const fs = require('fs');
```



#### fs.readFile()格式

```js
fs.readFile(path[,options],callback)
```

参数解读：

path:必选参数，字符串，表示文件的路径。

options：可选参数，表示以什么编码格式来读取文件。

callback：必选参数，文件读取完成后，通过回调函数拿到读取的结果。



 例子：

以utf-8的编码格式，读取指定文件的内容，并打印err和dataStr的值：

```js
const fs = require('fs');
fs.readFile('./files/11.txt','utf8',function(err,dataStr){
console.log(err);
console.log('-------');
console.log(dataStr);
})
```

若读取成功，err的值为null；

若读取失败，则err的值为错误对象，dataStr的值为undefined.