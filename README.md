# salved-tasks

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
   