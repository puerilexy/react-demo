ReactDOM.render 是 React 的最基本方法用于将模板转为 HTML 语言，并插入指定的 DOM 节点。

ReactDOM.render(element,container, [,callback]) 方法接收两个必选参数，一个可选参数：

- 第一个是创建的模板，多个 dom 元素外层需使用一个标签进行包裹
- 第二个参数是插入该模板的目标位置
- 第二个参数是dom渲染完成后的回调函数