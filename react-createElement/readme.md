### React.createElement

React.createElement()： 根据指定的第一个参数创建一个React元素。
- 第一个参数是必填, 传入的是似HTML标签名称，eg: ul, li
- 第二个参数是选填, 表示的是属性，eg: className
- 第三个参数是选填, 子节点，eg: 要显示的文本内容

```
React.createElement(
  type,
  [props],
  [...children]
)
```
- 注意：即使只创建一个li元素，createElement第二个参数也要加上key:’value’，value值彼此不相同，如果不指定此属性，虽然也能按照逻辑正常显示，但会报如下的警告：

```
Warning: Each child in an array or iterator should have a unique "key" prop. Check the top-level render call using <ul>. See https://fb.me/react-warning-keys for more information.
```

### React.cloneElement

React.createElement()： 根据指定的第一个参数克隆一个React元素。
- 第一个参数是必填, react组件或者 dom
- 第二个参数参数是选填, 当前element的 props
- 第三个参数是选填, 子节点，eg: 要显示的文本内容

```
React.cloneElement(
  element,
  [props],
  [...children]
)
```

### 区别
React.cloneElement()与 React.createElement()相似，不同的是它传入的第一个参数element是一个 React 元素，而不是标签名或组件。新添加的属性会并入原有的属性，传入到返回的新元素中，而旧的子元素将被替换。将保留原始元素的键和引用。
- 使用cloneElement我们可以在以后的组件封装中进行更加React化的设计,通过封装公共组件供其他页面迭代使用。
- 使用cloneElement通常会更快,因为您只需要实例化一个初始组件.
- 如果有一个可以克隆而不需要更改的基本组件,那么在语义和性能方面使用cloneElement是一个明确的选择.
