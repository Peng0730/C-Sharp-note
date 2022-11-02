[TOC]
# MD5加密
## MD5作用
* 用来加密密码
``` c#
class Program
    {
        static void Main()
        {
            //202cb962ac59075b964b07152d234b70
            Console.WriteLine("请输入密码：");
            string str =GetMD5(Console.ReadLine());
            Console.WriteLine(str);
        }
        public static string GetMD5(string input)
        {
            MD5 Md5 = MD5.Create();
            //开始加密
            //将字符转化成字节数组
            byte[] buffer = Encoding.Default.GetBytes(input);
            byte[] Md5buffer=Md5.ComputeHash(buffer);
            //string str=Encoding.UTF8.GetString(Md5buffer);
            string str = "";
            for (int i = 0; i < Md5buffer.Length; i++)
            {
                //str += Md5buffer[i].ToString();//十进制
                //str += Md5buffer[i].ToString("X");//十进制转换为十六进制
                str += Md5buffer[i].ToString("X2");//ToString存放转换格式 如:内部加c为金钱
            }
            return str;
        }

    }
```