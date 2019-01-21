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