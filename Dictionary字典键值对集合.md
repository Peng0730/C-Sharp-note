[TOC]
# Dictionary键值对集合字典
## Dictionary键值对集合字典特点
* 键的类型固定为int 值的类型固定为string 
* 键的值是唯一的不能有多个相同的键
* 可以通过索引的方式给索引的键的值重新赋值
* 可一起遍历键和值
``` c#
Dictionary<int,string> dic= new Dictionary<int, string> { };
dic.Add(1, "上");
dic.Add(2,"下");
dic.Add(3, "左");
dic.Add(4, "右");
dic.Add(5, "前");
dic.Add(6, "后");
foreach (KeyValuePair<int,string> KV in dic)
{
Console.WriteLine("{0}---{1}", KV.Key, KV.Value);
}
```
