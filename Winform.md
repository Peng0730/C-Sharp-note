[TOC]
# WinForm
## 组成
* 后台代码和Form1.Designer共同组成form函数
### 属性
* Name：为后台要获取的前台控件对象，需要使用Name
* text：为前台控件对象显示的名字
* Anchor：上下作用需要随窗口改变的属性
* ContextMenuStrip 右击菜单属性绑定
* Cursor放在控件上的鼠标图标
* Visible隐藏控件
* Enable显示控件（灰色）但不可以使用
* FlatStyle控件外观
* Font字体 ForeColor字体颜色
* ClientSize.Width 窗体活动区域的宽度
### 事件
* 注册事件  点击按钮谈文本框 双击控件都是默认被选中的那个事件 
``` c#
 private void button2_Click(object sender, EventArgs e)
        {
            //在内存中创建窗体2对象
            Form2 form2=new Form2();
            //展示窗体
            form2.ShowDialog();
        }
```
* 触发事件  点击就触发
* Click 与后台方法对接，实现触发事件，点击按钮就会触发
* MouseEnter当鼠标进入控件的时候触发事件

### 窗体
* 在main函数中创建的窗体对象，为这个窗体应用的主窗体，主窗体意味着当你将主窗体关闭后整个应用程序都关闭
* 对象可以存入静态字段中

### TextBox控件
* 用来输入文本
* 属性中WordWrap用来给控件中的文本换行
* 属性中ScrollBars用来调出滚动条 
* 属性中PasswordChar用来给文本换成密码*的文本
* 事件中TextChanged当文本框中改变的事件