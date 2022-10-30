[TOC]
# File类

* File.Create 在指定路径下创建指定文件 当桌面有该文件时 再次调用该方法时，文件不会重新创建，会在已有的文件上进行修改
``` c#
File.Create(@"C:\Users\Baicheng\Desktop\new.txt");
Console.WriteLine("创建成功!");
```
* File.Delete 彻底删除在指定路径下的指定文件（回收站中找不到删除的文件）
``` c#
File.Delete(@"C:\Users\Baicheng\Desktop\new.txt");
Console.WriteLine("删除成功!");
```
*  File.Copy 将指定路径下的指定文件复制到指定文件路径下并命名为指定文件名
``` c#
 File.Copy(@"C:\Users\Baicheng\Desktop\new.txt",@"C:\Users\Baicheng\Desktop\123.txt");
 Console.WriteLine("复制成功");
 ```
 *  File.Move 将文件移动到指定路径下并命名文件
 ``` c#
  File.Move(@"C:\Users\Baicheng\Desktop\new.txt", @"C:\Users\Baicheng\Desktop\新建文件夹\123.txt");
  ```
* File.ReadAllBytes 将文件读取后将内容转换为字节
``` c#
byte[] by=File.ReadAllBytes( @"C:\Users\Baicheng\Desktop\新建文件夹\123.txt");
string str = Encoding.Default.GetString(by);  //将字节转换为字符串
Console.WriteLine(str);
```

* File.WriteAllBytes 将内容以字节组写入文件
``` c#
string str ="学习文件的写入方式1  学习文件的写入方式2 学习文件的写入方式3";
byte[] bytes = Encoding.Default.GetBytes(str);//将输入的字符串转换为字节组
File.WriteAllBytes( @"C:\Users\Baicheng\Desktop\新建文件夹\123.txt",bytes);
```