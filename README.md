# salved-tasks

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
   