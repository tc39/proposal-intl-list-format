## Intl.ListFormat API Specification [draft]

### Status

__Stage 0__

Implementation Progress

 * Polyfill: https://github.com/zbraniecki/IntlListFormat

Backpointers

* https://github.com/tc39/ecma402/issues/34
* https://groups.google.com/forum/#!topic/javascript-globalization/3nFDf5al5hU

### Authors

 * Zibi Braniecki (@zbraniecki)

### Reviewers

TBD

### Informative

This proposal is based on the LDML spec, C.11 Language Plural Rules:


### Prior Art


### Usage

```javascript
let o = new Intl.ListFormat("en", {
    style: "regular" // default style
});
console.log(o.format(['foo', 'bar', 'baz']); // "foo, bar, and baz"
```

### Render Spec

```bash
npm install
npm run build
open index.html
```
