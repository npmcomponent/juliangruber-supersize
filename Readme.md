*This repository is a mirror of the [component](http://component.io) module [juliangruber/supersize](http://github.com/juliangruber/supersize). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/juliangruber-supersize`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# supersize

  make text as big as possible in its parent element.

```js
var supersize = require('supersize');
var el = document.querySelector('#el');
  
window.addEventListener('resize', supersize(el));
```
  
  check out the [demo](http://juliangruber.github.com/supersize).

## Installation

    $ component install juliangruber/supersize

## API

### supersize(el[, max=0.66])

  Make the inner text of `el` as big as possible while `el` still stays in the
  bounds of its parent element.
  
  **!!** the element's parent needs to have `position:relative` or
  `position:absolute`. 
  
  The factor `max` limits the maximum possible size. If you want the text to
  take all available space, set `max` to `1`.
  
  This returns a function that calls `supersize` again with the same
  arguments. This way you can execute it immediately and pass it as an event
  listener in one line:
  
```js
window.addEventListener('resize', supersize(el));
// scales now and on resize
```

## License

  MIT
