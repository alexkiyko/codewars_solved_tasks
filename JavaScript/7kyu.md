### Code challenges 7 kyu
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
function tidyNumber(n){
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