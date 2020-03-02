# solved-task
###Check the exam
```javascript
const checkExam = (arr1, arr2) => {
   const arr = arr2.reduce((total, responce, index) => {
     if(!responce) return total
     if(responce === arr1[index]) return total + 4
     if(responce !== arr1[index]) return total -1
     return total
   },0)
  return arr > 0 ? arr : 0
}
```
###Training JS #29: methods of arrayObject---concat() and join()
```javascript
function bigToSmall(arr){
  let result=[].concat(...arr).sort((a,b) => b - a).join('>')
  return result
}
```
###+1 Array
```javascript
function upArray(arr){
  if (!arr.every(v=>v>=0)||arr.length===0) return null
  
  if (arr.some(v=>v.toString().length>1)) return null
  let arr1 =[];
  for (let i=0;i<arr.length;i+=15){
  arr1.push(arr.slice(i,i+15))
  }
  arr1[arr1.length-1]= arr1[arr1.length-1].join('')*1+1
  arr1=arr1.map(v=>Array.isArray(v)?v.join('')*1:v)
  return (arr1.join('')).split('').map(v=>v*1)
}
```
### Training JS #34: methods of Math---pow() sqrt() and cbrt()
```javascript
const arr = n => Number.isInteger(Math.cbrt(n))
const cutCube = (volume,n) => arr(n) && arr(volume / n)
 
```
###CamelCase Method
```javascript

String.prototype.camelCase=function(){
  let arg = this.toString().trim().split(' ');
  let arr = arg.map((v,i,arr)=>v?v.slice(0,1).toUpperCase()+v.slice(1):v);
  return arr.join('');
}
```
###Autocomplete! Yay!
```javascript
function autocomplete(input, dictionary){
  input = input.replace(/[^a-zA-Z]/gi,"");
  let arr = [];
    for (i = 0; i < dictionary.length; i++){
      if(dictionary[i].slice(0, input.length).toLowerCase() === input.toLowerCase()){
        arr.push(dictionary[i])
      }
    }
  return arr.slice(0, 5)
}
```
###extract file name
```javascript
class FileNameExtractor {
    static extractFileName (dirtyFileName) {
        return dirtyFileName.match(/\d+_.+\..+\./).join``.replace(/^\d+_/,'').replace(/\.$/,'')
    }
}
```
###A Taste of Curry
```javascript
function curry(fun, ...arr) {
  return function (...arr2){
    return fun.call(this,...arr, ...arr2)
  };
}
```
###Array#reduce
```javascript
Array.prototype.reduce = function(process, initial) {
  for (let i = 0; i < this.length; i++) {
    if (!initial){i++;initial=this[0]}
    initial =  process(initial, this[i]);
 }
 return initial
}
```
###Arabian String
```javascript
const camelize = str => str.replace(/[^a-z0-9]/gi, " ").split` `.map
(el => el.slice(0, 1).toUpperCase() + el.slice(1).toLowerCase()).join``;
```
###Arguments to Binary addition
```javascript
function arr2bin(arr){
 let sum = 0;
   for (let i =0; i < arr.length; i++){
     if(typeof arr[i] === 'number'){
       sum += arr[i]
     }
   }
   return sum.toString(2)
  }

```
###Area or Perimeter
```javascript
const areaOrPerimeter = function(l , w) {
  if (l === w) return l * w
  else return (l + w) * 2
};
```
###A Memory game array
```javascript
function createTiles(n){
  if (n % 2 !==0) return [];
  const arr = [];
  for (let i = 1; i<=n /2; i++){
    arr.push(i)
    arr.push(i)
  }
  return arr.slice(0,1).concat(arr.slice(1).sort((a, b) => Math.round(Math.random())))
}
```
###Difference of 2
```javascript
function twosDifference(input){
   input = input.sort((a, b) => a - b);
   const arr = [];
   for (let i =0; i < input.length; i++){
   for (let j = i + 1; j < input.length; j++){
   if(Math.abs(input[i] - input[j]) === 2){
     arr.push([input[i], input[j]]);
     break;
      }
     }
   }
   return arr;
}
```
###Arrh, grabscrab!
```javascript
function grabscrab(anag, dict) {
  const result = anag.split('').sort().join('')
  const arr = [];
  
  for (let item of dict){
    itemSorted = item.split('').sort().join('')
      if (itemSorted === result) {
        arr.push(item)
    }
  }
  return arr
}
```
###What's Your Poison?
```javascript
const find = rats => rats.reduce((a,b) => a + Math.pow(2, b),0)
```
###Are they the "same"?
```javascript
function comp(array1, array2){
  if(!array1 || !array2 || array1.length !== array2.length) return false;
  return array1.map(el => el * el).sort().toString() === array2.sort().toString()
}
```
###Playing with cubes II
```javascript
function Cube(n) {
  var side = 0;
  
  this.getSide = function() { return side; };
  this.setSide = function(n) {
    if (isNaN(n) === true) { return; }
    side = Math.abs(n);
  };
};
```
###sPoNgEbOb MeMe
```javascript
function spongeMeme(str) {
  let arr = '';
  for (let i = 0; i < str.length; i++){
    arr += (i % 2) ? str[i].toLowerCase() : str[i].toUpperCase();
    }
    return arr
}
```
###Valid Parentheses
```javascript
function validParentheses(str){
 const arr = str.split('');
 let a = 0;
   for (let i =0; i < arr.length; i++){
   if (arr[i] === '(') a = a + 1;
   else if(arr[i] === ')') a= a - 1;
   if(a < 0) return false;
   }
   if(a === 0) return true;
   else return false;
}
```
###Arrays Similar
```javascript
function arraysSimilar(arr1, arr2) {
  return JSON.stringify(arr1.sort()) === JSON.stringify(arr2.sort())
}
```
###Remove duplicate words
```javascript
const removeDuplicateWords = s => arr = Array.from(new Set(s.split(' '))).join(' ');
```
### Leonardo Dicaprio and Oscars
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
   