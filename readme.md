# better-body [![NPM version][npmjs-shields]][npmjs-url] [![Build Status][travis-img]][travis-url] [![Dependency Status][depstat-img]][depstat-url] [![Coveralls][coveralls-shields]][coveralls-url]
> A koa body parser middleware with support for `multipart`, `json`, `csp-report` or `urlencoded` request bodies. Via formidable and co-body.


## Install [![Nodei.co stats][npmjs-install]][npmjs-url]
> Install with [npm](https://npmjs.org)

```
$ npm install koa-better-body
$ npm test
```


## Usage
> For a more comprehensive examples, see [examples](./examples) folder.

- [`examples/multer`](./examples/multer.js) - usage like Express's bodyParser - [multer][multer-url] `npm run examples-multer`
- [`examples/koa-router`](./examples/koa-router.js) - usage with Alex's [koa-router][koa-router-url] `npm run examples-koa-router`


## [.koaBetterBody](index.js#L45)
> However, `koa-better-body` have few custom options, see also [co-body][cobody-url], [raw-body][rawbody-url], [formidable][formidable-url]

* `[options]` **{Object}**  
  - `patchNode` **{Boolean}** Patch request body to Node's `ctx.req` object, default `false`
  - `patchKoa` **{Boolean}** Patch request body to Koa's `ctx.request` object, default `true`
  - `jsonLimit` **{String|Number}** The byte limit of the JSON body, default `1mb`
  - `formLimit` **{String|Number}** The byte limit of the form body, default `56kb`
  - `encoding` **{String}** Sets encoding for incoming form fields, default `utf-8`
  - `multipart` **{Boolean}** Support `multipart/form-data` request bodies, default `false`
  - `fieldsKey` **{String|Boolean}** Name of the key for fields in the body object or `false`, default `'fields'`
  - `formidable` **{Object}** Options that are passing to `formidable`
    + `formidable.maxFields` **{Number}** See [formidable-options](./readme.md#formidable-options). our default `10`
    + `formidable.multiples` **{Boolean}** See [formidable-options](./readme.md#formidable-options), our default `true`
    + `formidable.keepExtensions` **{Boolean}** See [formidable-options](./readme.md#formidable-options), our default `true`
* `return` **{GeneratorFunction}** That you can use with [koa][koa-url] or [co][co-url]

### formidable options
> See [node-formidable][formidable-url] for a full list of options

- `bytesExpected` **{Integer}** The expected number of bytes in this form, default `null`
- `maxFields` **{Integer}** Limits the number of fields that the querystring parser will decode, default `1000`
- `maxFieldsSize` **{Integer}** Limits the amount of memory a field can allocate _in bytes_, default `2mb`
- `uploadDir` **{String}** Sets the directory for placing file uploads in, default `os.tmpDir()`
- `hash` **{String}** If you want checksums calculated for incoming files - `'sha1'` or `'md5'`, default `false`
- `multiples` **{Boolean}** Multiple file uploads or no, default `false`


## Authors & Contributors 
**Charlike Make Reagent** [![author tips][author-gittip-img]][author-gittip]
+ [gittip/tunnckoCore][author-gittip]
+ [github/tunnckoCore][author-github]
+ [twitter/tunnckoCore][author-twitter]
+ [npmjs/tunnckoCore][author-npmjs]


## License [![MIT license][license-img]][license-url]
Copyright (c) 2014 [Charlike Make Reagent][author-website], [contributors](https://github.com/tunnckoCore/koa-better-body/graphs/contributors).  
Released under the [`MIT`][license-url] license.

[npmjs-url]: http://npm.im/koa-better-body
[npmjs-shields]: http://img.shields.io/npm/v/koa-better-body.svg
[npmjs-install]: https://nodei.co/npm/koa-better-body.svg?mini=true

[coveralls-url]: https://coveralls.io/r/tunnckoCore/koa-better-body?branch=master
[coveralls-shields]: https://img.shields.io/coveralls/tunnckoCore/koa-better-body.svg

[license-url]: https://github.com/tunnckoCore/koa-better-body/blob/master/license.md
[license-img]: http://img.shields.io/badge/license-MIT-blue.svg

[travis-url]: https://travis-ci.org/tunnckoCore/koa-better-body
[travis-img]: https://travis-ci.org/tunnckoCore/koa-better-body.svg?branch=master

[depstat-url]: https://david-dm.org/tunnckoCore/koa-better-body
[depstat-img]: https://david-dm.org/tunnckoCore/koa-better-body.svg

[author-gittip-img]: http://img.shields.io/gittip/tunnckoCore.svg
[author-gittip]: https://www.gittip.com/tunnckoCore
[author-github]: https://github.com/tunnckoCore
[author-twitter]: https://twitter.com/tunnckoCore

[author-website]: http://www.whistle-bg.tk
[author-npmjs]: https://npmjs.org/~tunnckocore

[cobody-url]: https://github.com/visionmedia/co-body
[mocha-url]: https://github.com/visionmedia/mocha
[rawbody-url]: https://github.com/stream-utils/raw-body
[multer-url]: https://github.com/expressjs/multer
[koa-router-url]: https://github.com/alexmingoia/koa-router
[koa-url]: https://github.com/koajs/koa
[formidable-url]: https://github.com/felixge/node-formidable
[co-url]: https://github.com/visionmedia/co
[extend-url]: https://github.com/justmoon/node-extend
[csp-report]: https://mathiasbynens.be/notes/csp-reports
