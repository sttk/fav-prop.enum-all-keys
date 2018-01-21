# [@fav/prop.enum-all-keys][repo-url] [![NPM][npm-img]][npm-url] [![MIT License][mit-img]][mit-url] [![Build Status][travis-img]][travis-url] [![Build Status][appveyor-img]][appveyor-url] [![Coverage status][coverage-img]][coverage-url]

Lists enumerable own and inherited property keys of an object.

> "fav" is an abbreviation of "favorite" and also the acronym of "for all versions".
> This package is intended to support all Node.js versions and many browsers as possible.
> At least, this package supports Node.js >= v0.10 and major Web browsers: Chrome, Firefox, IE11, Edge, Vivaldi and Safari.


## Install

To install from npm:

```sh
$ npm install --save @fav/prop.enum-all-keys
```

***NOTE:*** *npm < 2.7.0 does not support scoped package, but even old version Node.js supports it. So when you use such older npm, you should download this package from [github.com][repo-url], and move it in `node_modules/@fav/prop.enum-all-keys/` directory manually.*


## Usage

For Node.js:

```js
var enumAllKeys = require('@fav/prop.enum-all-keys');
enumAllKeys({ a: 1, b: true, c: 'C' }); // => ['a', 'b', 'c' ]

function Fn() { this.a = 1; }
Fn.prototype.b = true;
var fn = new Fn();
Object.defineProperty(fn, 'c', { value: 'C' });
enumAllKeys(fn); // => ['a', 'b']
```

For Web browsers:

```html
<script src="fav.prop.enum-all-keys.min.js"></script>
<script>
var enumAllKeys = fav.prop.enumAllKeys;
enumAllKeys({ a: 1, b: true, c: 'C' }); // => ['a', 'b', 'c' ]
</script>
```


## API

### <u>enumAllKeys(obj) : Array</u>

Lists enumerable own and inherited property keys of the given object.

This function returns property keys enumerated with "for-in", but returns an empty array if *obj* is nullish.

#### Parameter:

| Parameter |  Type  | Description                                |
|-----------|:------:|--------------------------------------------|
| *obj*     | object | The object to be listed its property keys. |

#### Return:

An array of property keys.

**Type:** Array


## Checked                                                                      

### Node.js (4〜9)

| Platform  |   4    |   5    |   6    |   7    |   8    |   9    |
|:---------:|:------:|:------:|:------:|:------:|:------:|:------:|
| macOS     |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Windows10 |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|

### io.js (1〜3)

| Platform  |   1    |   2    |   3    |
|:---------:|:------:|:------:|:------:|
| macOS     |&#x25ef;|&#x25ef;|&#x25ef;|
| Windows10 |&#x25ef;|&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef;|&#x25ef;|

### Node.js (〜0.12)

| Platform  |  0.7   |  0.8   |  0.9   |  0.10  |  0.11  |  0.12  |
|:---------:|:------:|:------:|:------:|:------:|:------:|:------:|
| macOS     |        |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Windows10 |        |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|

### Web browsers

| Platform  | Chrome | Firefox | Vivaldi | Safari |  Edge  | IE11   |
|:---------:|:------:|:-------:|:-------:|:------:|:------:|:------:|
| macOS     |&#x25ef;|&#x25ef; |&#x25ef; |&#x25ef;|   --   |   --   |
| Windows10 |&#x25ef;|&#x25ef; |&#x25ef; |   --   |&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef; |&#x25ef; |   --   |   --   |   --   |


## License

Copyright (C) 2017 Takayuki Sato

This program is free software under [MIT][mit-url] License.
See the file LICENSE in this distribution for more details.

[repo-url]: https://github.com/sttk/fav-prop.enum-all-keys/
[npm-img]: https://img.shields.io/badge/npm-v1.0.0-blue.svg
[npm-url]: https://www.npmjs.com/package/@fav/prop.enum-all-keys
[mit-img]: https://img.shields.io/badge/license-MIT-green.svg
[mit-url]: https://opensource.org/licenses/MIT
[travis-img]: https://travis-ci.org/sttk/fav-prop.enum-all-keys.svg?branch=master
[travis-url]: https://travis-ci.org/sttk/fav-prop.enum-all-keys
[appveyor-img]: https://ci.appveyor.com/api/projects/status/github/sttk/fav-prop.enum-all-keys?branch=master&svg=true
[appveyor-url]: https://ci.appveyor.com/project/sttk/fav-prop-enum-all-keys
[coverage-img]: https://coveralls.io/repos/github/sttk/fav-prop.enum-all-keys/badge.svg?branch=master
[coverage-url]: https://coveralls.io/github/sttk/fav-prop.enum-all-keys?branch=master
