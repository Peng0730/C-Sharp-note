[TOC]
# Path类

* Path.GetFileName 快速获取一个路径下的文件的名称(包括拓展名)
``` c#
string path = @"C:\Users\Baicheng\Desktop\1.txt";
string str2=Path.GetFileName(path);
```
* Path.GetFileNameWithoutExtension 快速获取一个路径下的文件的文件名但不包括拓展名
``` c#
string str3 = Path.GetFileNameWithoutExtension(path);
```
* Path.GetExtension 快速获取一个路径下的文件的拓展名但不包括文件名
``` c#
string str4=Path.GetExtension(path);
```
*  Path.GetDirectoryName 快速获取一个文件包含其的文件夹的路径名称
``` c#
 string str5 = Path.GetDirectoryName(path);
```
*  Path.GetFullPath 获得文件所在的全路径
``` c#
 string str6=Path.GetFullPath(path);
```
*  Path.Combine 将两个路径组合成一个路径
``` c#
 string str7=Path.Combine(@"c:\b\","b.txt");
```