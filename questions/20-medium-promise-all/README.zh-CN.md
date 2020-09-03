输入接受PromiseLike对象数组的函数PromiseAll，返回值应为Promise <T>，其中T是可解析的结果数组。

ts
const promise1 = Promise.resolve（3）;
const promise2 = 42;
const promise3 =新的Promise <string>（（（resolve，reject）=> {
  setTimeout（resolve，100，'foo'）;
}）;

//应该是Promise <[number，number，string]>
const p = Promise.all（[promise1，promise2，promise3] as const）
```

> 通过谷歌 API 自动翻译