### Code challenges 5 kyu

* __[Convert PascalCase string into snake_case](https://www.codewars.com/kata/529b418d533b76924600085d/train/javascript/)__
```javascript
function toUnderscore(s) {
  let res ='';
  let first = Number(s[0]) ? s[0].toString() : s[0].toLowerCase();

  for (let i = 1; i < s.length; i++) {
    if (s[i] === s[i].toUpperCase() && !Number(s[i])) {
      res += '_' + s[i].toLowerCase();
    } else if (Number(s[i])) {
      res += s[i];
    } else {
      res += s[i];
    }
  }
  return first + res;
}
```

* __[Where my anagrams at?](https://www.codewars.com/kata/523a86aa4230ebb5420001e1/train/javascript/)__
```javascript
function anagrams(word, words) {
  word = word.split('').sort().join('');
  let arr = [];

  for (let i = 0; i < words.length; i++) {
    let sorted = words[i].split('').sort().join('');
    if (word === sorted) {
      arr.push(words[i]);
    }
  }
  return arr;
}
```

* __[Moving Zeros To The End](https://www.codewars.com/kata/52597aa56021e91c93000cb0/train/javascript/)__
```javascript
var moveZeros = function (arr) {
  const zeros = [];
  const numbers = [];

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] !== 0) {
      numbers.push(arr[i])
    } else {
      zeros.push(arr[i]);
    }
  }
  return [...numbers, ...zeros];
};
```

* __[Scramblies](https://www.codewars.com/kata/55c04b4cc56a697bb0000048/train/javascript)__
```javascript
function scramble(str1, str2) {
  const word = {};

  for(let i = 0; i < str1.length; i++) {
    if(!word[str1[i]]) {
      word[str1[i]] = 1;
    } else if (word[str1[i]]) {
      word[str1[i]]++;
    }
  }

  for (let i = 0; i < str2.length; i++) {
    if (word[str2[i]]) {
      word[str2[i]]--;
    } else {
      return false;
    }
  }
  return true;
}
```

* __[Valid Parentheses](https://www.codewars.com/kata/valid-parentheses/train/javascript/)__
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
