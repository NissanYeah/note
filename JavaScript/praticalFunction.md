# JavaScript

### Pratical Function 

Age           | Return or not  | Return value | 
--------------|:--------------:|------------------------
For           |      no        | X
ForEach       |      no        | X
Map           |  return array  | Return all values by processing in the array
Filter        |  return array  | Only return qualified values in the array
Find          |  return array  | Only return the first value that meets the condition in the array

### For

```JavaScript
for (let i=0; i<items.length; i++) {
  copy.push(items[i])
}
```


### ForEach

- Just like for, ForEach doesn't return value

```JavaScript
var arr = [1,2,3,4]
var result =[ ]
var result = arr.forEach(
  function(item) {
    return item. 
  }
) 
console.log(result) //undefined，beacause ForEach doesn't return value
```


```JavaScript
//coding Style 1 
var result =[ ]
arr.forEach(
  function(item) {
    result.push(item)
}) 
```
```JavaScript
//coding Style 2
var result =[ ]
arr.forEach( item => result.push(item)) 
```


### Map()

- Map only return `array`
- Map can get `item`&`index`
- It's available to custom data structure we need

``` JavaScript
var arr = [1,2,3,4]
var result = arr.Map( item=> item*2 ); 
// [2,4,6,8]
var result2 = arr.Map ((item, index)=> {
                  return { name: item, order: index+1 } 
                }) 
// [{name:1 , order:1},{name:2 , order:2},{name:3,order:3},{name:4 ,order:4}]
```

### Filter()

- Only return qualified values in the array

```JavaScript
var ele = [1,2,3,4]
var result = arr.filter( item=> item > 2); // [3,4]
```

### Find()

- Only return the first value that meets the condition in the array

```JavaScript
arr = [2,3,4,5]
found = arr.find( item => item > 2)
console.log(found);  // 3
```