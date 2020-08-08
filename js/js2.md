# Javascript promises



```javascript
const  doCall = () => {
 let  promise = new  Promise(function(resolve, reject) {
	 setTimeout(() =>  resolve("done!"), 1000);
    });
   return  promise
 }
 
 // resolve runs the first function in .then
 doCall().then(
    result  =>  log(result), // shows "done!"
    error  =>  log(error) // doesn't run
  );
    
 const  getCall = async () => {
  let  x = await  doCall()  
  log(x)
}

/* other example */
const add = (a, b) => {
return new Promise((resolve, reject) => {
setTimeout(() => {
if (a < 0 || b < 0) {
return reject('Numbers must be non-negative')
}
resolve(a + b)
}, 2000)
})
}


add(1, 2).then((sum) => {
console.log(sum) // Will print 3
return add(sum, 4)
}).then((sum2) => {
console.log(sum2) // Will print 7
}).catch((e) => {
console.log(e)
})

const doWork = async () => {
const sum = await add(1, 99)
const sum2 = await add(sum, 50)
const sum3 = await add(sum2, 3)
return sum3
}
doWork().then((result) => {
console.log('result', result)
}).catch((e) => {
console.log('e', e)
})
   
```
