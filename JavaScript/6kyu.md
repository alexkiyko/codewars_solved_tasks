### Code challenges 6 kyu

* __[Break camelCase](https://www.codewars.com/kata/5208f99aee097e6552000148/train/javascript)__
```javascript
function solution(str) {
  let space = ' ';
  let newStr = '';

  for (let i = 0; i < str.length; i++) {
    if (str[i] === str[i].toUpperCase()) {
      newStr += space + str[i];
    } else {
      newStr += str[i];
    }
  }
  return newStr;
}
```

* __[Almost Even](https://www.codewars.com/kata/529e2e1f16cb0fcccb000a6b/train/javascript/)__
```javascript
var splitInteger = function(num, parts) {
  const arr = [];
  let number = Math.floor(num / parts);
  
  for (let i = 0; i < parts; i++) {
    arr.push(number)
  }

  function arrSum (array) {
    let sum = 0;
    for (let i = 0; i < array.length; i++) {
      sum += array[i];
    }
    return sum;
  }
  
  if (arrSum(arr) === num) {
    return arr;
  }

  for (let i = 0; i < arr.length; i++) {
    arr[i]++;
    if (arrSum(arr) === num) {
      return arr;
    }
  }
};
```

* __[Smallest Difference](https://www.codewars.com/kata/585de79128bc74912d0001c5/train/javascript/)__
```javascript
function smallestDiff(arr1, arr2) {
  if (arr1.length === 0 && arr2.length > 0) return Math.min(...arr2);
  if (arr2.length === 0 && arr1.length > 0) return Math.min(...arr1);
  if (arr1.length === 0 && arr2.length === 0) return -1;
  let diff = Number.MAX_SAFE_INTEGER;

  for (let i = 0; i < arr1.length; i++) {
    for (let j = 0; j < arr2.length; j++) {
      if (Math.abs(arr1[i] - arr2[j]) < diff) {
        diff = Math.abs(arr1[i] - arr2[j]);
      }
    }
  }
  return diff;
}
```

* __[Count the smiley faces!](https://www.codewars.com/kata/583203e6eb35d7980400002a/train/javascript/)__
```javascript
function countSmileys(arr) {
  let count = 0;
  const eye = {
    ':': true,
    ';': true
  };
  const nose = {
    '-': true,
    '~': true
  };
  const mouth = {
    ')': true,
    'D': true
  };

  for (let i = 0; i < arr.length; i++) {
    if (arr[i].length === 2) {
      if (eye[arr[i][0]] && mouth[arr[i][1]]) {
        count++;
      }
    } else if (arr[i].length === 3) {
      if (eye[arr[i][0]] && nose[arr[i][1]] && mouth[arr[i][2]]) {
        count++;
      }
    }
  }
  return count;
}
```

* __[Vasya - Clerk](https://www.codewars.com/kata/555615a77ebc7c2c8a0000b8/train/javascript/)__
```javascript
function tickets(peopleInLine) {
  let bills25 = 0;
  let bills50 = 0;
  let bills100 = 0;

  for (let i = 0; i < peopleInLine.length; i++) {
    let bill = peopleInLine[i];
    
    if (bill === 25) {
      bills25++;
    } else if (bill === 50 && bills25 > 0) {
      bills50++;
      bills25--;
    } else if (bill === 100 && bills50 > 0 && bills25 > 0) {
      bills100++;
      bills50--;
      bills25--;
    } else if (bill === 100 && bills25 > 2) {
      bills100++;
      bills25 -= 3;
    } else {
      return 'NO';
    }
  } return 'YES';
}
```

* __[Primorial Of a Number](https://www.codewars.com/kata/5a99a03e4a6b34bb3c000124/train/javascript/)__
```javascript
function isPrime (num) {
  for(let i = 2; i < num; i++) {
    if(num % i === 0) return false;
  }
  return num > 1;
}

const primes = [] ;
let number = 100;

for(let i = 2; i < number ; i ++) {
  if(isPrime(i)) {
    primes.push(i)
  }
}

function numPrimorial(n){
  let primesUpToN = primes.slice(0, n);
  return primesUpToN.reduce((acc, cur) => acc * cur, 1);
}
```

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
##### Solution 1
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
##### Solution 2
```javascript
function permuteAPalindrome (input) {

  const obj = {};
  let count = 0;

  for (let i = 0; i < input.length; i++) {
    if(obj[input[i]]) {
      obj[input[i]] -= 1;
      count -= 1;
    } else if (!obj[input[i]]) {
      obj[input[i]] = 1;
      count += 1;
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

