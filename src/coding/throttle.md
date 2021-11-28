### throttle

- 节流指的是当事件频繁触发时，每隔一定时间只能触发一次

const throttle = function (fn, delay) {
    let canDo = true
    return function (...args) {
        if (canDo) {
            canDo = false
            fn(...args)
            setTimeout(() => {
                canDo = true
            }, delay)
        } 
    }
}