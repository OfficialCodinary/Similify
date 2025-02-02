
# Similify

[![npm version](https://img.shields.io/npm/v/similify.svg)](https://www.npmjs.com/package/similify)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![GitHub issues](https://img.shields.io/github/issues/Untoldhacker-Dev/Similify.svg)](https://github.com/Untoldhacker-Dev/Similify/issues)
[![GitHub stars](https://img.shields.io/github/stars/Untoldhacker-Dev/Similify.svg)](https://github.com/Untoldhacker-Dev/Similify/stargazers)
[![Telegram](https://img.shields.io/badge/chat-on%20telegram-0088cc.svg)](https://t.me/AutomationCore)

Similify is a versatile JavaScript package designed to simplify and enhance similarity comparisons in various contexts. Whether you're comparing words, objects, arrays, or exploring string lengths and numerical ranges, Similify provides an easy-to-use interface with customizable thresholds. Effortlessly find the most similar instances and match percentages, making complex comparisons a breeze. Streamline your similarity analysis and unlock new possibilities with Similify.

## Installation

```bash
npm install similify
```

## Usage

Require Similify in your JavaScript file and start using its functions:

### Compare Words

```javascript
const { compareWords } = require('similify');

// Example usage with default threshold (70)
console.log(compareWords("apple", "orange"));

// Example usage with custom threshold
const customThreshold = 80;
console.log(compareWords("apple", "orange", customThreshold));
```

### Word to Object in Array Comparison

```javascript
const { wordToObjectArrayComparison } = require('similify');

const objectsArray = [{ name: "banana" }, { name: "orange" }];

console.log(wordToObjectArrayComparison("apple", objectsArray, "name"));
```

### Compare Objects

```javascript
const { compareObjects } = require('similify');

// Example usage with default threshold (70)
console.log(compareObjects({ a: 1, b: 2 }, { a: 1, b: 3 }));

// Example usage with custom threshold
const customThreshold = 80;
console.log(compareObjects({ a: 1, b: 2 }, { a: 1, b: 3 }, customThreshold));
```

### Compare Array Places

```javascript
const { compareArrayPlaces } = require('similify');

const array1 = ["apple", "banana"];
const array2 = ["orange", "banana"];

console.log(compareArrayPlaces(array1, 0, array2, 1));
```

### Compare Word to Array

```javascript
const { compareWordToArray } = require('similify');

const word = "apple";
const array = ["orange", "banana", "grape"];

console.log(compareWordToArray(word, array));
```

### Compare Arrays

```javascript
const { compareArrays } = require('similify');

const array1 = ["apple", "banana"];
const array2 = ["orange", "banana", "grape"];

console.log(compareArrays(array1, array2));
```

### Compare String Length

```javascript
const { compareStringLength } = require('similify');

console.log(compareStringLength("apple", "orange"));
```

### Compare Number to Range

```javascript
const { compareNumberToRange } = require('similify');

console.log(compareNumberToRange(25, 20, 30));
```

## Below are explanations for each function provided by the Similify package:

### `compareWords(word1, word2, threshold = 70)`

This function compares two words, `word1` and `word2`, by calculating the similarity percentage based on letter matching. The default threshold is set to 70, and the function returns an object with the most similar word and the match percentage.

### `wordToObjectArrayComparison(word, objectArray, key, threshold = 70)`

This function compares a word to the values of a specified key within an array of objects (`objectArray`). It calculates the similarity percentage for each value and returns an object containing the most similar object instance and the corresponding match percentage.

### `compareObjects(obj1, obj2, threshold = 70)`

Compares two objects (`obj1` and `obj2`) by converting them to JSON strings and then calculating the similarity percentage based on letter matching. The default threshold is set to 70, and the function returns an object with the most similar object and the match percentage.

### `compareArrayPlaces(array1, index1, array2, index2, threshold = 70)`

Compares two elements at specified indices (`index1` and `index2`) within two arrays (`array1` and `array2`). It calculates the similarity percentage based on letter matching and returns an object with the most similar element and the match percentage. The default threshold is set to 70.

### `compareWordToArray(word, array, threshold = 70)`

Compares a word to each element in an array (`array`). It calculates the similarity percentage for each element and returns an object with the most similar element and the match percentage. The default threshold is set to 70.

### `compareArrays(array1, array2, threshold = 70)`

Compares each element in two arrays (`array1` and `array2`). It calculates the similarity percentage for each pair of elements and returns an object with the most similar elements and the match percentage. The default threshold is set to 70.

### `compareStringLength(str1, str2)`

Compares the lengths of two strings (`str1` and `str2`). It returns an object with the longer string and the absolute difference in length between the two strings.

### `compareNumberToRange(number, min, max)`

Checks if a number is within a specified range (`min` to `max`). It returns an object with a boolean indicating whether the number is within the range and the deviation of the number from the midpoint of the range.

These functions provide a variety of comparison functionalities, allowing users to find similarities in words, objects, arrays, string lengths, and numerical ranges. Users can also customize the threshold for similarity based on their specific requirements.


## Support

For support and discussions, join our Telegram channel: [AutomationCore](https://t.me/AutomationCore)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
