
# Javascript

### Notes


```javascript

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
```