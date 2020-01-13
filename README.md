# salved-task

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
   