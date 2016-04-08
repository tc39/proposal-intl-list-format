## Intl.ListFormat API Specification [draft]

### Status

__Stage 1__

Implementation Progress

 * Polyfill: https://github.com/zbraniecki/IntlListFormat

Backpointers

* https://github.com/tc39/ecma402/issues/33
* http://cldr.unicode.org/translation/lists
* http://unicode.org/reports/tr35/tr35-general.html#ListPatterns

### Authors

 * Zibi Braniecki (@zbraniecki)

### Reviewers

TBD

### Informative

This proposal is based on the LDML spec, List Patterns:


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
