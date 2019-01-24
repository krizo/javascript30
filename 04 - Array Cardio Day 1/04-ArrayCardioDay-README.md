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

Sort items by comparing two items and "bubbling up" greater/lesser ones to the top

```javascript
const order = inventors.sort( (a, b) => a.year > b.year ? 1 : -1)
```

##### Reduce

Iterate through an array and manipulate with a starting value and all array's elements to calculate end result 

```javascript
const totalYears = inventors.reduce((total, inventor) => {
      return total + (inventor.passed - inventor.year);
    }, 0); // 0 -> number which total is starting from
```

Starting value can be also an object. Example for counting words by category:

```javascript
const data = ['car', 'car', 'truck', 'truck', 'bike', 'walk', 'car', 'van', 'bike', 'walk', 'car', 'van', 'car', 'truck' ];

     const transportation = data.reduce((obj, item) => {
       if (!obj[item] ) {
         obj[item] = 0;
       }
       obj[item]++;
       return obj;
     }, {})
```