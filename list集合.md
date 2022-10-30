[TOC]
# list集合
## ArrayList 
* 相对于数组
* 数组长度不可变，类型单一
* 集合的好处：长度可以任意改变 类型随意
* 语法及使用
``` c#
语法
ArrayList list= new ArrayList();
list.Add(1);
list.Add(c);
list.Add(100m);
list.Add('n');
list.Add(new int[]{1,2,3}); //添加入集合中后默认将元素类型转换为object类型
list.AddRange(new int[]{1,2,3});//AddRange和Add  Add添加单个元素，
//AddRange为在集合中添加集合（数组）
list.Count; //集合的元素个数为
list.clear;//集合全部清除  
list.Remove（）;//集合单个清除  删除单个元素
list.RemoveAt(0);//集合下表元素清除 
list.RemoveRange(0,9);//集合下表范围元素清除 
list.Insert（1，“插入元素”）;//集合插入  插入到下标前
list.InsertRange（1，“插入元素”）;// 集合插入集合 插入到下标前
list.Contains（）;//集合判断是否有无元素
list.Capacity ;//集合开辟的存储元素的内存个数
/*
超出开劈元素个数之后会开辟默认（四个空间）
开辟空间的两倍 如当超过四个空间（1个count）后第五个空间开辟出来的空间为八个（2个count）
第九个开辟的空间为十六个（4个count）
*/
```
