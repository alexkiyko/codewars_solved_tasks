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
