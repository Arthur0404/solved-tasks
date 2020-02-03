# salved-task
###Leonardo Dicaprio and Oscars
```javascript
  if (oscar === 88)return "Leo finally won the oscar! Leo is happy"
  if(oscar === 86)return "Not even for Wolf of wallstreet?!"
  if (oscar === 88 || oscar === 86 || oscar < 88) return  "When will you give Leo an Oscar?"
  if (oscar > 88) return "Leo got one already!"
}
```
###Price of Mangoes
   ```javascript
function mango(quantity, price){
  const arr = Math.floor(quantity / 3)
  return (quantity - arr) * price
}
```
###Did she say hallo?
```javascript
function validateHello(greetings) {
    return /(hello|ciao|salut|hallo|hola|ahoj|czesc)/i.test(greetings)
  }
```
###Training JS #6: Basic data types--Boolean and conditional statements if..else
```javascript
const trueOrFalse = val => (val ? 'true' : 'false')
```
###Stop gninnipS My sdroW!
```javascript
const spinWords = str => str.split(' ').map(el => el.length > 4 ? el.split('').reverse().join('') : el).join(' ')
```
###Grasshopper - Basic Function Fixer
```javascript
function addFive(num) {
  const total = num + 5
  return total
}
```
###Simple Fun #261: Whose Move
```javascript
function whoseMove(lastPlayer, win) {
  if (lastPlayer === 'black' && win === false) return 'white'
  if (lastPlayer === 'white' && win === true) return 'white'
  else return 'black'
}
```

###pick a set of first elements
```javascript
const first = (arr, n =1) => arr.slice(0, n)
```
### Contamination #1 -String-
```javascript
function contamination(text, char){
  return char.repeat(text.length)
}
```
###How many times should I go?
```javascript
function howManyTimes(annualPrice, individualPrice) {
  return Math.ceil(annualPrice / individualPrice)
}
```

###Exclamation marks series #4: Remove all exclamation marks from sentence but ensure a exclamation mark at the end of string
```javascript
const remove = s  =>`${s.replace(/!+/g, '')}!`  
```

###Training JS #7: if..else and ternary operator
```function saleHotdogs(n){
   if (n < 5 ) {
   return n * 100
   }
    else if (n >= 5 && n < 10){
    return n * 95
    }
    else if (n >= 10){
    return n * 90}
   }```
###Multiplication table for number
```javascript
function multiTable(number) {
  let arr = '';
  for (let i = 1; i <=10;i++){
    if(i === 10){
      arr += `${i} * ${number} = ${i * number}`
      break;
    }
    arr += `${i} * ${number} = ${i * number}\n`
}
  return arr
}
```
###USD => CNY
```javascript
function usdcny(usd) {
  return `${(usd * 6.75).toFixed(2)} Chinese Yuan`
}
```

###Twice as old
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs(dadYearsOld - sonYearsOld * 2)
}
```
###They say that only the name is long enough to attract attention. They also said that only a simple Kata will have someone to solve it. This is a sadly story #1: Are they opposite?
```javascript
function isOpposite(s1,s2){
  if( s1 === s2 || s1.toLowerCase() !== s2.toLowerCase()) return false
  for (let i =0; i < s1.length; i++){
  if(s1.charAt(i) === s2.charAt(i)) return false
  }
   return true
}
```
###Enumerable Magic #3 - Does My List Include This?
```javascript
function include(arr, item){
  return arr.includes(item);
}
```
###BASIC: Making Six Toast.
```javascript
function sixToast(num) {
  return Math.abs(num -6)
}

```
###Regexp Basics - is it a digit?
  ```javascript
 String.prototype.digit = function() {
    return /^\d$/g. test(this)
  }
```
###Permute a Palindrome
```javascript
function permuteAPalindrome(input) {
  let count = 0;
  const dict = input.split('').reduce((acc, curr) => ((acc[curr] = acc[curr] ? acc[curr] + 1 : 1), acc),
    {}
  );
  for (let i in dict) {
    if (dict[i] % 2 !== 0) {
      count++;
    }
    if (count === 2) return false;
  }
  return true;
}
```
###Find the position!
```javascript
function position(letter){
  return `Position of alphabet: ${letter.charCodeAt() - 96}`
}
```
###Numbers to Letters
```javascript
function switcher(x){
  return x.reduce((word, number) => `${word}${' ?!abcdefghijklmnopqrstuvwxyz'[29 - number]}`, '')
  }
```

###5 without numbers !!
```javascript
function unusualFive() {
   let arr = 'hello';
   return arr.length;
}
```
###Train to remove duplicates from an array with filter()
```javascript
function unique(arr) {
  const a = arr.filter((el,i) => i === arr.indexOf(el))
  return a;
}
```
###Be Concise IV - Index of an element in an array
```javascript
const find = (array, element) => array.includes(element) ? array.indexOf(element) : "Not found";
```
###A wolf in sheep's clothing
```javascript
function warnTheSheep(queue) {
  const arr = queue.indexOf('wolf')
  return arr === queue.length-1 ? "Pls go away and stop eating my sheep"
  :`Oi! Sheep number ${queue.length-1-arr}! You are about to be eaten by a wolf!`
}
```
###How good are you really?
```javascript
function betterThanAverage(classPoints, yourPoints) {
  let arr = 0;
  for (let i =0; i <classPoints.length;i++)
  arr += classPoints[i];
  let result = arr / classPoints.length;
  if (result <= yourPoints)return true;
  else return false;
}
```

###L1: Set Alarm
```javascript
function setAlarm(e, v){
  return e && !v;
}
```

###What is type of variable?
```javascript
function type(value) {
    if(value instanceof Array) return 'array'
    if (value instanceof Date) return 'date'
    if (value instanceof Object) return 'object'
    if (value === null) return 'null'
    return typeof value;
  }
```

###Is every value in the array an array?
```javascript
function arrCheck (value){
for (let i =0; i < value.length;i++) {
 if (!Array.isArray(value[i])) return false;
 }
return true;
 }
```
###Squares sequence
```javascript
function squares(x, n) {
  let arr = [];
  n > 0 ? arr.push(x) : arr;
  for (let i =1;i < n; i++)
  arr.push(Math.pow(arr[i -1],2))
     return arr;
}
```
###Alan Partridge II - Apple Turnover
```javascript
function apple(x){
if (x ** 2 >1000) return 'It\'s hotter than the sun!!';
else return 'Help yourself to a honeycomb Yorkie for the glovebox.';
}
```
###Is integer safe to use?
```javascript
function SafeInteger(n) {
 if (Number.isSafeInteger(n)) return true;
 else return false;
 
}
```



###isReallyNaN
```javascript
const isReallyNaN = (val) => {
  return Number.isNaN(val);  
  return true || false;
};

```






### Factorial
```javascrip 
function factorial(n){
 
  return (n != 0) ? n * factorial(n - 1) : 1;

}
```
#### Can we divide it?;
function isDivideBy(number, a, b) {
 return number % a === 0 && number % b === 0;
}

### Power of two;
function isPowerOfTwo(n){
  return !(n & (n - 1)) && n != 0;
}
```
   