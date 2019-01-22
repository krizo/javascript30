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