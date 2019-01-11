# `Intl.ListFormat` API Specification [draft]  

## Overview

The `Intl.ListFormat` object is a constructor for objects that enable language-sensitive list formatting. 

### Usage example

The following example shows how to create a formatted list using the English language.


```js
// Create a list formatter in your locale
// with default values explicitly passed in.
const lf = new Intl.ListFormat("en", {
    localeMatcher: "best fit", // other values: "lookup"
    type: "conjunction", // "conjunction", "disjunction" or "unit"
    style: "long", // other values: "short" or "narrow"
});

lf.format(['Motorcycle', 'Truck' , 'Car']);
// > "Motorcycle, Truck, and Car"
```

 >  When style is `narrow`, `unit` is the only allowed value for the type option


### Implementation Status

__Stage 3__

Implementation Progress

* Polyfill: https://github.com/zbraniecki/IntlListFormat

Backpointers

* https://github.com/tc39/ecma402/issues/33
* http://cldr.unicode.org/translation/lists
* https://unicode.org/reports/tr35/tr35-general.html#ListPatterns

### Authors

 * Zibi Braniecki (@zbraniecki)

### Reviewers

 * Jamund Ferguson (@xjamundx)
 * Daniel Ehrenberg (@littledan)

### Informative

This proposal is based on the LDML spec, List Patterns:


## Proposal


### Spec

You can view the [spec text](spec/listformat.html).


### API

#### `Intl.ListFormat([locales[, options]])`

The `Intl.ListFormat` object is a constructor for objects that enable language-sensitive list formatting.

#### `locales`

Optional. A string with a BCP 47 language tag, or an array of such strings. For the general form and interpretation of the `locales` argument, see the [`Intl` page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl#Locale_identification_and_negotiation).

#### `options`

Optional. An object with some or all of the following properties:

##### `localeMatcher`

The locale matching algorithm to use. Possible values are `"lookup"` and `"best fit"`; the default is `"best fit"`. For information about this option, see the  [`Intl` page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl#Locale_negotiation).

##### `type`


The format of output message. Possible values are  `"conjunction"` that stands for for "and"-based lists (default, e.g., `A, B, and C`), or `"disjunction"` that stands for "or"-based lists (e.g., `A, B, or C`). `"unit"` stands for lists of values with units (e.g., `5 pounds, 12 ounces`).


##### `style`

The length of the formated message. Possible values are: `"long"` (default, e.g., `A, B, and C`); `"short"` or `"narrow"` (e.g., `A, B,C`). when style is `narrow`, `unit` is the only allowed value for the type option.


## Development

### Render Spec

```
npm install
npm run build
open out/index.html
```

## Links

 * [MDN Documentation link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ListFormat) 