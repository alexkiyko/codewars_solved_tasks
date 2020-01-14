# CodeWars
* __[The Office II - Boredom Score](https://www.codewars.com/kata/57ed4cef7b45ef8774000014/train/javascript/)__ - 7 kyu
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
* __[Bingo ( Or Not )](https://www.codewars.com/kata/5a1ee4dfffe75f0fcb000145/train/javascript/)__ - 7 kyu
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
* __[Simple Fun #152: Invite More Women?](https://www.codewars.com/kata/58acfe4ae0201e1708000075/train/javascript)__ - 7 kyu
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
* __[Count the Digit](https://www.codewars.com/kata/566fc12495810954b1000030/train/javascript/)__ - 7 kyu
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
* __[Most valuable character](https://www.codewars.com/kata/5dd5128f16eced000e4c42ba/train/javascript/)__ - 7 kyu
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
* __[What is my name score? #1](https://www.codewars.com/kata/576a29ab726f4bba4b000bb1/train/javascript?)__ - 7 kyu
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
* __[Powers of 3](https://www.codewars.com/kata/57be674b93687de78c0001d9/train/javascript/)__ - 7 kyu
```javascript
function largestPower(n) {
  let res = 0;
  while (3 ** res < n) { 
    res++;
  }
  return res - 1;
}
```
* __[Permute a Palindrome](https://www.codewars.com/kata/58ae6ae22c3aaafc58000079/train/javascript/)__ - 6 kyu
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
* __[How many days are we represented in a foreign country?](https://www.codewars.com/kata/58e93b4706db4d24ee000096/train/javascript/)__ - 7 kyu
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
* __[The Office I - Outed](https://www.codewars.com/kata/57ecf6efc7fe13eb070000e1/train/javascript/)__ - 7 kyu
```javascript
function outed(meet, boss){
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
* __[Coding Meetup #5 - Higher-Order Functions Series - Prepare the count of languages](https://www.codewars.com/kata/5828713ed04efde70e000346/train/javascript)__ - 7 kyu
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
* __[Numbers to Objects](https://www.codewars.com/kata/57ced2c1c6fdc22123000316/train/javascript/)__ - 7 kyu
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
* __[Add property to every object in array](https://www.codewars.com/kata/54e8c3e89e2ae6f4900005a1/train/javascript/)__ - 7 kyu
```javascript
for (let i = 0; i < questions.length; i++) {
  questions[i].usersAnswer = null;
}
```
* __[Breaking chocolate problem](https://www.codewars.com/kata/534ea96ebb17181947000ada/train/javascript/)__ - 7 kyu
```javascript
function breakChocolate(n,m) {
  if (n > 0 && m > 0) {
    return (n * m) - 1;
  } else {
    return 0;
  }
}
```
* __[Simple Fun #37: House Numbers Sum](https://www.codewars.com/kata/simple-fun-number-37-house-numbers-sum/train/javascript/)__ - 7 kyu
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
* __[Multiple of index](https://www.codewars.com/kata/multiple-of-index/train/javascript/)__ - 8 kyu
```javascript
function multipleOfIndex(array) {
  const arr = [];

  for (let i = 0; i < array.length; i++) {
    if (array[i] % i === 0) {
      arr.push(array[i]);
    }
  }
  return arr;
}
```
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
