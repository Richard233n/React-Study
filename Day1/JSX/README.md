# 认识JSX语法
这段element变量的声明右侧赋值的标签语法是什么呢？
1. 它不是一段字符串（因为没有使用引号包裹）；
2. 它看起来是一段HTML元素，但是我们能在js中直接给一个变量赋值html吗？
3. 其实是不可以的，如果我们将type="text/babel'"去除掉，那么就会出现语法错误；
4. 它到底是什么呢？其实它是一段jsx的语法，

![认识jSX](http://m.qpic.cn/psc?/V5161jQp0UJiQ743pKKQ25ViNk0hh083/ruAMsa53pVQWN7FLK88i5uL4e*nur*gSZrVUP08aF9su2UqcMyErx8DjYW.nvtYj.je94K0c5G1B4RQ0c4QCQPJdyb5A..rRGY9JgK.byw4!/b&bo=PwZ*AQAAAAADB2U!&rf=viewer_4"title")

# JSX的基本使用
* JSX嵌入变量作为子元素
1. 情况一：当变量是Number、.String、Array类型时，可以直接显示
2. 情况二：当变量是null、undefined、Boolean类型时，内容为空；
   如果希望可以显示null、undefined、Boolean,那么需要转成字符串；
   转换的方式有很多，比如toString.方法、和空字符串拼接，String(变量)等方式
3. 情况三：Object对象类型不能作为子元素(not valid as a React child)



# JSX的事件绑定

# JSX的列表渲染

