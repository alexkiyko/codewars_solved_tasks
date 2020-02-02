### Code challenges 5 kyu

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
