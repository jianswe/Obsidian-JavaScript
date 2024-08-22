In JavaScript, a `String` is a primitive data type used to represent and manipulate text. Strings are a sequence of characters enclosed in single quotes (`'`), double quotes (`"`), or backticks (`` ` ``). They are immutable, meaning once a string is created, it cannot be altered. However, you can create new strings by concatenating or modifying existing ones.
## Common String Methods

JavaScript provides a wide range of methods to manipulate and interact with strings:

1. **`charAt(index)`**: Returns the character at the specified index. Time Complexity: `O(1)`
   ```javascript
   let text = "Hello, Jian!";
   console.log(text.charAt(1)); // e
   ```

2. **`concat(str1, str2, ...)`**: Combines two or more strings. Time Complexity: `O(n+m+...)`
   ```javascript
   let text1 = "Hello";
   let text2 = "Jian";
   let combined = text1.concat(", ", text2, "!");
   console.log(combined); // "Hello, Jian!"
   ```

3. **`slice(start, end)`**: Extracts a section of the string and returns it as a new string. Time Complexity: `O(m)` linear relative to the length of the substring `m` that is being extracted, as it needs to copy each character into a new string.
   ```javascript
   let text = "Hello, Jian!";
   console.log(text.slice(7, 11)); // "Jian"
   ```

4. **`substring(start, end)`**: Similar to `slice`, extracts characters from `start` to `end` (but does not accept negative indices). Time Complexity: **O(m)** where `m` is the length of the substring being extracted.
    ```javascript
    let text = "Hello, Jian!";
    console.log(text.substring(7, 11)); // "Jian"
    ```

5. **`toUpperCase()` and `toLowerCase()`**: Converts the entire string to uppercase or lowercase. Time Complexity: `O(n)` 
   ```javascript
   let text = "Hello, Jian!";
   console.log(text.toUpperCase()); // "HELLO, JIAN!"
   console.log(text.toLowerCase()); // "hello, jian!"
   ```

6. **`trim()`**: Removes whitespace from both ends of a string. Time Complexity: `O(n)
   ```javascript
   let text = "   Hello, Jian!   ";
   console.log(text.trim()); // "Hello, Jian!"
   ```

7. **`split(separator)`**: Splits the string into an array of substrings based on the specified separator. Time Complexity: `O(n*m)` depends on both the length of the string (`n`) and the number of splits (`m`), leading to a potential complexity of `O(n * m)` in the worst case.
   ```javascript
   let text = "Hello, Jian!";
   let words = text.split(" ");
   console.log(words); // ["Hello,", "Jian!"]
   ```

8. **`includes(substring)`**: Checks if a string contains a specific substring, returning `true` or `false`. Time Complexity: `O(n*m)` If `n` is the length of the string and `m` is the length of the substring
   ```javascript
   let text = "Hello, Jian!";
   console.log(text.includes("Jian")); // true
   ```

9. **`indexOf(substring)`**: Returns the index of the first occurrence of a substring, or `-1` if not found. Time Complexity: `O(n*m)`
   ```javascript
   let text = "Hello, Jian!";
   console.log(text.indexOf("Jian")); // 7
   ```

10. **`replace(searchValue, newValue)`**: Replaces the first occurrence of a substring with a new value. Time Complexity: **O(n * m)** depends on searching for the substring (`O(n * m)`) and constructing the new string.
   ```javascript
   let text = "Hello, Jian!";
   let newText = text.replace("Jian", "World");
   console.log(newText); // "Hello, World!"
   ```
### Template Literals

Template literals, introduced in ES6, provide a more powerful way to work with strings:

- **Multi-line Strings:**
  ```javascript
  let multiLine = `This is
  a string
  with multiple lines.`;
  console.log(multiLine);
  ```

- **String Interpolation:**
  ```javascript
  let name = "Jian";
  let greeting = `Hello, ${name}!`;
  console.log(greeting); // "Hello, Jian!"
  ```

### Immutability of Strings

Since strings are immutable, any method or operation that appears to modify a string actually returns a new string.

```javascript
let text = "Hello, Jian!";
text[0] = "h"; // This does nothing, as strings are immutable
console.log(text); // "Hello, Jian!"
```

### Summary

Strings in JavaScript are a versatile and fundamental data type, offering various methods for manipulation and formatting. Their immutability ensures that any operations on strings do not change the original string but instead return new ones, making them reliable and predictable in use.