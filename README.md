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
function noSpace(x){
let space = '';
for (let i = 0; i < x.length; i++){
  if (x[i] !== ' ') {
  space += x[i];
    }
  }
  return space;
}
```
* Alan Partridge II - Apple Turnover
```javascript
function apple(x){
if ( x ** 2 > 1000){
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
function binToDec(bin){
  return Number.parseInt(bin, 2);
}
```
* Hex to Decimal
```javascript
function hexToDec(hexString){
  return Number.parseInt(hexString, 16);
}
```
* Be Concise IV - Index of an element in an array
```javascript
const find = (array, element) => array.includes(element) ? array.indexOf(element): 'Not found';
```