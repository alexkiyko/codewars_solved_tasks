### Code challenges 6 kyu

* __[Sums of Parts](https://www.codewars.com/kata/5ce399e0047a45001c853c2b/train/javascript/)__
```javascript
function partsSums(ls) {
  const arr = [0];
  let sum = 0;
  for (let i = ls.length -1; i >= 0; i--) {
    arr.push(sum += ls[i]);
  }
  return arr.reverse();
}
```

* __[Permute a Palindrome](https://www.codewars.com/kata/58ae6ae22c3aaafc58000079/train/javascript/)__
```javascript
function permuteAPalindrome (input) {
  let obj = {};

  for (let i = 0; i < input.length; i++) {
    if (!obj[input[i]]) {
      obj[input[i]] = 1;
    } else {
      obj[input[i]] = obj[input[i]] + 1;
    }
  }
  let count = 0;

  for (let j in obj) {
    if (obj[j] % 2 !== 0) {
      count++;
    }
  }
  return count <= 1;
}
```

* __[Sum of Digits / Digital Root](https://www.codewars.com/kata/541c8630095125aba6000c00/train/javascript/)__
```javascript
function digital_root(number) {
  number = String(number);
  let nextNumber = 0;

  if (number.length === 1) {
    return Number(number);
  }
    
  for (let i = 0; i < number.length; i++) {
    nextNumber += Number(number[i]);
  }
  return digital_root(nextNumber);
}
```

* __[Which are in?](https://www.codewars.com/kata/550554fd08b86f84fe000a58/train/javascript/)__
```javascript
function inArray(array1,array2) {
  const result = [];
  
  for (let i = 0; i < array2.length; i++) {
    for (let j = 0; j < array1.length; j++) {
      if (array2[i].includes(array1[j])){
        result.push(array1[j]);
      }
    }
  }
  return  result.filter((el, i) => i === result.indexOf(el)).sort();
}
```

