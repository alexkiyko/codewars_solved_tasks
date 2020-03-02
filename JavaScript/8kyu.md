### Code challenges 8 kyu

* __[Palindrome Strings](https://www.codewars.com/kata/57a5015d72292ddeb8000b31/train/javascript/)__
```javascript
function isPalindrome(line) {
  line = String(line);
  return line.split('').reverse().join('').toLowerCase() === line.toLowerCase();
}
```

* __[Reversed Strings](https://www.codewars.com/kata/5168bb5dfe9a00b126000018/train/javascript/)__
```javascript
function solution(str){
  let reversedStr = '';
  
  for (let i = str.length -1; i >= 0; i--) {
    reversedStr += str[i]; 
  }
  return reversedStr;
}
```

* __[Find the Difference in Age between Oldest and Youngest Family Members](https://www.codewars.com/kata/5720a1cb65a504fdff0003e2/train/javascript/)__
```javascript
function differenceInAges(ages){
  const agesSorted = ages.sort((min, max) => max -min);
  const maxAge = agesSorted[0];
  const minAge = agesSorted[agesSorted.length -1];
  return [minAge, maxAge, maxAge - minAge];
}
```

* __[Area or Perimeter](https://www.codewars.com/kata/5ab6538b379d20ad880000ab/train/javascript/)__
```javascript
const areaOrPerimeter = function(length , width) {
  if (length === width) return length * width;
  else return length * 2 + width * 2;
};
```

* __[How many lightsabers do you own?](https://www.codewars.com/kata/51f9d93b4095e0a7200001b8/train/javascript/)__
```javascript
function howManyLightsabersDoYouOwn(name) {
  return name === 'Zach' ? 18 : 0;
}
```

* __[Grasshopper - Terminal game combat function](https://www.codewars.com/kata/586c1cf4b98de0399300001d/train/javascript/)__
```javascript
function combat(health, damage) {
  return (health - damage) < 0 ? 0 : health - damage;
}
```

* __[Will there be enough space?](https://www.codewars.com/kata/5875b200d520904a04000003/train/javascript/)__
```javascript
function enough(cap, on, wait) {
  let emptySeats = cap - on;
  let availableSeats = emptySeats - wait;
  if (emptySeats >= wait) {
    return 0;
  } else if (emptySeats < wait) {
    return wait - emptySeats;
  }
}
```

* __[Grasshopper - Terminal game move function](https://www.codewars.com/kata/563a631f7cbbc236cf0000c2/train/javascript/)__
```javascript
function move (position, roll) {
 return position + roll * 2;
}
```

* __[Correct the mistakes of the character recognition software](https://www.codewars.com/kata/correct-the-mistakes-of-the-character-recognition-software/train/javascript/)__
```javascript
function correct(string) {
  return string.replace(/0/g, "O")
               .replace(/5/g, "S")
               .replace(/1/g, "I");
}
```

* __[Multiple of index](https://www.codewars.com/kata/multiple-of-index/train/javascript/)__
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

* __[Sum Mixed Array](https://www.codewars.com/kata/sum-mixed-array/train/javascript/)__
```javascript
function sumMix(x){
  return x.map(Number).reduce((acc, cur) => acc + cur, 0);
}
```

* __[Tip Calculator](https://www.codewars.com/kata/tip-calculator/train/javascript/)__
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

* __[Is it a palindrome?](https://www.codewars.com/kata/is-it-a-palindrome/train/javascript/)__
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

* __[Simple Comparison?](https://www.codewars.com/kata/simple-comparison/train/javascript/)__
```javascript
function add(a, b) {
  return +a === +b || a === b;
}
```

* __[Is he gonna survive?](https://www.codewars.com/kata/is-he-gonna-survive/train/javascript/)__
```javascript
function hero(bullets, dragons) {
  return (bullets * 2) >= dragons;
}
```

* __[Beginner - Lost Without a Map](https://www.codewars.com/kata/beginner-lost-without-a-map/train/javascript/)__
```javascript
function maps(x) {
  return x.map(x => x * 2);
}
```

* __[Keep Hydrated!](https://www.codewars.com/kata/keep-hydrated-1/train/javascript/)__
```javascript
function litres(hour) {
  return Math.floor(hour * 0.5);
}
```

* __[Sum of Multiples](https://www.codewars.com/kata/sum-of-multiples/train/javascript/)__
```javascript
function sumMul(n, m) {
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

* __[Draw stairs](https://www.codewars.com/kata/draw-stairs/train/javascript/)__
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

* __[Remove String Spaces](https://www.codewars.com/kata/remove-string-spaces/train/javascript/)__
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

* __[Alan Partridge II - Apple Turnover](https://www.codewars.com/kata/alan-partridge-ii-apple-turnover/train/javascript/)__
```javascript
function apple(x) {
  if ( x ** 2 > 1000) {
    return "It's hotter than the sun!!";
  } else {
    return 'Help yourself to a honeycomb Yorkie for the glovebox.';
  }
}
```

* __[Do I get a bonus?](https://www.codewars.com/kata/do-i-get-a-bonus/train/javascript/)__
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

* __[Convert a Boolean to a String](https://www.codewars.com/kata/convert-a-boolean-to-a-string/train/javascript/)__
```javascript
function booleanToString(b) {
  if (Boolean(b)) {
    return 'true';
  } else {
    return 'false';
  }
}
```

* __[Parse float](https://www.codewars.com/kata/parse-float/train/javascript/)__
```javascript
const parseF = s => (Number.isNaN(parseFloat(s)) ? null : parseFloat(s));
```

* __[Bin to Decimal](https://www.codewars.com/kata/bin-to-decimal/train/javascript/)__
```javascript
function binToDec(bin) {
  return Number.parseInt(bin, 2);
}
```

* __[Hex to Decimal](https://www.codewars.com/kata/hex-to-decimal/train/javascript/)__
```javascript
function hexToDec(hexString) {
  return Number.parseInt(hexString, 16);
}
```

* __[Be Concise IV - Index of an element in an array](https://www.codewars.com/kata/be-concise-iv-index-of-an-element-in-an-array/train/javascript/)__
```javascript
const find = (array, element) => array.includes(element) ? array.indexOf(element): 'Not found';
```

* __[Who is going to pay for the wall?](https://www.codewars.com/kata/who-is-going-to-pay-for-the-wall/train/javascript/)__
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

* __[Capitalization and Mutability](https://www.codewars.com/kata/capitalization-and-mutability/train/javascript/)__
```javascript
function capitalizeWord(word) {
  return word.charAt(0).toUpperCase() + word.slice(1);
}
```

* __[Well of Ideas - Easy Version](https://www.codewars.com/kata/well-of-ideas-easy-version/train/javascript/)__
```javascript
function well(x){
  let arr = [];
  arr = x.filter(el => el === 'good');
  if (arr.length === 0) return 'Fail!';
  if (arr.length  > 0 && arr.length <= 2) return 'Publish!';
  if (arr.length > 2) return 'I smell a series!';
}
```

* __[A wolf in sheep's clothing](https://www.codewars.com/kata/a-wolf-in-sheeps-clothing/train/javascript/)__
```javascript
function warnTheSheep(queue) {
  if (queue.indexOf('wolf') === queue.length -1) return "Pls go away and stop eating my sheep";
  else return `Oi! Sheep number ${Math.abs(queue.indexOf('wolf') - queue.length + 1 )}! You are about to be eaten by a wolf!`
}
```

* __[Beginner - Reduce but Grow](https://www.codewars.com/kata/beginner-reduce-but-grow/train/javascript/)__
```javascript
const grow = x => x.reduce((acc, cur) => acc * cur, 1);
```

* __[Enumerable Magic #25 - Take the First N Elements](https://www.codewars.com/kata/enumerable-magic-number-25-take-the-first-n-elements/train/javascript/)__
```javascript
const take = (arr, n) => arr.splice(0, n);
```

* __[SpeedCode #2 - Array Madness](https://www.codewars.com/kata/speedcode-number-2-array-madness/train/javascript/)__
```javascript
function arrayMadness(a, b) {
  let sumA = a.reduce((acc, cur) => acc + Math.pow(cur, 2), 0);
  let sumB = b.reduce((acc, cur) => acc + Math.pow(cur, 3), 0);
  return sumA > sumB;
}
```

* __[Surface Area and Volume of a Box](https://www.codewars.com/kata/565f5825379664a26b00007c/train/javascript/)__
```javascript
function getSize(w, h, d) {
  return [2 * (h * w) + 2 * (h * d) + 2 * (w * d), h * w * d];
}
```

* __[Get the mean of an array](https://www.codewars.com/kata/563e320cee5dddcf77000158/train/javascript/)__
```javascript
function getAverage(marks) {
  return Math.floor(marks.reduce((acc, cur) => acc + cur, 0) / marks.length);
}
```

* __[Watermelon](https://www.codewars.com/kata/55192f4ecd82ff826900089e/train/javascript/)__
```javascript
function divide(weight) {
  return weight % 2 === 0 && weight > 2;
}
```

* __[Simple validation of a username with regex](https://www.codewars.com/kata/56a3f08aa9a6cc9b75000023/train/javascript/)__
```javascript
function validateUsr(username) {
  return /^([a-z]|[0-9]|[_]){4,16}$/.test(username);
}
```

* __[Swap Values](https://www.codewars.com/kata/5388f0e00b24c5635e000fc6/train/javascript/)__
```javascript
function swapValues(arr) {
  return arr.reverse();
}
```

* __[Grasshopper - Grade book](https://www.codewars.com/kata/55cbd4ba903825f7970000f5/train/javascript/)__
```javascript
function getGrade (s1, s2, s3) {
  let score = (s1 + s2 + s3) / 3;
  if (score >= 90 && score <= 100) {
    return 'A';
  } else if (score >= 80 && score < 90) {
    return 'B';
  } else if (score >= 70 && score < 90) {
    return 'C';
  } else if (score >= 60 && score < 70) {
    return 'D';
  } else if (score >= 0 && score < 60) {
    return 'F'
  }
}
```

* __[Beginner Series #2 Clock](https://www.codewars.com/kata/55f9bca8ecaa9eac7100004a/train/javascript/)__
```javascript
const past = (hour, min, sec) => (hour * 3600000) + (min * 60000) + (sec * 1000);
```

* __[noobCode 01: SUPERSIZE ME.... or rather, this integer!](https://www.codewars.com/kata/5709bdd2f088096786000008/train/javascript/)__
```javascript
function superSize(num) {
  num = num.toString().split('');
  const maxToMin = num.sort((a, b) => b - a).join('');
  return Number(maxToMin);
}
```
