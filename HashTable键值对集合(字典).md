[TOC]
# HashTable键值对集合(字典)
## 特点
* 键值对是根据键去找值的 键值对中键是唯一的但值可以重复
``` c#
Hashtable ht = new Hashtable();
ht.Add(键, 值);//赋值操作  再次调用相同键赋值时会报错不能重新赋值
ht[键]=值；//作用有两种  1赋值操作  2重新赋值操作
ht.keys; //键的值
ht.containskey();//判断是否该键存在
ht.containsvalue();//判断是否该值存在
ht.clear();//清空所有键值对
ht.Remove(键);
```