# CodeWars

* __[Sum Mixed Array](https://www.codewars.com/kata/sum-mixed-array/train/javascript/)__ - 8 kyu
```javascript
function sumMix(x){
  return x.map(Number).reduce((acc, cur) => acc + cur, 0);
}
```
* __[Make a function that does arithmetic!](https://www.codewars.com/kata/make-a-function-that-does-arithmetic/train/javascript/)__ - 7 kyu
```javascript
function arithmetic(a, b, operator){
  const operators = {
    add : a + b,
    subtract : a - b,
    divide : a / b,
    multiply : a * b,
  };
  return operators[operator];
}
```
* __[Tip Calculator](https://www.codewars.com/kata/tip-calculator/train/javascript/)__ - 8 kyu
```javascript
function calculateTip(amount, rating) {
  rating = rating.toLowerCase();
  
  let tipObj = {
    terrible : 0,
    poor : 5,
    good : 10,
    great : 15,
    excellent : 20,
  };
  
  if (!tipObj.hasOwnProperty(rating)) {
    return "Rating not recognised";
  } else {
    return Math.ceil(tipObj[rating] * amount / 100);
  }
}
```

* __[Every possible sum of two digits](https://www.codewars.com/kata/every-possible-sum-of-two-digits/train/javascript/)__ - 7 kyu
```javascript
function digits(num){
  const arr = [];
  num = num.toString().split('').map(Number);
  for (let i = 0; i < num.length; i++) {
     for (let j = i + 1; j < num.length; j++){
        arr.push(num[i] + num[j]);
     }
  }
  return arr;
}
```
* __[Correct the mistakes of the character recognition software](https://www.codewars.com/kata/correct-the-mistakes-of-the-character-recognition-software/train/javascript/)__ - 8 kyu
```javascript
function correct(string) {
  return string.replace(/0/g, "O")
               .replace(/5/g, "S")
               .replace(/1/g, "I");
}
```
* __[Complementary DNA](https://www.codewars.com/kata/complementary-dna/train/javascript)__ - 7 kyu
```javascript
function DNAStrand(dna){
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
* __[Isograms](https://www.codewars.com/kata/isograms/train/javascript)__ - 7 kyu
```javascript
function isIsogram(str) {
  const strArr = str.toLowerCase().split('');
  let strDif = strArr.filter((el, i) => i !== strArr.indexOf(el));
  return strDif.length === 0;
}
```
* __[Factorial](https://www.codewars.com/kata/factorial-1/train/javascript/)__ - 7 kyu
```javascript
function factorial(n) {
  let factorial = 1;
  for (let i = 1; i <= n; i++) {
    factorial = factorial * i;
  }
  return factorial;
}
```
* __[Valid Parentheses](https://www.codewars.com/kata/valid-parentheses/train/javascript/)__ - 5 kyu
```javascript
function validParentheses(parens){
  let count = 0;
  for (let i = 0; i < parens.length; i++) {
    if (parens[i] === '(') count++;
    if (parens[i] !== '(') count--;
    if (count < 0) return false;
  }
  return count === 0;
}
```
* __[Lottery machine](https://www.codewars.com/kata/lottery-machine/train/javascript/)__ - 7 kyu
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
* __[Find the capitals](https://www.codewars.com/kata/find-the-capitals-1/train/javascript/)__ - 7 kyu
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
* __[The highest profit wins!](https://www.codewars.com/kata/the-highest-profit-wins/train/javascript/)__ - 7 kyu
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
* __[Is it a palindrome?](https://www.codewars.com/kata/is-it-a-palindrome/train/javascript/)__ - 8 kyu
```javascript
function isPalindrome(x) {
  x = x.toLowerCase().split('');
  for (let i = 0; i < x.length / 2; i++) {
    if (x[i] !== x[x.length - 1 - i]) {
       return false;
     }
  }
  return true;
}
```
* __[Simple Comparison?](https://www.codewars.com/kata/simple-comparison/train/javascript/)__ - 8 kyu
```javascript
function add(a, b) {
  return +a === +b || a === b;
}
```
* __[Is he gonna survive?](https://www.codewars.com/kata/is-he-gonna-survive/train/javascript/)__ - 8 kyu
```javascript
function hero(bullets, dragons) {
  return (bullets * 2) >= dragons;
}
```
* __[Beginner - Lost Without a Map](https://www.codewars.com/kata/beginner-lost-without-a-map/train/javascript/)__ - 8 kyu
```javascript
function maps(x){
  return x.map(x => x * 2);
}
```
* __[Discover The Original Price](https://www.codewars.com/kata/discover-the-original-price/train/javascript/)__ - 7 kyu
```javascript
function discoverOriginalPrice(discountedPrice, salePercentage) {
  salePercentage = salePercentage / 100;
  let originalPrice = discountedPrice / (1 - salePercentage);
  return +originalPrice.toFixed(2);
}
```
* __[Keep Hydrated!](https://www.codewars.com/kata/keep-hydrated-1/train/javascript/)__ - 8 kyu
```javascript
function litres(hour) {
  return Math.floor(hour * 0.5);
}
```
* __[Sum of Multiples](https://www.codewars.com/kata/sum-of-multiples/train/javascript/)__ - 8 kyu
```javascript
function sumMul(n, m){
  if (n >= m) {
    return 'INVALID';
  }
  let sum = 0;
  for (let i = n; i < m; i += n) {
    sum += i;
  }
  return sum;
}
```
* __[Draw stairs](https://www.codewars.com/kata/draw-stairs/train/javascript/)__ - 8 kyu
```javascript
function drawStairs(n) {
  let s = '';
  for (let i = 0; i < n; i++) {
     s = s + ' '.repeat(i) + 'I';
     if (i < (n - 1)) {
       s += '\n';
     }
  }
  return s;
}
```
* __[Sum of the first nth term of Series](https://www.codewars.com/kata/sum-of-the-first-nth-term-of-series/train/javascript/)__ - 7 kyu
```javascript
function SeriesSum(n) {
  let sum = 0;
  for(i = 0; i < n; i++) {
    sum += (1 / (1 + (i * 3)));
  }
  return sum.toFixed(2);
}
```
* __[Remove String Spaces](https://www.codewars.com/kata/remove-string-spaces/train/javascript/)__ - 8 kyu
```javascript
function noSpace(x) {
  let space = '';
  for (let i = 0; i < x.length; i++) {
    if (x[i] !== ' ') {
      space += x[i];
    }
  }
  return space;
}
```
* __[Alan Partridge II - Apple Turnover](https://www.codewars.com/kata/alan-partridge-ii-apple-turnover/train/javascript/)__ - 8 kyu
```javascript
function apple(x) {
  if ( x ** 2 > 1000) {
    return "It's hotter than the sun!!";
  } else {
    return 'Help yourself to a honeycomb Yorkie for the glovebox.';
  }
}
```
* __[Do I get a bonus?](https://www.codewars.com/kata/do-i-get-a-bonus/train/javascript/)__ - 8 kyu
```javascript
function bonusTime(salary, bonus) {
  if (bonus === true) {
    salary = salary * 10;
    return "£" + salary;
  } else {
    return "£" + salary;
  }
}
```
* __[Convert a Boolean to a String](https://www.codewars.com/kata/convert-a-boolean-to-a-string/train/javascript/)__ - 8 kyu
```javascript
function booleanToString(b) {
  if (Boolean(b)) {
    return 'true';
  } else {
    return 'false';
  }
}
```
* __[Parse float](https://www.codewars.com/kata/parse-float/train/javascript/)__ - 8 kyu
```javascript
const parseF = s => (Number.isNaN(parseFloat(s)) ? null : parseFloat(s));
```
* __[Bin to Decimal](https://www.codewars.com/kata/bin-to-decimal/train/javascript/)__ - 8 kyu
```javascript
function binToDec(bin) {
  return Number.parseInt(bin, 2);
}
```
* __[Hex to Decimal](https://www.codewars.com/kata/hex-to-decimal/train/javascript/)__ - 8 kyu
```javascript
function hexToDec(hexString) {
  return Number.parseInt(hexString, 16);
}
```
* __[Be Concise IV - Index of an element in an array](https://www.codewars.com/kata/be-concise-iv-index-of-an-element-in-an-array/train/javascript/)__ - 8 kyu
```javascript
const find = (array, element) => array.includes(element) ? array.indexOf(element): 'Not found';
```
* __[Who is going to pay for the wall?](https://www.codewars.com/kata/who-is-going-to-pay-for-the-wall/train/javascript/)__ - 8 kyu
```javascript
function whoIsPaying(name) {
  const arr = [];
  if (name.length <= 2) {
    arr.push(name);
  } else if (name.length > 2) {
    arr.unshift(name);
    arr.push(name.substring(0, 2));
  }
  return arr;
}
```
* __[Capitalization and Mutability](https://www.codewars.com/kata/capitalization-and-mutability/train/javascript/)__ - 8 kyu
```javascript
function capitalizeWord(word) {
  return word.charAt(0).toUpperCase() + word.slice(1);
}
```
* __[Well of Ideas - Easy Version](https://www.codewars.com/kata/well-of-ideas-easy-version/train/javascript/)__ - 8 kyu
```javascript
function well(x){
  let arr = [];
  arr = x.filter(el => el === 'good');
  if (arr.length === 0) return 'Fail!';
  if (arr.length  > 0 && arr.length <= 2) return 'Publish!';
  if (arr.length > 2) return 'I smell a series!';
}
```
* __[A wolf in sheep's clothing](https://www.codewars.com/kata/a-wolf-in-sheeps-clothing/train/javascript/)__ - 8 kyu
```javascript
function warnTheSheep(queue) {
  if (queue.indexOf('wolf') === queue.length -1) return "Pls go away and stop eating my sheep";
  else return `Oi! Sheep number ${Math.abs(queue.indexOf('wolf') - queue.length + 1 )}! You are about to be eaten by a wolf!`
}
```
* __[JavaScript Array Filter](https://www.codewars.com/kata/javascript-array-filter/train/javascript/)__ - 7 kyu
```javascript
function getEvenNumbers(numbersArray){
  return numbersArray.filter(el => el % 2 === 0);
}
```
* __[Beginner - Reduce but Grow](https://www.codewars.com/kata/beginner-reduce-but-grow/train/javascript/)__ - 8 kyu
```javascript
const grow = x => x.reduce((acc, cur) => acc * cur, 1);
```
* __[Enumerable Magic #25 - Take the First N Elements](https://www.codewars.com/kata/enumerable-magic-number-25-take-the-first-n-elements/train/javascript/)__ - 8 kyu
```javascript
const take = (arr, n) => arr.splice(0, n);
```
* __[SpeedCode #2 - Array Madness](https://www.codewars.com/kata/speedcode-number-2-array-madness/train/javascript/)__ - 8 kyu
```javascript
function arrayMadness(a, b) {
  let sumA = a.reduce((acc, cur) => acc + Math.pow(cur, 2), 0);
  let sumB = b.reduce((acc, cur) => acc + Math.pow(cur, 3), 0);
  return sumA > sumB;
}
```
