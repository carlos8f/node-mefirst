node-mefirst
============

Attach an event listener to run first.

Usage
-----

```javascript
var EventEmitter = require('events').EventEmitter
  , emitter = new EventEmitter
  , mefirst = require('mefirst')

emitter.on('something', function() {
  console.log('i ran');
});

mefirst(emitter, 'something', function() {
  console.log('i ran first!');
});

emitter.emit('something');
```

```
i ran first!
i ran
```

License
-------

MIT