# eslint-formatter-codeframe

> ESLint’s official `codeframe` formatter, extracted from ESLint 7

This formatter has been removed from ESLint 8 so it lives as a standalone module here.

**Warning:** This module is not maintained. If you're an ESLint contributor or dependable open-sourcerer, open an issue here and I'll pass you this repo and npm name. You can also ping me on Twitter [@fregante](https://twitter.com/fregante)

## Install

```sh
npm install --save-dev eslint-formatter-codeframe
```

## Usage

More information about formatters can be found on https://eslint.org/docs/user-guide/formatters/

```
eslint --format codeframe
```

## Example output

```
error: 'addOne' is defined but never used (no-unused-vars) at fullOfProblems.js:1:10:
> 1 | function addOne(i) {
    |          ^
  2 |     if (i != NaN) {
  3 |         return i ++
  4 |     } else {


error: Use the isNaN function to compare with NaN (use-isnan) at fullOfProblems.js:2:9:
  1 | function addOne(i) {
> 2 |     if (i != NaN) {
    |         ^
  3 |         return i ++
  4 |     } else {
  5 |       return


error: Unexpected space before unary operator '++' (space-unary-ops) at fullOfProblems.js:3:16:
  1 | function addOne(i) {
  2 |     if (i != NaN) {
> 3 |         return i ++
    |                ^
  4 |     } else {
  5 |       return
  6 |     }


warning: Missing semicolon (semi) at fullOfProblems.js:3:20:
  1 | function addOne(i) {
  2 |     if (i != NaN) {
> 3 |         return i ++
    |                    ^
  4 |     } else {
  5 |       return
  6 |     }


warning: Unnecessary 'else' after 'return' (no-else-return) at fullOfProblems.js:4:12:
  2 |     if (i != NaN) {
  3 |         return i ++
> 4 |     } else {
    |            ^
  5 |       return
  6 |     }
  7 | };


warning: Expected indentation of 8 spaces but found 6 (indent) at fullOfProblems.js:5:1:
  3 |         return i ++
  4 |     } else {
> 5 |       return
    | ^
  6 |     }
  7 | };


error: Function 'addOne' expected a return value (consistent-return) at fullOfProblems.js:5:7:
  3 |         return i ++
  4 |     } else {
> 5 |       return
    |       ^
  6 |     }
  7 | };


warning: Missing semicolon (semi) at fullOfProblems.js:5:13:
  3 |         return i ++
  4 |     } else {
> 5 |       return
    |             ^
  6 |     }
  7 | };


error: Unnecessary semicolon (no-extra-semi) at fullOfProblems.js:7:2:
  5 |       return
  6 |     }
> 7 | };
    |  ^


5 errors and 4 warnings found.
2 errors and 4 warnings potentially fixable with the `--fix` option.
```

## Links

- [Other official ESLint formatters as standalone modules](https://github.com/fregante/eslint-formatters)

