[TOC]
# File类
## File类的特点
* 只能用来读取小文件
* 易于操作
## File类的方法
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
* File.ReadAllLines 读取文件中所有单行（返回字串串数组）
``` c#
string[] str = File.ReadAllLines(@"C:\Users\Baicheng\Desktop\新建文件夹\123.text", Encoding.Default);
Console.WriteLine(str);         
```

* File.ReadAllText 读取多行文本（返回字符串）
``` c#
string str = File.ReadAllText(@"C:\Users\Baicheng\Desktop\新建文件夹\123.text", Encoding.Default);
Console.WriteLine(str);
```
*ReadAllLines和ReadAllText只能读取文本形式的文件不能读取多媒体文件（音乐类 视频类文件）
*  File.WriteAllText 将文本写入到文件中
``` c#
File.WriteAllText(@"C:\Users\Baicheng\Desktop\新建文件夹\123.text", "秋水共长天一色");
```
*以上关于写入的方式会覆盖掉之前的文件中的内容 下面的写人方式不会覆盖掉
*  File.AppendAllText 在之前文件内容的基础上添加文本（不换行）
``` c#
File.AppendAllText(@"C:\Users\Baicheng\Desktop\新建文件夹\123.text", "秋水共长天一色");
```
* File.AppendAllLines 在之前文件内容的基础上添加文本（换行）
``` c#
File.AppendAllLines(@"C:\Users\Baicheng\Desktop\新建文件夹\123.text",new string[] { "秋水共长天一色" });
```