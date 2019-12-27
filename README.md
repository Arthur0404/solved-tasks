# salved-tasks

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
   