
# escape-html-unicode

  Escape string for use in JavaScript or React

This module exports a single function, `escapeHtml`, that is used to escape
a string of content such that it can be interpolated in HTML content.

This module will escape the following characters: `"`, `'`, `&`, `<`, and `>`
to their unicode escape code. (\u0022, ...).

## Example

```js
var escapeHtml = require('escape-html-unicode');
var html = escapeHtml('foo & bar');
// -> foo \u0026 bar
```

## Benchmark

```
$ yarn run bench
yarn run v0.21.3
$ node benchmark/index.js 

  http_parser@2.7.0
  node@7.7.1
  v8@5.5.372.41
  uv@1.11.0
  zlib@1.2.11
  ares@1.10.1-DEV
  modules@51
  openssl@1.0.2k
  icu@58.2
  unicode@9.0
  cldr@30.0.3
  tz@2016j


  3 tests completed.

  no special characters    x 23,021,340 ops/sec ±2.07% (187 runs sampled)
  single special character x  8,321,581 ops/sec ±0.78% (188 runs sampled)
  many special characters  x  2,974,007 ops/sec ±0.81% (188 runs sampled)

✨  Done in 33.35s.
```

## License

  MIT
