# catAddress
lldb指令查看地址

# libCatAddress.dylib配置方法
在根目录下创建`.lldbinit`文件

在文件中添加下边代码：
```
plugin load /Users/xxxxxxxxx/development/libCatAddress.dylib
```
plugin load 后边是libCatAddress.dylib文件在电脑上的路径
