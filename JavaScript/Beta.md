### Code challenges Beta

* __[Fibonacci Number](https://www.codewars.com/kata/553e6558e848c5a3180000bc/train/javascript/)__
```javascript
const fib = function (steps) {
  let fibNum = [0, 1];

  for (let i = 2; i < steps + 1; i++) {
    fibNum.push(fibNum[i - 2] + fibNum[i - 1])
  }
  return fibNum[steps];
}
```