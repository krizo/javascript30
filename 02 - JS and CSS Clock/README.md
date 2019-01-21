## 02 - JS and CSS Clock

##### Rotate an element by 90 degrees from the right side end (CSS):
```
transform: rotate(90deg);
transform-origin: 100%;
``` 

##### Simulate tick effect (CSS)
```
transition: all 0.05s;
transition-timing-function: cubic-bezier(0.1, 2.7, 0.58, 1); 
```

##### Calling function each second
```
setInterval(my_function, 1000)
```

##### Rotate element via js
```
const secondHand = document.querySelector('.second-hand')
const seconds = now.getSeconds();
const secondsDegree = ((seconds / 60) * 360) + 90; // 90 -offset
secondHand.style.transform = `rotate(${secondsDegree}deg)`;
```
