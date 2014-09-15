# keanu
[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][coveralls-image]][coveralls-url]

A CommonJS adaptation of [keymaster](https://github.com/madrobby/keymaster).
Define and dispatch keyboard shortcuts.

## Installation
```bash
$ npm i --save keanu
```

## Overview
```js
// define short of 'a'
key('a', function(){ alert('you pressed a!') });

// returning false stops the event and prevents default browser events
key('ctrl+r', function(){ alert('stopped reload!'); return false });

// multiple shortcuts that do the same thing
key('⌘+r, ctrl+r', function(){ });
```

## API
#### key(key)
Register a key.
```js
// define short of 'a'
key('a', function(){ alert('you pressed a!') });

// returning false stops the event and prevents default browser events
key('ctrl+r', function(){ alert('stopped reload!'); return false });

// multiple shortcuts that do the same thing
key('⌘+r, ctrl+r', function(){ });
```

#### key.unbind(key)
Unbind a bound key.
```js
// unbind 'a' handler
key.unbind('a');
```

## License
[MIT](https://tldrlegal.com/license/mit-license) ©
[Yoshua Wuyts](yoshuawuyts.com)

[npm-image]: https://img.shields.io/npm/v/keanu.svg?style=flat-square
[npm-url]: https://npmjs.org/package/keanu
[travis-image]: https://img.shields.io/travis/yoshuawuyts/keanu.svg?style=flat-square
[travis-url]: https://travis-ci.org/yoshuawuyts/keanu
[coveralls-image]: https://img.shields.io/coveralls/yoshuawuyts/keanu.svg?style=flat-square
[coveralls-url]: https://coveralls.io/r/yoshuawuyts/keanu?branch=master
