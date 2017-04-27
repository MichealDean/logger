
# koa-logger-md

[![npm version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]

 Development style logger middleware for [koa](https://github.com/koajs/koa).

___Notice: `koa-logger@2` supports `koa@2`; if you want to use this module with `koa@1`, please use `koa-logger@1`.___

```
[2017-04-27T09:18:01.344Z]<-- GET /
[2017-04-27T09:18:02.344Z]--> GET / 200 835ms 746b
[2017-04-27T09:18:03.344Z]<-- GET /
[2017-04-27T09:18:04.344Z]--> GET / 200 960ms 1.9kb
[2017-04-27T09:18:05.344Z]<-- GET /users
[2017-04-27T09:18:06.344Z]--> GET /users 200 357ms 922b
[2017-04-27T09:18:07.344Z]<-- GET /users?page=2
[2017-04-27T09:18:09.344Z]--> GET /users?page=2 200 466ms 4.66kb
```

## Installation

```js
$ npm install koa-logger-md
```

## Example

```js
const logger = require('koa-logger-md')
const Koa = require('koa')

const app = new Koa()
app.use(logger())
```

## Notes

  Recommended that you `.use()` this middleware near the top
  to "wrap" all subsequent middleware.

## License

  MIT

[npm-image]: https://img.shields.io/npm/v/koa-logger.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/koa-logger
[travis-image]: https://img.shields.io/travis/koajs/logger.svg?style=flat-square
[travis-url]: https://travis-ci.org/koajs/logger
