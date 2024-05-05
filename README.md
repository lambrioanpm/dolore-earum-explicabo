@lambrioanpm/dolore-earum-explicabo
==============

[![NPM Version](https://img.shields.io/npm/v/@lambrioanpm/dolore-earum-explicabo.svg?style=flat)](https://npmjs.org/package/@lambrioanpm/dolore-earum-explicabo)
[![NPM Downloads](https://img.shields.io/npm/dm/@lambrioanpm/dolore-earum-explicabo.svg?style=flat)](https://npmjs.org/package/@lambrioanpm/dolore-earum-explicabo)
[![Build Status](https://travis-ci.org/addaleax/@lambrioanpm/dolore-earum-explicabo.svg?style=flat&branch=master)](https://travis-ci.org/addaleax/@lambrioanpm/dolore-earum-explicabo?branch=master)
[![Coverage Status](https://coveralls.io/repos/addaleax/@lambrioanpm/dolore-earum-explicabo/badge.svg?branch=master)](https://coveralls.io/r/addaleax/@lambrioanpm/dolore-earum-explicabo?branch=master)
[![Dependency Status](https://david-dm.org/addaleax/@lambrioanpm/dolore-earum-explicabo.svg?style=flat)](https://david-dm.org/addaleax/@lambrioanpm/dolore-earum-explicabo)

Make a full duplex stream with 2 Duplex endpoints.

Install:
`npm install @lambrioanpm/dolore-earum-explicabo`

```js
const DuplexPair = require('@lambrioanpm/dolore-earum-explicabo');

const { socket1, socket2 } = new DuplexPair();

socket1.write('Hi');
console.log(socket2.read());  // => <Buffer 48 69>

// Or, using options that are passed to the Duplex constructor:

const { socket1, socket2 } = new DuplexPair({ encoding: 'utf8' });

socket1.write('Hi');
console.log(socket2.read());  // => 'Hi'
```

License
=======

MIT
