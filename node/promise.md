Promise.all
当一些异步任务，如初始化时的一些无序的，需要初始化的一批，那么就用到了这个，需要的是当所有的任务都完成的时候初始化完成，停止转菊花，然后进入主页，这个就是所需要的，当所有任务完成的时候才输出。
如果需要其中一个fail就停止，那么这个也满足需要。
注意：返回的promise没有done哦~
Promise.all(...).then(...).catch(...).done is not a function

引用MDN：
Promise.all(iterable) 方法返回一个promise，该promise会等iterable参数内的所有promise都被resolve后被resolve，或以第一个promise被reject的原因而reject 。
iterable 一个可迭代对象，比如Array。参见iterable.
结果是promise的一组值。如果传入的可迭代数组中某项不是一个promise，该项会被用Promise.resolve转换为一个promise。如果任一传入的promise被拒绝了，all Promise立刻带着该promise的拒绝原因进入拒绝(rejected)状态，不再理会其它传入的promise是否被解决。
Promise.all waits for all fulfillments (or the first rejection).
```
var p1 = Promise.resolve(3);
var p2 = 1337;
var p3 = new Promise((resolve, reject) => {
    console.log('p3 start');
    setTimeout(resolve, 100, "foo");
});

Promise.all([p1, p2, p3]).then((values) => {
    console.log(values); // [3, 1337, "foo"] 
}).catch((error) => {
    console.error(error)
});
```

Promise.all fail-fast behaviour
```

var p1 = new Promise((resolve, reject) => {
    console.log('p1 start');
    setTimeout(resolve, 1000, "one");
});
var p2 = new Promise((resolve, reject) => {
    console.log('p2 start');
    setTimeout(resolve, 2000, "two");
});
var p3 = new Promise((resolve, reject) => {
    console.log('p3 start');
    setTimeout(resolve, 3000, "three");
});
var p4 = new Promise((resolve, reject) => {
    console.log('p4 start');
    setTimeout(resolve, 4000, "four");
});
var p5 = new Promise((resolve, reject) => {
    console.log('p5 start');
    reject("reject");
});

Promise.all([p1, p2, p3, p4, p5]).then((value) => {
    console.log(value);
}).catch((error) => {
    console.error('error', error)
});

```
