### debounce

- 防抖，对于频繁触发的事件的优化处理之一，前端一般会通过注册回调函数来监听某些事件的触发，注册的回调函数有时会有网络请求或者耗时的异步操作场景，而有一些事件会有较高的触发频率，此时可以通过防抖的形式进行优化，节省浏览器资源消耗。

- 防抖指的是当事件频繁触发时，在规定的时间内只让最后一次事件触发时执行回调的优化方式

const debounce = function (fn, delay) {
    let timer
    return function(...args) {
        timer && clearTimeout(timer)
        timer = setTimeout(() => {
            fn(...args)
        }, delay)
    }
}