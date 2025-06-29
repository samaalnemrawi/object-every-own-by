# Object Every Own By: Validate Object Properties with Ease

![GitHub release](https://img.shields.io/github/release/samaalnemrawi/object-every-own-by.svg) ![GitHub issues](https://img.shields.io/github/issues/samaalnemrawi/object-every-own-by.svg) ![GitHub forks](https://img.shields.io/github/forks/samaalnemrawi/object-every-own-by.svg) ![GitHub stars](https://img.shields.io/github/stars/samaalnemrawi/object-every-own-by.svg)

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [API](#api)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

## Overview

The **Object Every Own By** library allows you to test whether all own properties of an object pass a test implemented by a predicate function. This utility simplifies the validation process for object properties in JavaScript, making it easier to ensure data integrity.

### Key Features

- Validate all own properties of an object.
- Implement your own predicate function.
- Works seamlessly with JavaScript and Node.js.
- Lightweight and easy to integrate.

## Installation

To install the library, you can use npm or yarn. Open your terminal and run one of the following commands:

```bash
npm install object-every-own-by
```

or

```bash
yarn add object-every-own-by
```

## Usage

After installation, you can import the library into your JavaScript file. Here’s how to use it:

```javascript
const everyOwnBy = require('object-every-own-by');

const obj = {
    a: 1,
    b: 2,
    c: 3
};

const predicate = value => value > 0;

const result = everyOwnBy(obj, predicate);
console.log(result); // true
```

## API

### `everyOwnBy(object, predicate)`

- **Parameters**
  - `object`: The object whose properties you want to test.
  - `predicate`: A function that takes a property value and returns a boolean.

- **Returns**
  - A boolean indicating whether all own properties pass the test.

### Example

Here’s a more detailed example to illustrate how the library works:

```javascript
const everyOwnBy = require('object-every-own-by');

const person = {
    name: 'John',
    age: 30,
    height: 175
};

const isNumber = value => typeof value === 'number';

const allAreNumbers = everyOwnBy(person, isNumber);
console.log(allAreNumbers); // true
```

## Examples

### Example 1: All Properties Are Strings

```javascript
const everyOwnBy = require('object-every-own-by');

const colors = {
    red: 'red',
    green: 'green',
    blue: 'blue'
};

const isString = value => typeof value === 'string';

const allAreStrings = everyOwnBy(colors, isString);
console.log(allAreStrings); // true
```

### Example 2: Mixed Property Types

```javascript
const everyOwnBy = require('object-every-own-by');

const mixed = {
    name: 'Alice',
    age: 25,
    employed: true
};

const isBoolean = value => typeof value === 'boolean';

const allAreBooleans = everyOwnBy(mixed, isBoolean);
console.log(allAreBooleans); // false
```

### Example 3: Custom Predicate Function

```javascript
const everyOwnBy = require('object-every-own-by');

const numbers = {
    a: 4,
    b: 8,
    c: 12
};

const isEven = value => value % 2 === 0;

const allAreEven = everyOwnBy(numbers, isEven);
console.log(allAreEven); // true
```

## Contributing

Contributions are welcome! If you want to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature/YourFeature`).
6. Open a pull request.

Please ensure your code follows the project's coding style and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest releases, visit [Releases](https://github.com/samaalnemrawi/object-every-own-by/releases). You can download the latest version and execute it as needed.

## Additional Resources

- [JavaScript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [GitHub Guides](https://guides.github.com/)

## Feedback

If you have any questions or feedback, feel free to reach out through the Issues section on GitHub. Your input is valuable and helps improve the project.

For further updates, you can always check the [Releases](https://github.com/samaalnemrawi/object-every-own-by/releases) section for the latest changes and improvements.