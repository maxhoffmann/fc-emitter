Emitter
=======

Event emitter implementation using the “frozen closure” pattern as [described by Douglas Crockford](http://www.ustream.tv/recorded/46640057). Heavily inspired by [component/emitter](https://github.com/component/emitter).

Browser support: ES5 compatible browsers (IE9+)

Installation
------------

```bash
npm install maxhoffmann/emitter --save
```

Usage
-----

```js
var emitter = Emitter();

emitter.on('eventName', listener);
emitter.once('eventName', listener); // only listen once

emitter.off('eventName', listener); // remove specific listener
emitter.off('eventName'); // remove all listeners of this event
emitter.off(); // remove all listeners

emitter.trigger('eventName', arg1, arg2…); // arguments are optional

emitter.hasListeners('eventName');

emitter.hasListeners(); // throws an error (not yet implemented)
```

Testing
-------

- `cd` into directory
- run `npm test`

LICENSE
-------

The MIT License
