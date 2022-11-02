[TOC]
# 重写ToString方法（仅在当前类中重写）
``` c#
class Program
    {
        static void Main()
        {
            Person person = new Person();
            Console.WriteLine(person.ToString());
        }

    }
    public  class Person
    {
        public override string ToString()  //ToString 方法是object的虚方法所以能重写
        {
            return "hello world";
        }
    }

```