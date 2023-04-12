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

# 组件化问题二：事件绑定中的this
* 在类中直接定义一个函数，并且将这个函数绑定到元素的onClick事件上，当前这个函数的this指向的是谁呢？

* 默认情况下是undefined
1. 因为在正常的DOM操作中，监听点击，监听函数中的this其实是节点对象（比如说是outto对象）；
2. 这次因为React并不是直接渲染成真实的DOM,我们所编写的button只是一个语法糖，它的本质React的Elementy对象；
3. 那么在这里发生监听的时候，reacti在执行函数时并没有绑定this,默认情况下就是一个undefined;

* 在绑定的函数中，可能想要使用当前对象，比如执行this.setState函数，就必须拿到当前对象的this
1. 我们就需要在传入函数时，给这个函数直接绑定this
2. 类似于以下的写法：<button onClick:={this.changeText..bind(this)}>改变文本</button>


# 数据存放位置
![React案例01](http://m.qpic.cn/psc?/V5161jQp0UJiQ743pKKQ25ViNk0hh083/ruAMsa53pVQWN7FLK88i5v7mIW*hDoYwbvHkCIQT3qwjCs2tMqDTfQYVruqtr*KsSU.KmORe2vwKQpYncExk7eeg8RNxb.2VU**oXLxoeBQ!/b&bo=DQTSAQAAAAADB*g!&rf=viewer_4"title")

