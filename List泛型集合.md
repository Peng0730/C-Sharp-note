[TOC]
# List泛型集合
## List泛型集合的特点
* 规定集合的类型但不规定的长度
``` c#
list<int> listfan=new list<int> ();
```
* list泛型集合可以转换为数组
``` c#
int[] int1=lists.ToArray();
```
* 数组也可以转换成集合
``` c#
int[] int2 = new int[123];
List<int> lists1 =int2.ToList();
```
## List泛型集合的方法（基本和ArrayList集合一致）
* lists.Add 添加单个元素到集合中
``` c#
lists.Add(1);
foreach (var item in lists)
{
Console.WriteLine(item);
}
```
* lists.AddRange 添加一个集合元素到集合中
``` c#
lists.AddRange(new List<int> { 1, 3, 5, 7, 9 });
foreach (var item in lists)
{
Console.WriteLine(item);
}   
```
* lists.Insert 从下标处插入元素
``` c#
lists.Insert(0, 2);
```
