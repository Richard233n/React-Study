1. 在界面上通过React显示一个Hello World
* 注意：这里编写React的script代码中，必须添加type="text/babel",作用是可以让babel解析jsx的语法
* ReactDOM.createRoot函数：用于创建一个Reacti根，之后渲染的内容会包含在这个根中
* 参数：将渲染的内容，挂载到哪一个HTML元素上
* 定义一个id为app的div用于渲染
root.Render函数
* 参数:要渲染的根组件

# 案例展示图
![React案例01](http://m.qpic.cn/psc?/V5161jQp0UJiQ743pKKQ25ViNk0hh083/ruAMsa53pVQWN7FLK88i5vDaMMTkVS.yYovWYSi1x8e3q0SHMWeKBoHM4ipV12s9c0e*d*EyArOrxr.Ypslz3DwiTPEmT5CO3S3*KwMrEco!/b&bo=pQU4BAAAAAADB74!&rf=viewer_4"title")

# 组件化开发
* 组件分为两种
1. 类组件
2. 函数组件

# 如何封装一个组件
1. 定义一个类（类名大写，组件的名称是必须大写的，小写会被认为是HTML元素），继承自React.Component
2. 实现当前组件的renderi函数
3. render当中返回的jsx内容，就是之后React会帮助我们渲染的内容


# 组件化问题一：数据在哪里定义？
* 在组件中的数据，我们可以分成两类：
1. 参与界面更新的数据：当数据变量时，需要更新组件渲染的内容；
2. 不参与界面更新的数据：当数据变量时，不需要更新将组建渲染的内容；

* 参与界面更新的数据我们也可以称之为是参与数据流,这个数据是定义在当前对象的<b>state</b>中
1. 我们可以通过在构造函数中this.state={定义的数据}
2. 当我们的数据发生变化时，我们可以调用this.setState来更新数据，并且通知Reacti进行update:操作；
3. 在进行update操作时，就会重新调用renderi函数，并且使用最新的数据，来渲染界面

# 数据存放位置
![React案例01](http://m.qpic.cn/psc?/V5161jQp0UJiQ743pKKQ25ViNk0hh083/ruAMsa53pVQWN7FLK88i5v7mIW*hDoYwbvHkCIQT3qwjCs2tMqDTfQYVruqtr*KsSU.KmORe2vwKQpYncExk7eeg8RNxb.2VU**oXLxoeBQ!/b&bo=DQTSAQAAAAADB*g!&rf=viewer_4"title")

