# React 入门实例
> 下面代码注意两个地方：
> 1.```<script>``` 标签的 type 属性为 text/babel    
> 因为 React 独有的 JSX 语法，跟 JavaScript 不兼容。凡是使用 JSX 的地方，都要加上 type="text/babel" 。  
> 2.上面代码一共用了三个库： react.js 、react-dom.js 和 Browser.js ，它们必须首先> 加载。其中，react.js 是 React 的核心库，react-dom.js 是提供与 DOM 相关的功能，
> Browser.js 的作用是将 JSX 语法转为 JavaScript 语法，这一步很消耗时间，实际上线的> 时候，应该将它放到服务器完成。
>
```
<head>
    <script src="../build/react.js"></script>
    <script src="../build/react-dom.js"></script>
    <script src="../build/browser.min.js"></script>
</head>
<body>
<div id="example"></div>
<script type="text/babel">
    // ** Our code goes here! **
</script>
</body>
```

> $ babel src --out-dir build
> 可以通过babel 将JSX 语法转为 JavaScript 语法

#  ReactDOM.render()
### ReactDOM.render 是 React 的最基本方法，用于将模板转为 HTML 语言，并插入指定的 DOM 节点。
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('example')
);
```
> 上面代码将一个 h1 标题，插入 example 节点（查看 demo01），运行结果如下。
