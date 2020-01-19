[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![](https://img.shields.io/npm/v/birthgem.svg)](https://www.npmjs.com/package/birthgem)

# Birthgem

Determines the birthstones from the given month, day of the week or zodiac sign.

*This is based on ekimng's [package](https://github.com/ekimng/birthstone).*

- The stone names and zodiac signs names can be in different languages.
- All results are returned into an array except for error codes which are negative integers.

## Installation

You have to add this module to your npm modules folder.

```bash
$ npm install birthgem
```

## Example

### Importing the module

```js
const birthgem = require('birthgem')('en');
// Require with a language (format xx-YY sets (format xx)
const birthgem = require('birthgem')('en-US')
// Require without an argument sets 'en'
const birthgem = require('birthgem')();
```

### Displaying a month birthstone

```js
// Returns the birthstone of the present month
console.log(birthgem.month());
// Returns the birthstone of January (values: [1;12])
console.log(birthgem.month(1));
// Overload the default language (format xx-YY sets (format xx)
console.log(birthgem.month(1, 'fr'));
```

### Displaying a day of the week birthstone

```js
// Returns the birthstone of the present day
console.log(birthgem.day());
// Returns the birthstone of Monday (values: [1;7])
console.log(birthgem.day(1));
// Overloads the default language (format xx-YY sets (format xx)
console.log(birthgem.day(1, 'fr'));
```

### Displaying a zodiac sign birthstone

```js
// Returns the birthstone of the zodiac sign Aries (values: zodiac signs names and symbols)
console.log(birthgem.zodiac('aries'));
console.log(birthgem.zodiac('♈');
// Overload the default language (format xx-YY sets (format xx)
console.log(birthgem.zodiac('aries', 'fr'));
console.log(birthgem.zodiac('♈', 'fr');
```

## Error management

An integer is returned if the given parameter is wrong:

| Type   | Values                         | Error code |
|--------|--------------------------------|------------|
| Day    | [1;7]                          | -1         |
| Month  | [1;12]                         | -2         |
| Zodiac | zodiac signs names and symbols | -3         |

## Translation

For the moment, the only avaible languages are English and French.

Obviously, you are free to participate to the translation in any other language.

### Avaible languages

- English
- French

## Thanks

Thanks to ekimng for the original package: [birthstone](https://github.com/ekimng/birthstone).

## License

- My source code is published under [MIT License](https://github.com/Helmasaur/birthgem/blob/master/LICENSE).
- The original package is published under [MIT License](https://github.com/ekimng/birthstone/blob/master/LICENSE).