## React的开发依赖

# 依赖下载网址
* https://legacy.reactjs.org/docs/cdn-links.html

# 开发React必须依赖三个库：

# 三个依赖包(本地引入失败,建议直接链接引入)

```
https://unpkg.com/react@18/umd/react.development.js
```

```
https://unpkg.com/react-dom@18/umd/react-dom.development.js
```

```
https://unpkg.com/babel-standalone@6/babel.min.js
```

# 依赖的三种引入方式：
1. 直接CDN引入
2. 下载后，添加本地依赖
3. 通过npm管理（后续脚手架再使用）



# 代码片段生成工具
* https://snippet-generator.app/

1. react:包含react所必须的核心代码
2. react-dom:react渲染在不同平台所需要的核心代码
3. babel:将jsx转换成React代码的工具

# 为什么要进行拆分呢？原因就是react-native。
1. react包中包含了react web和react-native所共同拥有的核心代a码。
2. react-dom针对web和native所完成的事情不同：
3. web端：react-dom会将jsx最终渲染成真实的DOM,显示在浏览器中
4. √nativei端：react-dom会将jsx最终渲染成原生的控件（比如Android中的Button,iOS中的UlButton)。


