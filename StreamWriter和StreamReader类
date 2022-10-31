[TOC]

# StreamWriter和StreamReader类
## StreamReader
``` c#
 using (StreamReader sr=new StreamReader(@"C:\Users\Baicheng\Desktop\新建文件夹\123.txt",Encoding.Default))
 {
string temp;
while (!sr.EndOfStream)
{
temp = sr.ReadLine();
Console.WriteLine(temp);
Console.WriteLine("读取完毕！");
}
}
```
## StreamWriter
``` c#
using (StreamWriter sw = new StreamWriter(@"C:\Users\Baicheng\Desktop\新建文件夹\321.txt",true))  
{
string str2 = "北海北";
sw.Write(str2);
}
```