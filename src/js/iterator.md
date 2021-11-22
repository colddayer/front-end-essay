### Iterator
- es6新加入为数据结构提供统一遍历的接口
- 这个接口返回一个对象，对象中有必选的Next方法，和可选的return方法，throw方法   
- 这个接口使用for ... of 消费
- for ... of会循环调用对象的next方法，直到遍历结束，如果for ... of中有break会执行return方法，如果for ... of中有报错，会执行throw方法