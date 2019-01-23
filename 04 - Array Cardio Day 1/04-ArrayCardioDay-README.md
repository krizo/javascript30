## 04 - Array Cardio Day

##### Filter array 

Use `filter` function to keep the elements of the array which fulfill condition

```javascript
const fifteen = inventors.filter(function(inventor) {
  if (inventor.year >= 1500 && inventor.year < 1600) return true //keep it!
})
```

##### Map 

Iterate through all items in the array, change them and produce the other array with the same length asd original

```javascript
const fullNames = inventors.map(inventor => `${inventor.first} ${inventor.last}`)
```

##### Sort

Sort items by comparing two items and "bubbling" greater/lesser ones to the top

```javascript
const order = inventors.sort( (a, b) => a.year > b.year ? 1 : -1)
```