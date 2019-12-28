# CodeWars
* Simple Comparison?
```javascript
function add(a, b) {
  if (+a === +b || a === b) return true;
  else return false;
}
```
* Is he gonna survive?
```javascript
function hero(bullets, dragons){
  if ((bullets * 2) >= dragons) return true;
  else return false;
}
```
* Beginner - Lost Without a Map
```javascript
function maps(x){
  return x.map(x => x * 2);
}
```
* Discover The Original Price
```javascript
function discoverOriginalPrice(discountedPrice, salePercentage) {
  salePercentage = salePercentage / 100;
  let originalPrice = discountedPrice / (1 - salePercentage);
  return +originalPrice.toFixed(2);
}
```
* Keep Hydrated!
```javascript
function litres(hour) {
  return Math.floor(hour * 0.5);
}
```
* Sum of Multiples
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
* Draw stairs
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
* Sum of the first nth term of Series
```javascript
function SeriesSum(n) {
  let sum = 0;
  for(i = 0; i < n; i++) {
    sum += (1 / (1 + (i * 3)));
  }
  return sum.toFixed(2);
}
```
* Remove String Spaces
1. Solution 
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
* Alan Partridge II - Apple Turnover
```javascript
function apple(x) {
  if ( x ** 2 > 1000) {
    return "It's hotter than the sun!!";
  } else {
    return 'Help yourself to a honeycomb Yorkie for the glovebox.';
  }
}
```
* Do I get a bonus?
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
* Convert a Boolean to a String
```javascript
function booleanToString(b) {
  if (Boolean(b)) {
    return 'true';
  } else {
    return 'false';
  }
}
```
* Parse float
```javascript
const parseF = s => (Number.isNaN(parseFloat(s)) ? null : parseFloat(s));
```
* Bin to Decimal
```javascript
function binToDec(bin) {
  return Number.parseInt(bin, 2);
}
```
* Hex to Decimal
```javascript
function hexToDec(hexString) {
  return Number.parseInt(hexString, 16);
}
```
* Be Concise IV - Index of an element in an array
```javascript
const find = (array, element) => array.includes(element) ? array.indexOf(element): 'Not found';
```
* Who is going to pay for the wall?
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
* Capitalization and Mutability
```javascript
function capitalizeWord(word) {
  return word.charAt(0).toUpperCase() + word.slice(1);
}
```
* Well of Ideas - Easy Version
```javascript
function well(x){
  let arr = [];
  arr = x.filter(el => el === 'good');
  if (arr.length === 0) return 'Fail!';
  if (arr.length  > 0 && arr.length <= 2) return 'Publish!';
  if (arr.length > 2) return 'I smell a series!';
}
```
* A wolf in sheep's clothing
```javascript
function warnTheSheep(queue) {
  if (queue.indexOf('wolf') === queue.length -1) return "Pls go away and stop eating my sheep";
  else return `Oi! Sheep number ${Math.abs(queue.indexOf('wolf') - queue.length + 1 )}! You are about to be eaten by a wolf!`
}
```
* JavaScript Array Filter
```javascript
function getEvenNumbers(numbersArray){
  return numbersArray.filter(el => el % 2 === 0);
}
```
* Beginner - Reduce but Grow
```javascript
const grow = x => x.reduce((acc, cur) => acc * cur, 1);
```
* Enumerable Magic #25 - Take the First N Elements
```javascript
const take = (arr, n) => arr.splice(0, n);
```
* SpeedCode #2 - Array Madness
```javascript
function arrayMadness(a, b) {
  let sumA = a.reduce((acc, cur) => acc + Math.pow(cur, 2), 0);
  let sumB = b.reduce((acc, cur) => acc + Math.pow(cur, 3), 0);
  return sumA > sumB ? true : false;
}
```
* The highest profit wins!
```javascript
function minMax(arr){
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