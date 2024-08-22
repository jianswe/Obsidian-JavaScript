In JavaScript, basic data types (also known as primitive data types) are the fundamental building blocks for managing data. Here are the main ones:

1. **Number**: Represents both integer and floating-point numbers. Example:
   ```javascript
   let age = 25;
   let temperature = 98.6;
   ```

2. **String**: A sequence of characters used to represent text. Strings are enclosed in single (`'`), double (`"`), or backticks (`` ` ``). Example:
   ```javascript
   let name = "Jian Kuang";
   let greeting = `Hello, ${name}`;
   ```

3. **Boolean**: Represents logical values, either `true` or `false`. Example:
   ```javascript
   let isActive = true;
   let isComplete = false;
   ```

4. **Null**: A special value representing "no value" or "nothing." It’s explicitly assigned to a variable to indicate the absence of any object value. Example:
   ```javascript
   let emptyValue = null;
   ```

5. **Undefined**: Represents a variable that has been declared but not yet assigned a value. Example:
   ```javascript
   let notAssigned;
   console.log(notAssigned); // undefined
   ```
 You should generally avoid manually assigning `undefined` because it can obscure the intent of your code and lead to confusion. Instead, use `null` for intentional empty values and rely on `undefined` for uninitialized variables or missing properties. This practice helps keep your code more readable, consistent, and easier to debug.  
6. **Symbol**: Introduced in ES6, `Symbol` is used to create unique identifiers. Example:
   ```javascript
   let uniqueId = Symbol('id');
   ```

7. **BigInt**: Introduced in ES2020, `BigInt` is used for integers that are too large to be represented by the `Number` type. Example:
   ```javascript
   let bigNumber = BigInt(1234567890123456789012345678901234567890n);
   ```

These basic data types form the foundation of data handling in JavaScript.