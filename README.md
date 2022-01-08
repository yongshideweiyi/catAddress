# catAddress
lldb指令查看地址

# libCatAddress.dylib配置方法
在根目录下创建`.lldbinit`文件
```
vim ~/.lldbinit
```

在文件中添加下边代码：
```
plugin load /Users/xxxxxxxxx/development/libCatAddress.dylib
```
> plugin load 后边是libCatAddress.dylib文件在电脑上的路径

之后，可以通过`cat address`指令打印内存地址的情况，如下：
```
(lldb) po withUnsafePointer(to: &age){print($0)}
0x00007ffeefbff358
0 elements

(lldb) cat address 0x00007ffeefbff358
address:0x00007ffeefbff358, stack address (SP: 0x7ffeefbff330 FP: 0x7ffeefbff360) ClassVSStruct.test() -> ()
(lldb) 
```

