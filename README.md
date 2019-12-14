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
