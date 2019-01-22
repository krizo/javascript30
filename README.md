# javascript30

My code and notes on [javascript30](https://javascript30.com/) course.

## 01 - Drumkit

##### Make a window (or other element) reacting on key pressing

`window.addEventListener('keydown', function_to_be_called)`

##### Find elements of `key` class

`const keys = document.querySelectorAll('.key');`

##### Find only first matching element with custom selector

`const key = document.querySelector(`.key[data-key="${e.keyCode}"`)`

##### Find and play audio element
```
const audio = document.querySelector(`audio`)
audio.play();
```

##### Add/remove class attribute

```
audio.classList.add('playing')
//...
audio.classList.remove('playing')
``` 

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

## 03 - Playing with CSS variaqbles and JS

##### Declaring CSS variables

```
:root {
      --base: #ffc600;
      --spacing: 10px;
      --blur: 10px;
    }
```

##### Using CSS variables
```
img {
    padding: var(--spacing);
    spacing: var(--base);
    filter: blur(var(--blur));
}  
```  

##### Selecting specific element types (inputs) of specific class ('.controls')

```const inputs = document.querySelectorAll('.controls input');``` 


##### List all element's `data-` attributes

``` 
const inputs = document.querySelectorAll('.controls input');
inputs.forEach(input => console.log(input.dataset));
```
 
##### Updating CSS variables via JS

``` 
function handleUpdate() {
    const suffix = this.dataset.sizing || '';
    document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
}

inputs.forEach(input => input.addEventListener('change', handleUpdate));
inputs.forEach(input => input.addEventListener('mousemove', handleUpdate));```

