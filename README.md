## React-Study
# React 学习库

* 创建一个vue项目
```shell
npm init vue@latest
```

* 初始化vue项目
```shell
npm install
```
* 虚拟DOM的创建过程
1. 我们通过React..createElement最终创建出来一个ReactElement对像<br>
2. 原因是React利用ReactElementi对象组成了一个JavaScript的对象树<br>
3. JavaScript的对象树就是虚拟DOM(Virtual DOM)

## Reacti官方的说法：Virtual DOM是一种编程理念
1. 虚拟dom帮助我们从命令式编程转到了声明式编程
2. 在这个理念中，UI以一种理想化或者说虚拟化的方式保存在内存中，并且它是一个相对简单的JavaScript对象
3. 我们可以通过ReactDOM.renderi让虚拟DOM和真实DOM同步起来，这个过程中叫做协调(Reconciliation);
## 这种编程的方式赋予了Reacti声明式的API
1. 只需要告诉Reacti希望让Ul是什么状态；
2. React来确保DOM和这些状态是匹配的；
3. 不需要直接进行DOM操作，就可以从手动更改DOM、属性操作、事件处理中解放出来；