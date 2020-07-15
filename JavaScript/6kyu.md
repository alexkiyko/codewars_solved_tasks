### Code challenges 6 kyu

*  __[Custom Array Filters](https://www.codewars.com/kata/53fc954904a45eda6b00097f/train/javascript/)__
```javascript
Array.prototype.even = function(){
  return this.filter(el => typeof el === 'number' &&  el % 1 === 0 && el % 2 === 0);
};

Array.prototype.odd = function(){
  return this.filter(el => typeof el === 'number' && el % 1 === 0 && el % 2 !== 0 );
};

Array.prototype.under = function(x){
  return this.filter(el => typeof el === 'number' && el % 1 === 0 && el < x);
};

Array.prototype.over = function(x){
  return this.filter(el => typeof el === 'number' && el % 1 === 0 && el > x);
};

Array.prototype.inRange = function(min,max){
  return this.filter(el => typeof el === 'number' && el % 1 === 0 && el >= min && el <= max);
};
```

* __[Consonant value](https://www.codewars.com/kata/59c633e7dcc4053512000073/train/javascript/)__
```javascript
function solve(s) {
  let count = 0;
  let max = 0;
  let obj = {
    a: true,
    e: true,
    i: true,
    o: true,
    u: true,
  };
  
  for (let i = 0; i < s.length; i++) {
    if (obj[s[i]]) count = 0;
    else count += s[i].charCodeAt(0) - 96;
    if (count > max) max = count;
  }
  return max;
}
```

* __[Duplicate Encoder](https://www.codewars.com/kata/54b42f9314d9229fd6000d9c/train/javascript/)__
```javascript
function duplicateEncode(word) {
  word = word.toLowerCase();
  const obj = {};
  let res = '';

  for (let i = 0; i < word.length; i++) {
    if (obj[word[i]]) obj[word[i]] += 1;
    else obj[word[i]] = 1;
  }

  for (let i = 0; i < word.length; i++) {
    if (obj[word[i]] === 1) res += '(';
    else res += ')';
  }
  return res;
}
```

* __[Adjacent repeated words in a string](https://www.codewars.com/kata/5245a9138ca049e9a10007b8/train/javascript/)__
```javascript
function countAdjacentPairs(str) {
  const arr =str.toLowerCase().split(' ');
  let count = 0;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === arr[i + 1]) {
      if (arr[i + 1] === arr[i + 2]) {
        continue
      }
      count++;
    }
  }
  return count;
}
```

* __[Extract last names of people named Michael](https://www.codewars.com/kata/580741302e14acaef900015a/train/javascript/)__
```javascript
function getMichaelLastName(inputText) {
  const input = inputText.split(' ');
  const res = [];

  for (let i = 0; i < input.length; i++) {
    let name = input[i];
    let lastName = input[i + 1];
    if (name === 'Michael' && lastName[0] === lastName[0].toUpperCase()) {
      res.push(lastName.replace(/[!?,.]/g, ''));
    }
  }
  return res;
}
```

* __[Masquerade Waiting Line](https://www.codewars.com/kata/5357edc90d9c5df39a0013bc/train/javascript/)__
```javascript
function friendFind(line) {
  let count = 0;

  for (let i = 0; i < line.length; i++) {
    if (line[i] === 'red') {
      if(line[i - 2] === 'blue' && line[i - 1] === 'blue') count++;
      else if (line[i - 1] === 'blue' && line[i + 1] === 'blue') count++;
      else if (line[i + 1] === 'blue' && line[i + 2] === 'blue') count++;
    }
  }
  return count;
}
```

* __[Two Sum](https://www.codewars.com/kata/52c31f8e6605bcc646000082/train/javascript)__
```javascript
function twoSum(numbers, target) {
  let obj = {};
  let res = [];

  for (let i = 0; i < numbers.length; i++) {
    if (obj[numbers[i]] !== undefined) {
      res.push(obj[numbers[i]], i);
    } else {
      obj[target - numbers[i]] = i;
    }
  }
  return res;
}
```

* __[Replace With Alphabet Position](https://www.codewars.com/kata/546f922b54af40e1e90001da/train/javascript/)__
```javascript
function alphabetPosition(text) {
  text = text.toLowerCase().replace(/[^a-z]/g, '');
  let alphabetNumbers = '';

  for (let i = 0; i < text.length; i++) {
    alphabetNumbers += text.charCodeAt(i) - 96 + ' ';
  }
  return alphabetNumbers.trim();
}
```

* __[Counting Duplicates](https://www.codewars.com/kata/54bf1c2cd5b56cc47f0007a1/train/javascript/)__
```javascript
var duplicateCount = function(iterable) {
  iterable = iterable.toLowerCase();
  const obj = {};

  for (let i = 0; i < iterable.length; i++) {
    obj[iterable[i]] ? obj[iterable[i]]+= 1 : obj[iterable[i]] = 1;
  }

  let count  = 0;

  for (let key in obj) {
    if (obj[key] > 1) {
      count++;
    }
  }
  return count;
};
```

* __[Find the unique number](https://www.codewars.com/kata/585d7d5adb20cf33cb000235/train/javascript/)__
```javascript
function findUniq(arr) {
  const filtered = arr.filter(el => arr.indexOf(el) === arr.lastIndexOf(el));
  return filtered[0];
}
```

* __[Merge two arrays](https://www.codewars.com/kata/583af10620dda4da270000c5/train/javascript/)__
```javascript
function mergeArrays(a, b) {
  const arr = [];

  for (let i = 0; i < (a.length + b.length); i++) {
    if(a[i] !== undefined) {
      arr.push(a[i])
    } 
    if(b[i] !== undefined) {
      arr.push(b[i])
    } 
  }
  return arr;
}
```

* __[Multiples of 3 or 5](https://www.codewars.com/kata/514b92a657cdc65150000006/train/javascript/)__
```javascript
function solution(number) {
  let sum = 0;

  for (let i = 1; i < number; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
}
```

* __[Convert string to camel case](https://www.codewars.com/kata/517abf86da9663f1d2000003/train/javascript/)__
```javascript
function toCamelCase(str) {
  const s = str.split('');

  for (let i = 0; i < s.length; i++) {
    if (s[i] === '_' || s[i] === '-') {
      s[i] = '';
      s[i + 1] = s[i + 1].toUpperCase()
    }
  }
  return s.join('');
}
```

* __[Count characters in your string](https://www.codewars.com/kata/52efefcbcdf57161d4000091/train/javascript/)__
```javascript
function count (str) {
  const obj = {};

  for (let i = 0; i < str.length; i++) {
    obj[str[i]] ? obj[str[i]]++ : obj[str[i]] = 1;
  }
  return obj;
}
```

* __[Dashatize it](https://www.codewars.com/kata/58223370aef9fc03fd000071/train/javascript/)__
```javascript
function dashatize(num) {
  if(isNaN(num)) {
    return num.toString();
  }

  num = Math.abs(num).toString();
  let str = '';

  for (let i = 0; i < num.length; i++) {
    if (Number(num[i]) % 2 === 0 && Number(num[i + 1]) % 2 === 0) {
      str += num[i];
    } else {
      str += num[i] + '-';
    }
  }
  return str.substring(0, str.length -1);
}
```

* __[Find the missing term in an Arithmetic Progression](https://www.codewars.com/kata/52de553ebb55d1fca3000371/train/javascript/)__
```javascript
var findMissing = function (list) {
  const diff = (list[list.length - 1] - list[0]) / list.length;

  for (let i = 0; i < list.length - 1; i++) {
    if((list[i + 1] - list[i]) !== diff) {
      return list[i] + diff;
    }
  }
};
```

* __[Delete occurrences of an element if it occurs more than n times](https://www.codewars.com/kata/554ca54ffa7d91b236000023/train/javascript/)__
```javascript
function deleteNth(arr,n) {
  const res = [];
  const obj = {};

  for (let i = 0; i < arr.length; i++) {
    if (obj[arr[i]]) {
      obj[arr[i]] += 1;
    } else {
      obj[arr[i]] = 1;
    }
    if (obj[arr[i]] <= n) {
      res.push(arr[i]);
    }
  }
  return res;
}
```

* __[Title Case](https://www.codewars.com/kata/5202ef17a402dd033c000009/train/javascript/)__
```javascript
function titleCase(title, minorWords = '') {
  if (title.length === 0) {
    return '';
  }
  let minorArr = minorWords.toLowerCase().split(' ');
  const titleArr = title.toLowerCase().split(' ');
  const arr = [];

  arr.push(firstLetterCapital(titleArr[0]));

  for (let i = 1; i < titleArr.length; i++) {
    if(minorArr.indexOf(titleArr[i]) === -1) {
      arr.push(firstLetterCapital(titleArr[i]));
    } else
      arr.push(titleArr[i]);
  }
  return arr.join(' ');
}

function firstLetterCapital(str) {
  return str[0].toUpperCase() + str.slice(1);
}
```

* __[Unique In Order](https://www.codewars.com/kata/54e6533c92449cc251001667/train/javascript/)__
```javascript
var uniqueInOrder = function(iterable) {
  const arr = [];

  for (let i = 0; i < iterable.length; i++) {
    if (iterable[i] !== iterable[i + 1]) {
      arr.push(iterable[i]);
    }
  }
  return arr;
};
```

* __[Array.diff](https://www.codewars.com/kata/523f5d21c841566fde000009/train/javascript/)__
```javascript
function arrayDiff(a, b) {
  const arr =[];

  for (let i = 0; i < a.length; i++) {
    let include = true;
    for (let j = 0; j < b.length; j++) {
      if (a[i] === b[j]) {
        include = false;
        break;
      }
    }
    if (include) {
      arr.push(a[i]);
    }
  }
  return arr;
}
```

* __[Backspaces in string](https://www.codewars.com/kata/5727bb0fe81185ae62000ae3/train/javascript/)__
```javascript
function cleanString(s) {
  const arr = [];

  for (let i = 0; i < s.length; i++) {
    if (s[i] !== '#') {
      arr.push(s[i]);
    } else if (s[i] === '#') {
      arr.pop();
    }
  }
  return arr.join('');
};
```

* __[Find the odd int](https://www.codewars.com/kata/54da5a58ea159efa38000836/train/javascript/)__
```javascript
function findOdd(arr) {
  const obj = {};

  for(let i = 0; i < arr.length; i++) {
    if (obj[arr[i]]) {
      obj[arr[i]]++;
    } else {
      obj[arr[i]] = 1
    }
  }

  for (let prop in obj) {
    if (obj[prop] % 2 !== 0) {
      return +prop;
    }
  }
}
```

* __[Split Strings](https://www.codewars.com/kata/515de9ae9dcfc28eb6000001/train/javascript/)__
```javascript
function solution(str) {
  const arr = [];
  let newStr = '';

  if (str.length % 2 !== 0) {
    newStr = str + '_';
  } else {
    newStr = str;
  }
  
  for (let i = 0; i < newStr.length; i = i + 2) {
    arr.push(newStr[i] + newStr[i + 1]);
  }
  return arr;
}
```

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

