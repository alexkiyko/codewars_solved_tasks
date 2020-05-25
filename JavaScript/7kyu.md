### Code challenges 7 kyu

* __[Are the numbers in order?](https://www.codewars.com/kata/56b7f2f3f18876033f000307/train/javascript)__
```javascript
function inAscOrder(arr) {
  for (let i = 0; i < arr.length; i++) {
    if(arr[i] > arr[i + 1]) return false;
  }
  return true;
}
```

* __[Coding Meetup #1 - Higher-Order Functions Series - Count the number of JavaScript developers coming from Europe](https://www.codewars.com/kata/582746fa14b3892727000c4f/train/javascript)__
```javascript
function countDevelopers(list) {
  let count = 0;

  for (let i = 0; i < list.length; i++) {
    if(list[i].continent === 'Europe' && list[i].language === 'JavaScript') {
      count++;
    }
  }
  return count;
}
```

* __[Unique string characters](https://www.codewars.com/kata/5a262cfb8f27f217f700000b/train/javascript/)__
```javascript
function solve(a,b){
  a = a.split('');
  b = b.split('');

  const difA = a.filter(x => b.indexOf(x) === -1);
  const difB = b.filter(x => a.indexOf(x) === -1);

  return [...difA, ...difB].join('');
};
```

* __[Get initials from person name](https://www.codewars.com/kata/57b56af6b69bfcffb80000d7/train/javascript/)__
```javascript
function toInitials(name) {
  let arr = [];

  for (let i = 0; i < name.length; i++) {
    if (name[i] === ' ' || name[i] === '.') {
      continue;
    } else if (name[i] === name[i].toUpperCase()) {
      arr.push(name[i] + '.')
    }
  }
  return arr.join(' ');
}
```

* __[Bumps in the Road](https://www.codewars.com/kata/57ed30dde7728215300005fa/train/javascript/)__
```javascript
function bump(x) {
  let count = 0;

  for (let i = 0; i < x.length; i++) {
    if (x[i] === 'n') {
      count++;
    }
  }
  return count <= 15 ? "Woohoo!" : "Car Dead";
}
```

* __[Find all occurrences of an element in an array](https://www.codewars.com/kata/59a9919107157a45220000e1/train/javascript/)__
```javascript
const findAll = (array, n) => {
  const indexOfN = [];

  for (let i = 0; i < array.length; i++) {
    if (array[i] === n) {
      indexOfN.push(i);
    }
  }
  return indexOfN;
};
```

* __[esreveR](https://www.codewars.com/kata/5413759479ba273f8100003d/train/javascript/)__
```javascript
reverse = function(array) {
  const reversedArr = [];

  for (let i = array.length -1; i >= 0; i--) {
    reversedArr.push(array[i]);
  }
  return reversedArr;
}
```

* __[Simple Fun #176: Reverse Letter](https://www.codewars.com/kata/58b8c94b7df3f116eb00005b/train/javascript/)__
```javascript
function reverseLetter(str) {
  const filteredStr = str.replace(/[^a-z]/g, '');
  let result = '';

  for (let i = filteredStr.length -1; i >= 0; i--) {
    result += filteredStr[i];
  }
  return result;
}
```

* __[Debug Sum of Digits of a Number](https://www.codewars.com/kata/563d59dd8e47a5ed220000ba/train/javascript/)__
```javascript
function getSumOfDigits(integer) {
  let digits =  Math.floor(integer).toString();
  let sum = 0;

  for(let i = 0; i < digits.length; i++) {
    sum += +digits[i];
  }
  return sum;
}
```

* __[Not above the one!](https://www.codewars.com/kata/5b5097324a317afc740000fe/train/javascript/)__
```javascript
function binaryCleaner(arr) {
  const arrNumBelowOne = [];
  const arrIndexOfRemovedNumbers = [];

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] < 2) {
      arrNumBelowOne.push(arr[i]);
    }
    if (arr[i] >= 2 ) {
      arrIndexOfRemovedNumbers.push(i);
    }
  }
  return [arrNumBelowOne, arrIndexOfRemovedNumbers];
}
```

* __[Split In Parts](https://www.codewars.com/kata/5650ab06d11d675371000003/train/javascript/)__
```javascript
var splitInParts = function(s, n) {
  let str = '';
  let count = 0;

  for (let i = 0; i < s.length; i++) {
    str += s[i];
    count++;
    if (count === n) {
      str += ' ';
      count = 0;
    }
  }
  return str.trim();
};
```

* __[Deodorant Evaporator](https://www.codewars.com/kata/5506b230a11c0aeab3000c1f/train/javascript)__
```javascript
function evaporator(content, evap_per_day, threshold) {
  let thresholdPercent = threshold / 100;
  let evapPercent = evap_per_day / 100;
  let thresholdVal = content * thresholdPercent;

  let totalDay = 0;
  while (content >= thresholdVal) {
    content = content - (content * evapPercent);
    totalDay++;
  }
  return totalDay;
}
```

* __[Sum even numbers](https://www.codewars.com/kata/586beb5ba44cfc44ed0006c3/train/javascript/)__
```javascript
function sumEvenNumbers(input) {
  let sum = 0;

  for (let i = 0; i < input.length; i++) {
    if (input[i] % 2 === 0) {
      sum += input[i];
    }
  }
  return sum;
}
```

* __[Series of integers from m to n](https://www.codewars.com/kata/5841f680c5c9b092950001ae/train/javascript/)__
```javascript
function generateIntegers(m, n) {
  const arr = [];
  
  for (let i = m; i <= n; i++) {
    arr.push(i);
  }
  return arr;
}
```

* __[Find min and max](https://www.codewars.com/kata/57a1ae8c7cb1f31e4e000130/train/javascript/)__
```javascript
function getMinMax(arr) {
  let min = arr[0];
  let max = arr[0];

  for (let i = 1; i < arr.length; i++) {
   if (arr[i] <= min) min = arr[i];
   if (arr[i] >= max) max = arr[i];
  }
  return [min, max];
}
```
* __[Multiply array values and filter non-numeric](https://www.codewars.com/kata/55ed875819ae85ca8b00005c/train/javascript/)__
```javascript
function multiplyAndFilter(array, multiplier) {
  const result = [];
  const filtered = array.filter(el => typeof el === 'number');
  for (let i = 0; i < filtered.length; i++) {
    result.push(filtered[i] * multiplier);
  }
  return result;
}
```

* __[Halving Sum](https://www.codewars.com/kata/5a58d46cfd56cb4e8600009d/train/javascript/)__
```javascript
function halvingSum(n) {
  let sum = 0;
  while (n >= 1) {
    sum += n;
    n = Math.floor(n / 2);
  }
  return sum;
}
```

* __[Happy Birthday, Darling!](https://www.codewars.com/kata/5e96332d18ac870032eb735f/train/javascript/)__
```javascript
function womensAge(n) {
  let result;
  if (n % 2 === 0) {
    result = `${n}? That's just 20, in base ${n / 2}!`
  } else {
    result = `${n}? That's just 21, in base ${Math.floor(n / 2)}!`
  }
  return result
}
```

* __[My Languages](https://www.codewars.com/kata/5b16490986b6d336c900007d/train/javascript/)__
```javascript
function myLanguages(obj) {
  const arr = [];
  const objSorted = Object.entries(obj).sort((a,b) => b[1] - a[1]);

  for (let i = 0; i < objSorted.length; i++) {
    if(objSorted[i][1] >= 60) {
      arr.push(objSorted[i][0]);
      }
    }
  return arr;
}
```

* __[Asterisk it](https://www.codewars.com/kata/5888cba35194f7f5a800008b/train/javascript/)__
```javascript
function asteriscIt(n) {
  let result = '';
  let arr;

  if (Array.isArray(n)) {
    arr = n.join('').split('');
  } else {
    arr = Array.from(String(n));
  }

  for (let i = 0; i < arr.length; i++) {
    if(arr[i] % 2 === 0 && arr[i + 1] % 2 === 0 ) {
      result += arr[i] + '*';
    } else {
      result += arr[i];
    }
  }
  return result;
}
```

* __[Changing letters](https://www.codewars.com/kata/5831c204a31721e2ae000294/train/javascript/)__
```javascript
function swap(str) {
  const vowels = {
    a: true,
    e: true,
    i: true,
    o: true,
    u: true
  };
  
  let strCapitalVowels = '';
  
  for(let i = 0; i < str.length; i++) {
    if (vowels[str[i]]) {
      strCapitalVowels += str[i].toUpperCase()
    } else {
      strCapitalVowels += str[i];
    }
  }
  return strCapitalVowels;
}
```

* __[Vowel Count](https://www.codewars.com/kata/54ff3102c1bad923760001f3/train/javascript/)__
```javascript
function getCount(str) {
  let vowelsCount = 0;

  const obj = {
    a: true,
    e: true,
    i: true,
    o: true,
    u: true
  };

  for(let i = 0; i < str.length; i++) {
    if (obj[str[i]]) {
      vowelsCount++
    }
  }
  return vowelsCount;
}
```

* __[Two Oldest Ages](https://www.codewars.com/kata/511f11d355fe575d2c000001/train/javascript/)__
```javascript
function twoOldestAges(ages) {
  return ages.sort((a, b) => a - b).slice(-2);
}
```

* __[Alternate capitalization](https://www.codewars.com/kata/59cfc000aeb2844d16000075/train/javascript/)__
```javascript
function capitalize(s) {
  let even =  '', odd = '';

  for (let i = 0; i < s.length; i++) {
    if (i % 2 === 0) {
      even += s[i].toUpperCase();
      odd += s[i];
    } else {
      even += s[i];
      odd += s[i].toUpperCase();
    }
  }
  return [even, odd];
}
```

* __[Fizz Buzz](https://www.codewars.com/kata/5300901726d12b80e8000498/train/javascript/)__
```javascript
function fizzbuzz(n) {
  const arr = [];

  for (let i = 1; i <= n; i++) {
    if (i % 15 === 0) {
      arr.push('FizzBuzz');
    } else if (i % 5 === 0) {
      arr.push('Buzz')
    } else if (i % 3 === 0) {
      arr.push('Fizz');
    } else {
      arr.push(i);
    }
  }
  return arr;
}
```

* __[Borrower Speak](https://www.codewars.com/kata/57d2ba8095497e484e00002e/train/javascript/)__
```javascript
function borrow(s) {
  return s.replace(/[^a-z]/gi, '').toLowerCase();
}
```

* __[Return the first M multiples of N](https://www.codewars.com/kata/593c9175933500f33400003e/train/javascript/)__
```javascript
function multiples(m, n) {
  const arr = [];

  for (let i = 1; i <= m; i++) {
    arr.push(n * i);
  }
  return arr;
}
```

* __[The Office VI - Sabbatical](https://www.codewars.com/kata/57fe50d000d05166720000b1/train/javascript/)__
```javascript
function sabb(x, val, happ) {
  const numOfLetters = x.replace(/[^sabticl]/gi, '').length;
  return numOfLetters + val + happ > 22 ? 'Sabbatical! Boom!' : 'Back to your desk, boy.';
}
```

* __[Sort the Gift Code](https://www.codewars.com/kata/52aeb2f3ad0e952f560005d3/train/javascript/)__
```javascript
function sortGiftCode(code) {
  return code.split('').sort().join('');
}
```

* __[Currying functions: multiply all elements in an array](https://www.codewars.com/kata/586909e4c66d18dd1800009b/train/javascript/)__
```javascript
const multiplyAll = arr => int => {
  return arr.map(num => num * int)
}
```

* __[Odder Than the Rest](https://www.codewars.com/kata/5983cba828b2f1fd55000114/train/javascript/)__ 
##### Solution 1
```javascript
function oddOne(arr) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2 !== 0) {
      return arr.indexOf(arr[i]);
    }
  } return -1;
}
```
##### Solution 2
```javascript
function oddOne(arr) {
  return arr.findIndex(number => number % 2 !== 0);
}
```

* __[List Filtering](https://www.codewars.com/kata/53dbd5315a3c69eed20002dd/train/javascript/)__
##### Solution 1
```javascript
function filter_list(arr) {
  const filteredArray = [];
  for (let i = 0; i < arr.length; i++) {
    if (typeof arr[i] === 'number') {
      filteredArray.push(arr[i]);
    }
  }
  return filteredArray;
}
```
##### Solution 2
```javascript
function filter_list(arr) {
  const filteredArr = arr.filter(el => typeof el === 'number');
  return filteredArr;
}
```
* __[Ski Jump](https://www.codewars.com/kata/57ed7214f670e99f7a000c73/train/javascript/)__
```javascript
function skiJump(mountain) {
  let speed = mountain.length * 1.5;
  let jumpLength = ((mountain.length * speed * 9) /10).toFixed(2);

  if (jumpLength < 10) {
      return `${jumpLength} metres: He's crap!`;
    } else if (10 <= jumpLength && jumpLength <= 24) {
      return `${jumpLength} metres: He's ok!`;
    } else if (25 <= jumpLength && jumpLength < 50) {
      return `${jumpLength} metres: He's flying!`;
    } else if ( jumpLength >= 50) {
      return `${jumpLength} metres: Gold!!`;
    }
}
```

* __[Scrabblemania](https://www.codewars.com/kata/5b68983a975680155000005d/train/javascript/)__
```javascript
function wordScore(word) {
  const score = {
    "a" : 1, "b" : 3,"c" : 3,"d" : 2, "e" : 1, "f" : 4,"g" : 2,"h" : 4,"i" : 1,
    "j" : 8,"k" : 5,"l" : 1,"m" : 3,"n" : 1,"o" : 1,"p" : 3,"q" : 10,"r" : 1,
    "s" : 1,"t" : 1,"u" : 1,"v" : 4, "w" : 4,"x" : 8,"y" : 4,"z" : 10
    };
  let wordSum = 0;
  let bonus = 50;

  for (let i = 0; i < word.length; i++) {
    if (score[word[i]]) {
      wordSum += score[word[i]];
    }
  }
  if (word.length >= 7) return  wordSum * word.length + bonus;
  else return wordSum * word.length;
}
```

* __[Sum of Minimums!](https://www.codewars.com/kata/5d5ee4c35162d9001af7d699/train/javascript/)__
```javascript
function sumOfMinimums(arr) {
  let sumOfMinVal = 0;
  for (let i = 0; i < arr.length; i++) {
    sumOfMinVal += Math.min(...arr[i]);
  }
  return sumOfMinVal;
}
```

* __[Form The Largest](https://www.codewars.com/kata/5a4ea304b3bfa89a9900008e/train/javascript/)__
```javascript
function maxNumber(n){
  const numbers = Array.from(n.toString());
  return Number(numbers.sort((min, max) => max - min).join(''));  
}
```

* __[Form The Minimum](https://www.codewars.com/kata/5ac6932b2f317b96980000ca/train/javascript/)__
```javascript
function minValue(values) {
  return Number(values
    .filter((number, index) => index === values.indexOf(number))
    .sort((min, max) => min - max)
    .join(''));
}
```

* __[Balanced Number (Special Numbers Series #1)](https://www.codewars.com/kata/5a4e3782880385ba68000018/train/javascript/)__
```javascript
function balancedNum(number) {
  if (number < 100) return 'Balanced';
  number = number.toString();
  let leftSide;
  let rightSide;
  let leftSideSum = 0;
  let rightSideSum = 0;
  
  if (number.length % 2 !== 0) {
    leftSide = Array.from(number).slice(0, number.length / 2);
    rightSide = Array.from(number).slice(number.length / 2 + 1);
  }
  if (number.length % 2 === 0) {
    leftSide = Array.from(number).slice(0, number.length / 2 - 1);
    rightSide = Array.from(number).slice(number.length / 2 + 1);
  }
  for (let i = 0; i < rightSide.length; i++) {
    rightSideSum += +rightSide[i];
    leftSideSum += +leftSide[i];
  }
  return rightSideSum === leftSideSum ? 'Balanced' : 'Not Balanced';
}
```

* __[Scrabble Score](https://www.codewars.com/kata/558fa34727c2d274c10000ae/train/javascript/)__
```javascript
function scrabbleScore(str) {
  if (str === '') return 0;
  str = str.toUpperCase().replace(/[' ']/g, '');
  let score = 0;

  for (let i = 0; i < str.length; i++) {
    if ($dict[str[i]]) {
      score += $dict[str[i]];
    }
  }
  return score;
};
```

* __[Extra Perfect Numbers (Special Numbers Series #7)](https://www.codewars.com/kata/5a662a02e626c54e87000123/train/javascript/)__
```javascript
function extraPerfect(n) {
  const arr = [];

  for (let i = 1; i <= n; i += 2) {
    arr.push(i);
  }
  return arr;
}
```

* __[Product Of Maximums Of Array (Array Series #2)](https://www.codewars.com/kata/5a63948acadebff56f000018/train/javascript/)__
```javascript
function maxProduct(numbers, size) {
  const numbersMax = numbers.sort((a, b) => b - a).slice(0, size);
  return numbersMax.reduce((acc, cur) => acc * cur, 1);
}
```

* __[Remove duplicate words](https://www.codewars.com/kata/5b39e3772ae7545f650000fc/train/javascript/)__
```javascript
function removeDuplicateWords (s) {
  const arr = s.split(' ');
  const arrFiltered = arr.filter((el, index) => index === arr.indexOf(el));
  return arrFiltered.join(' ');
}
```

* __[Help Bob count letters and digits.](https://www.codewars.com/kata/5738f5ea9545204cec000155/train/javascript/)__
```javascript
function countLettersAndDigits(input) {
    let regex = /[^a-z0-9]/gi;
    return input.replace(regex, '').length;
}
```

* __[Sort Out The Men From Boys](https://www.codewars.com/kata/5af15a37de4c7f223e00012d/train/javascript)__
```javascript
function menFromBoys(arr) {
  const arrMen = [];
  const arrBoys = [];

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2 === 0) {
      arrMen.push(arr[i]);
    } else arrBoys.push(arr[i]);
  }
  const arrMenBoys = arrMen.sort((a, b) => a - b).concat(arrBoys.sort((a, b) => b - a));
  return arrMenBoys.filter((item, index) => index === arrMenBoys.indexOf(item));

}
```

* __[Tidy Number (Special Numbers Series #9)](https://www.codewars.com/kata/5a87449ab1710171300000fd/train/javascript/)__
```javascript
function tidyNumber(n) {
  const numbers = Array.from(String(n), Number).join('');
  const numbersInOrder = Array.from(String(n), Number).sort((a, b) => a - b).join('');
  return numbers === numbersInOrder;
}
```

* __[Special Number (Special Numbers Series #5)](https://www.codewars.com/kata/5a55f04be6be383a50000187/train/javascript)__
```javascript
function specialNumber(n) {
  const numbers = n.toString().split('').map(Number);

  if (numbers.every(el => el <= 5)) {
    return "Special!!";
  } else return "NOT!!";
}
```

* __[Sum of numbers from 0 to N](https://www.codewars.com/kata/56e9e4f516bcaa8d4f001763/train/javascript/)__
```javascript
var SequenceSum = (function() {
  function SequenceSum() {}

  SequenceSum.showSequence = function(count) {
    if (count < 0) return `${count} < 0`;
    if (count === 0) return `${count} = 0`;

    let numbersFrom0ToCount = '';
    let sum = 0;

    for (let i = 0; i < count; i++) {
      sum += i;
      numbersFrom0ToCount += i + '+';
      if (i === count - 1) {
        numbersFrom0ToCount += count;
        sum += count;
      }
    }
    return `${numbersFrom0ToCount} = ${sum}`;
  };
  return SequenceSum;
})();
```

* __[Most sales](https://www.codewars.com/kata/5e16ffb7297fe00001114824/train/javascript/)__
```javascript
function top3(products, amounts, prices) {
  const obj = {};

  for (let i = 0; i <products.length; i++) {
    if(!obj[products[i]]) {
      obj[products[i]] = amounts[i] * prices[i];
    }
  }
  const array = Object.entries(obj).sort((a, b) => b[1] - a[1]);
  return [array[0][0], array[1][0], array[2][0]];
}
```

* __[Friend or Foe?](https://www.codewars.com/kata/55b42574ff091733d900002f/train/javascript)__
```javascript
function friend(friends) {
  const realFriends = [];
  
  for (let i = 0; i < friends.length; i++) {
    if (friends[i].length === 4) {
       realFriends.push(friends[i]);
    }
  }
  return realFriends;
}
```

* __[Convert the score](https://www.codewars.com/kata/5b6c220fa0a661fbf200005d/train/javascript/)__
```javascript
function scoreboard(string) {
  const score = [];
  const arr = string.split(' ');

  const num = {
    nil : '0',
    one : '1',
    two : '2',
    three : '3',
    four : '4',
    five : '5',
    six : '6',
    seven : '7',
    eight : '8',
    nine : '9'
  };

  for (let i = 0; i < arr.length; i++) {
    if (num[arr[i]]) {
      score.push(num[arr[i]]);
    }
  }
  return score.map(Number);
}
```

* __[Well of Ideas - Harder Version](https://www.codewars.com/kata/57f22b0f1b5432ff09001cab/train/javascript/)__
```javascript
function well(x){
  let count = 0;

  for (let i = 0; i < x.length; i++) {
    for (let j = 0; j < x[i].length; j++) {          
      if (typeof x[i][j] === 'string' && x[i][j].toLowerCase() === 'good') count++;
    }
  }
  return count === 0 ? 'Fail!' : count <= 2 ? 'Publish!' : 'I smell a series!';
}
```

* __[Count the divisors of a number](https://www.codewars.com/kata/542c0f198e077084c0000c2e/train/javascript/)__
```javascript
function getDivisorsCnt(n) {
  let count = 0;

  for (let i = 1; i <= n; i++) {
    if (n % i === 0) {
      count++;
    }
  }
  return count;
}
```

* __[Substring fun](https://www.codewars.com/kata/565b112d09c1adfdd500019c/train/javascript/)__
```javascript
function nthChar(words) {
  let str = '';

  for (let i = 0; i < words.length; i++) {
    str += words[i].substring(i, i + 1);
  }
  return str;
}
```

* __[Minimize Sum Of Array (Array Series #1)](https://www.codewars.com/kata/5a523566b3bfa84c2e00010b/train/javascript/)__
```javascript
function minSum(arr) {
  const sortedArr = arr.sort((a, b) => b - a);
  const arrMax = sortedArr.slice(0, sortedArr.length/2);
  const arrMin = sortedArr.slice(sortedArr.length/2).sort((a, b) => a - b);
  const sumArr = [];
  
  for (let i = 0; i < arrMax.length; i++) {
    sumArr.push(arrMax[i] * arrMin[i]);
  }
  return sumArr.reduce((acc, cur) => acc + cur, 0);
}
```

* __[The Office III - Broken Photocopier](https://www.codewars.com/kata/57ed56657b45ef922300002b/train/javascript/)__
```javascript
function broken(x) {
  x = x.split('');
  const arr = [];

  for (let i = 0; i < x.length; i++) {
    if (x[i] === '1') {
      x[i] = '0';
        arr.push(x[i]);
      } else if (x[i] === '0') {
        x[i] = '1';
        arr.push(x[i]);
      }
  }
  return arr.join('');
}
```

* __[The Office IV - Find a Meeting Room](https://www.codewars.com/kata/57f604a21bd4fe771b00009c/train/javascript?/)__
```javascript
function meeting(x) {
  return x.indexOf('O') !== -1 ? x.indexOf('O') : 'None available!';
}
```

* __[The Office II - Boredom Score](https://www.codewars.com/kata/57ed4cef7b45ef8774000014/train/javascript/)__
```javascript
function boredom(staff) {
    let sumScores = 0;

    const scores = {
        accounts: 1,
        finance: 2,
        canteen: 10,
        regulation: 3,
        trading: 6,
        change: 6,
        IS: 8,
        retail: 5,
        cleaning: 4,
        'pissing about': 25
    };
    let arrScores = Object.values(staff);

    for (let i = 0; i < arrScores.length; i++) {
        if (scores[arrScores[i]]) {
            sumScores += scores[arrScores[i]];
        }
    }
    if (sumScores < 80) return 'kill me now';
    if (sumScores > 80 && sumScores < 100) return 'i can handle this';
    if (sumScores >= 100) return 'party time!!'
}
```

* __[Bingo ( Or Not )](https://www.codewars.com/kata/5a1ee4dfffe75f0fcb000145/train/javascript/)__
```javascript
function bingo(a) {
  const arr = [];
  let arrFiltered = [];
  let str = '';

  for (let i = 0; i < a.length; i++) {
    arr.push(String.fromCharCode(64 + a[i]));
  }
    
  arrFiltered = arr.sort().filter((el, i) => i === arr.indexOf(el)).join('');
  str = arrFiltered.replace(/[^BINGO]/g,'');
  return str.length === 5? 'WIN' : 'LOSE';
}
```

* __[Simple Fun #152: Invite More Women?](https://www.codewars.com/kata/58acfe4ae0201e1708000075/train/javascript/)__
```javascript
function inviteMoreWomen(arr) {
  let men = 0;
  let women = 0;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === 1) men++;
    else women++;
  }
  return women < men;
}
```

* __[Count the Digit](https://www.codewars.com/kata/566fc12495810954b1000030/train/javascript/)__
```javascript
function nbDig(n, d) {
  const arr = [];
  let countDigit = 0;

  for (let i = 0; i <= n; i++) {
    arr.push(String(i ** 2));
  }

  let newArr = arr.join('').split('');

  for (let i = 0; i < newArr.length; i++) {
    if (newArr[i].includes(d.toString())) countDigit++;
  }
  return countDigit;
}
```

* __[Most valuable character](https://www.codewars.com/kata/5dd5128f16eced000e4c42ba/train/javascript/)__
```javascript
function solve(st) {
  const obj = {};
  const orderedObj = {};

  for (let i = 0; i < st.length; i++) {
    if (!obj[st[i]]) {
      obj[st[i]] = st.lastIndexOf(st[i]) - st.indexOf(st[i]);
    }
  }
  
  let max = 0;
  for (let i in obj) {
    if (obj[i] > max) max = obj[i];
  }

  Object.keys(obj).sort().forEach(key => orderedObj[key] = obj[key]);

  for (let key in orderedObj) {
    if(orderedObj[key] === max) return key;
  }
}
```

* __[What is my name score? #1](https://www.codewars.com/kata/576a29ab726f4bba4b000bb1/train/javascript?)__
```javascript
function nameScore(name) {

  let obj = {};
  let count = 0;

  for (let i = 0; i < name.length; i++) {
    for (let j in alpha) {
      if (j.includes(name[i].toUpperCase())) {
        count += alpha[j];
      }
    }
  }

  obj[name] = count;
  return obj;
}
```

* __[Powers of 3](https://www.codewars.com/kata/57be674b93687de78c0001d9/train/javascript/)__
```javascript
function largestPower(n) {
  let res = 0;
  while (3 ** res < n) { 
    res++;
  }
  return res - 1;
}
```

* __[How many days are we represented in a foreign country?](https://www.codewars.com/kata/58e93b4706db4d24ee000096/train/javascript/)__
```javascript
function daysRepresented(trips){
  const arr = [];

  for (let i = 0; i < trips.length; i++) {
    for (let j = trips[i][0]; j <= trips[i][1]; j++) {
      arr.push(j);
    }
  }
  
  const sortedArr = arr.filter((el, i) => i === arr.indexOf(el));
  return sortedArr.length;
}
```

* __[The Office I - Outed](https://www.codewars.com/kata/57ecf6efc7fe13eb070000e1/train/javascript/)__
```javascript
function outed(meet, boss) {
  let sum = 0;
  let countMembers = 0;
  let bossScore = 0;
  
  for (let prop in meet) {
    sum += meet[prop];
    if (meet.hasOwnProperty(prop)) countMembers++;
    if (prop === boss) bossScore += meet[prop];
  }

  let rating = (sum + bossScore) / countMembers;
  return rating <= 5 ? 'Get Out Now!' : 'Nice Work Champ!';
}
```

* __[Coding Meetup #5 - Higher-Order Functions Series - Prepare the count of languages](https://www.codewars.com/kata/5828713ed04efde70e000346/train/javascript)__
```javascript
function countLanguages(list) {
  let obj = {};
  for (let i = 0; i < list.length; i++) {
    if (!obj[list[i].language]) {
      obj[list[i].language] = 1;
    } else {
      obj[list[i].language] =  obj[list[i].language] + 1;
    }
  }
  return obj;
}
```

* __[Numbers to Objects](https://www.codewars.com/kata/57ced2c1c6fdc22123000316/train/javascript/)__
```javascript
function numObj(s) {
  let arr = [];
  
  for (let i = 0; i < s.length; i++) {
    let obj = {};
    obj[s[i.toString()]] = String.fromCharCode(s[i]);
    arr.push(obj);
  }
    return arr;
}
```

* __[Add property to every object in array](https://www.codewars.com/kata/54e8c3e89e2ae6f4900005a1/train/javascript/)__
```javascript
for (let i = 0; i < questions.length; i++) {
  questions[i].usersAnswer = null;
}
```

* __[Breaking chocolate problem](https://www.codewars.com/kata/534ea96ebb17181947000ada/train/javascript/)__
```javascript
function breakChocolate(n,m) {
  if (n > 0 && m > 0) {
    return (n * m) - 1;
  } else {
    return 0;
  }
}
```

* __[Simple Fun #37: House Numbers Sum](https://www.codewars.com/kata/simple-fun-number-37-house-numbers-sum/train/javascript/)__
```javascript
function houseNumbersSum(inputArray) {
  let index = inputArray.indexOf(0);
  let sum = 0;

  for (let i = 0; i < index; i++) {
    sum += inputArray[i];
  }
  return sum;
}
```

* __[Make a function that does arithmetic!](https://www.codewars.com/kata/make-a-function-that-does-arithmetic/train/javascript/)__
```javascript
function arithmetic(a, b, operator) {
  const operators = {
    add : a + b,
    subtract : a - b,
    divide : a / b,
    multiply : a * b,
  };
  return operators[operator];
}
```

* __[Every possible sum of two digits](https://www.codewars.com/kata/every-possible-sum-of-two-digits/train/javascript/)__
```javascript
function digits(num) {
  const arr = [];
  num = num.toString().split('').map(Number);

  for (let i = 0; i < num.length; i++) {
    for (let j = i + 1; j < num.length; j++) {
      arr.push(num[i] + num[j]);
    }
  }
  return arr;
}
```

* __[Complementary DNA](https://www.codewars.com/kata/complementary-dna/train/javascript)__
```javascript
function DNAStrand(dna) {
  let dnaKey = {
    'A' : 'T',
    'T' : 'A',
    'G' : 'C',
    'C' : 'G'
  };
  let dnaReverse = '';
  for (let i = 0; i < dna.length; i++) {
    dnaReverse += dnaKey[dna[i]] ;
  }
  return dnaReverse;
}
```

* __[Isograms](https://www.codewars.com/kata/isograms/train/javascript)__
```javascript
function isIsogram(str) {
  const strArr = str.toLowerCase().split('');
  let strDif = strArr.filter((el, i) => i !== strArr.indexOf(el));
  return strDif.length === 0;
}
```

* __[Factorial](https://www.codewars.com/kata/factorial-1/train/javascript/)__
```javascript
function factorial(n) {
  let factorial = 1;
  for (let i = 1; i <= n; i++) {
    factorial = factorial * i;
  }
  return factorial;
}
```

* __[JavaScript Array Filter](https://www.codewars.com/kata/javascript-array-filter/train/javascript/)__
```javascript
function getEvenNumbers(numbersArray){
  return numbersArray.filter(el => el % 2 === 0);
}
```

* __[Lottery machine](https://www.codewars.com/kata/lottery-machine/train/javascript/)__
```javascript
function lottery(str) {
  const arrStr = str.replace(/[a-z]/gi, '').split('');
  const filteredArr = arrStr.filter((el, i) => i === arrStr.indexOf(el)).join('');
  if (filteredArr.length > 0) {
    return filteredArr;
  } else {
  return 'One more run!';
  }
}
```

* __[Find the capitals](https://www.codewars.com/kata/find-the-capitals-1/train/javascript/)__
```javascript
var capitals = function (word) {
  const arrList = [];
  for (let i = 0; i < word.length; i++) {
    if (word[i] === word[i].toUpperCase()) {
      arrList.push(word.indexOf(word[i]));
    }
  }
  return arrList;
}
```

* __[The highest profit wins!](https://www.codewars.com/kata/the-highest-profit-wins/train/javascript/)__
```javascript
function minMax(arr) {
  let min = arr[0];
  let max = arr[0];
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i];
    } else if (arr[i] < min) {
      min = arr[i];
    }
  }
  return [min, max];
}
```

* __[Discover The Original Price](https://www.codewars.com/kata/discover-the-original-price/train/javascript/)__
```javascript
function discoverOriginalPrice(discountedPrice, salePercentage) {
  salePercentage = salePercentage / 100;
  let originalPrice = discountedPrice / (1 - salePercentage);
  return +originalPrice.toFixed(2);
}
```

* __[Sum of the first nth term of Series](https://www.codewars.com/kata/sum-of-the-first-nth-term-of-series/train/javascript/)__
```javascript
function SeriesSum(n) {
  let sum = 0;
  for(i = 0; i < n; i++) {
    sum += (1 / (1 + (i * 3)));
  }
  return sum.toFixed(2);
}
```
