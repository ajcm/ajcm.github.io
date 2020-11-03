
# Javascript

### Notes


```javascript

/* parse object entries */
Object.entries(obj)

/* Check Object Empy */
Object.keys(obj).length === 0 && obj.constructor === Object


/* check if Array */
Array.isArray(obj)

/* check if Array not Empty */
if (Array.isArray(array) && array.length) {
    // array exists and is not empty
}

   
```


#### Use Reducers
```javascript
['a','b'].reduce(function(result, item, index, array) {
  result[item] = item; //a, b, c
  return result;
}, {})

/* example */
var result = list.reduce((acc,item) => {
      acc.push(item)
      return acc
    },[])

```

#### For each
```javascript
arr.forEach(callback(currentValue[, index[, array]]) {
  // execute something
}[, thisArg]);

/* async */
ratings.forEach(async function(rating) {
  sum = await sumFunction(sum, rating)
})


/* with arrow */
someValues.forEach((element, index) => {
    console.log(`Current index: ${index}`);
    console.log(element);
});

```

#### Array.find
```javascript
let result = arr.find(function(item, index, array) {
  // if true is returned, item is returned and iteration is stopped
  // for falsy scenario returns undefined
});

ex:
let user = users.find(item => item.id == 1);

```