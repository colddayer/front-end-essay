### sysmbol

- sysmbol是es6新加入的基本数据类型，表示独一无二的值
- 一般用来解决变量命名重复导致的问题
- description转换为string
- 对象赋值必须加中括号
- sysmbol作为属性名只能被Object.getOwnPropertySymbols读取，返回symbol属性数组
- 使用symbol.for获取相同值
- sysmbol有些静态方法，可以定义字符串某些API如何对对象使用，如split，search，replace等