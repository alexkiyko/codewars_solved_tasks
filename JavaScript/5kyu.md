### Code challenges 5 kyu

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
