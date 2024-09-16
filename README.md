# 200 Javascript Interview Questions

Here’s a list of 100 **JavaScript output-based interview questions** along with **detailed explanations** of each, helping you grasp the key concepts easily.

---

### **1. What is the output of the following?**

```js
console.log(typeof null);
```

**Output**: `"object"`

**Explanation**: In JavaScript, `null` is considered to be an object for legacy reasons. It's a bug in the language but can't be fixed due to backward compatibility.

---

### **2. What is the output of this?**

```js
console.log(1 + '2' + '2');
```

**Output**: `"122"`

**Explanation**: JavaScript uses type coercion. Here, `1` is a number, `'2'` is a string. The number `1` is coerced into a string, resulting in concatenation: `'1' + '2' + '2' = "122"`.

---

### **3. What is the output?**

```js
console.log('1' - 1);
```

**Output**: `0`

**Explanation**: When using the `-` operator, JavaScript converts the string `'1'` into a number and performs the subtraction, resulting in `0`.

---

### **4. What is the result of this?**

```js
console.log(true + false);
```

**Output**: `1`

**Explanation**: In JavaScript, `true` is coerced to `1` and `false` to `0`. Hence, `1 + 0 = 1`.

---

### **5. What’s the output?**

```js
console.log(3 > 2 > 1);
```

**Output**: `false`

**Explanation**: `3 > 2` evaluates to `true`. Then, `true > 1` is evaluated as `1 > 1`, which is `false`.

---

### **6. What will this print?**

```js
console.log([] + []);
```

**Output**: `""` (empty string)

**Explanation**: When you use `+` with arrays, JavaScript converts them to strings. Since both are empty arrays, you get an empty string.

---

### **7. What will this print?**

```js
console.log([] + {});
console.log({} + []);
```

**Output**:
- First: `"[object Object]"`
- Second: `0`

**Explanation**: 
- `[] + {}`: Array gets converted to an empty string, and object gets converted to `'[object Object]'`, so the result is `"[object Object]"`.
- `{}` is interpreted as a block, and `+[]` results in `0`.

---

### **8. What’s the output?**

```js
console.log(1 + + '2');
```

**Output**: `3`

**Explanation**: The unary `+` operator before `'2'` converts it to a number, so it's equivalent to `1 + 2 = 3`.

---

### **9. What does this print?**

```js
let a = [1, 2, 3];
a[10] = 99;
console.log(a.length);
```

**Output**: `11`

**Explanation**: Setting a value at index 10 means the array’s length becomes `11`, even though there are empty slots between index `3` and `9`.

---

### **10. What is the output here?**

```js
console.log(null == undefined);
```

**Output**: `true`

**Explanation**: `null` and `undefined` are loosely equal but not strictly equal (`===`).

---

### **11. What will this return?**

```js
console.log(!!null);
console.log(!!"");
console.log(!!1);
```

**Output**: 
- `false`
- `false`
- `true`

**Explanation**: The `!!` converts a value to its boolean equivalent. `null` and `""` are falsy, while `1` is truthy.

---

### **12. What will be the result?**

```js
console.log(typeof NaN);
```

**Output**: `"number"`

**Explanation**: `NaN` stands for "Not-a-Number", but it is still of type `"number"` in JavaScript.

---

### **13. What’s the output?**

```js
let a = 1;
let b = 2;
console.log(a = b);
```

**Output**: `2`

**Explanation**: The expression `a = b` assigns the value of `b` to `a`, and the result of the assignment is the value assigned, which is `2`.

---

### **14. What will this print?**

```js
console.log([] == []);
console.log({} == {});
```

**Output**: 
- `false`
- `false`

**Explanation**: Arrays and objects are compared by reference, not by value. Two different arrays or objects are never equal, even if they have the same contents.

---

### **15. What does this print?**

```js
let a = [1, 2, 3];
let b = a;
b.push(4);
console.log(a);
```

**Output**: `[1, 2, 3, 4]`

**Explanation**: `b` is a reference to the same array as `a`, so pushing to `b` also affects `a`.

---

### **16. What’s the output?**

```js
console.log([] == ![]);
```

**Output**: `true`

**Explanation**: The `![]` converts the empty array to `false`. Then, `[] == false` becomes `true` because of type coercion (`[]` is falsy).

---

### **17. What’s the output of this?**

```js
console.log(typeof function(){});
```

**Output**: `"function"`

**Explanation**: Functions in JavaScript are of the type `"function"`.

---

### **18. What will be the result?**

```js
let a = [1, 2, 3];
delete a[1];
console.log(a);
console.log(a.length);
```

**Output**: 
- `[1, empty, 3]`
- `3`

**Explanation**: `delete` removes the value but does not update the length of the array. It leaves an empty slot (`undefined`).

---

### **19. What does this return?**

```js
let a = 5;
console.log(a++); 
console.log(++a);
```

**Output**: 
- `5`
- `7`

**Explanation**:
- `a++` returns the current value (`5`), then increments `a` to `6`.
- `++a` increments `a` first (`7`), then returns it.

---

### **20. What is the output here?**

```js
console.log(typeof typeof 1);
```

**Output**: `"string"`

**Explanation**: 
- `typeof 1` returns `"number"`.
- `typeof "number"` returns `"string"` because `"number"` is a string.

---

### **21. What does this log?**

```js
console.log("5" - 3);
```

**Output**: `2`

**Explanation**: The `-` operator forces the string `"5"` to be converted into a number, so `5 - 3 = 2`.

---

### **22. What’s the output?**

```js
console.log([1, 2] + [3, 4]);
```

**Output**: `"1,23,4"`

**Explanation**: When arrays are concatenated using `+`, they are first converted to strings. `['1,2'] + ['3,4'] = "1,23,4"`.

---

### **23. What will this return?**

```js
console.log(0.1 + 0.2 == 0.3);
```

**Output**: `false`

**Explanation**: Due to floating-point precision errors, `0.1 + 0.2` equals something like `0.30000000000000004`, not exactly `0.3`.

---

### **24. What will this print?**

```js
let a = 0;
console.log(a++);
console.log(a);
```

**Output**:
- `0`
- `1`

**Explanation**: `a++` increments the value of `a` but returns the previous value.

---

### **25. What’s the output?**

```js
console.log([] == ![]);
```

**Output**: `true`

**Explanation**: `![]` evaluates to `false`, and `[] == false` is coerced to `true` because of JavaScript's type coercion rules.

---

### **26. What’s the result of this?**

```js
console.log({} + {});
```

**Output**: `[object Object][object Object]`

**Explanation**: When objects are concatenated, they are converted to strings, resulting in `"[object Object][object Object]"`.

---

### **27. What will this log?**

```js
console.log(3 + '3' - '3');
```

**Output**: `30`

**Explanation**: `'3' - '3'` is `0`, and `3 + '0'` results in `30`.

---

### **28. What does this return?**

```js
console.log(true == '1');
```

**Output**: `true`

**Explanation**: The string `'1'` is coerced

 into the number `1`, and `true` is also coerced into `1`, making them equal.

---

### **29. What is the output?**

```js
console.log(!!false == !!'');
```

**Output**: `true`

**Explanation**: Both `false` and `''` are falsy values. Using the `!!` operator converts them into `false`, so the result is `true`.

---

### **30. What’s the output of this?**

```js
console.log([] == ![]);
```

**Output**: `true`

**Explanation**: The `![]` is evaluated as `false`, and `[] == false` results in `true` due to type coercion.

---

---

### **31. What is the output of this code?**

```js
console.log([] == false);
```

**Output**: `false`

**Explanation**: `[]` is an empty array and `false` is a boolean. When comparing different types, JavaScript attempts to coerce them to a common type. Here, `[]` is coerced to a string `""` and `false` to `"false"`, so they are not equal.

---

### **32. What does this print?**

```js
console.log([] == 0);
```

**Output**: `false`

**Explanation**: An empty array `[]` is coerced to an empty string `""` and then to `0` in the context of numerical comparison. However, `[]` coerces to `false` in other contexts, but not `0`. Thus, `[] == 0` is `false`.

---

### **33. What will this return?**

```js
console.log(0 == '0');
console.log(0 === '0');
```

**Output**:
- `true`
- `false`

**Explanation**:
- `==` performs type coercion, so `0` is coerced to `'0'`, making them equal.
- `===` checks for strict equality without type coercion, so `0` (number) and `'0'` (string) are not equal.

---

### **34. What is the result of this?**

```js
console.log([1, 2] == [1, 2]);
```

**Output**: `false`

**Explanation**: In JavaScript, arrays are compared by reference, not by value. Even though the arrays have the same contents, they are different objects in memory, so they are not equal.

---

### **35. What does this code print?**

```js
console.log(1 + '2' - 1);
```

**Output**: `11`

**Explanation**: `1 + '2'` results in `'12'` due to string concatenation. Subtracting `1` from `'12'` coerces `'12'` back to a number, resulting in `11`.

---

### **36. What will be the output of this?**

```js
console.log('5' - 3);
console.log('5' * 2);
console.log('5' / 2);
```

**Output**:
- `2`
- `10`
- `2.5`

**Explanation**:
- `'5' - 3` converts `'5'` to a number, resulting in `2`.
- `'5' * 2` converts `'5'` to a number and multiplies, resulting in `10`.
- `'5' / 2` converts `'5'` to a number and divides, resulting in `2.5`.

---

### **37. What will be the output?**

```js
console.log(0.1 + 0.2 == 0.3);
console.log(Math.abs((0.1 + 0.2) - 0.3) < Number.EPSILON);
```

**Output**:
- `false`
- `true`

**Explanation**:
- `0.1 + 0.2` is not exactly `0.3` due to floating-point precision errors.
- `Number.EPSILON` is a tiny number representing the smallest interval between two representable numbers, used to check if the result is within acceptable precision.

---

### **38. What’s the result of this?**

```js
console.log(typeof null == typeof undefined);
```

**Output**: `true`

**Explanation**: Both `null` and `undefined` have the same type when using `typeof`, which is `"object"` for `null` (legacy bug) and `"undefined"` for `undefined`. The comparison is `true` for the types used in `typeof`.

---

### **39. What does this code print?**

```js
console.log([1] == [1]);
console.log([1] === [1]);
```

**Output**:
- `false`
- `false`

**Explanation**:
- `==` and `===` compare references, not values. Different array instances even with the same contents are not equal.

---

### **40. What is the output?**

```js
console.log('a' + + 'b');
```

**Output**: `"aNaN"`

**Explanation**: `+ 'b'` attempts to coerce `'b'` to a number, resulting in `NaN`. Concatenating `'a'` with `NaN` results in `'aNaN'`.

---

### **41. What will this return?**

```js
console.log('true' == true);
console.log('true' === true);
```

**Output**:
- `false`
- `false`

**Explanation**:
- `==` performs type coercion, but `'true'` is a string and `true` is a boolean, so they are not equal.
- `===` checks for strict equality without type coercion.

---

### **42. What’s the result of this?**

```js
console.log(1 + '2' + 2);
```

**Output**: `"122"`

**Explanation**: `1 + '2'` results in `'12'`, and `'12' + 2` results in `'122'` because `2` is coerced to a string.

---

### **43. What does this code print?**

```js
console.log([] + {});
console.log({} + []);
```

**Output**:
- `"[object Object]"`
- `0`

**Explanation**:
- `[] + {}`: Array `[]` is converted to an empty string `""`, and `{}` is converted to `[object Object]`.
- `{}` is interpreted as a block statement, so `{} + []` is equivalent to `0 + []` which results in `0`.

---

### **44. What is the output?**

```js
console.log(1 + '1' - 1);
```

**Output**: `10`

**Explanation**: `1 + '1'` results in `'11'`. Subtracting `1` from `'11'` coerces it back to a number, resulting in `10`.

---

### **45. What does this print?**

```js
console.log([1] + [2]);
console.log([1] + 2);
console.log(2 + [1]);
```

**Output**:
- `"12"`
- `"12"`
- `"21"`

**Explanation**:
- Arrays are converted to strings when used with `+`, so `[1] + [2]` becomes `"1" + "2"`.
- `[1] + 2` is `"1" + "2"`.
- `2 + [1]` is `2 + "1"` which results in `"21"`.

---

### **46. What will this return?**

```js
console.log(+ '1' === 1);
```

**Output**: `true`

**Explanation**: `+ '1'` converts the string `'1'` to the number `1`, which is strictly equal to `1`.

---

### **47. What does this print?**

```js
console.log(0 == '0');
console.log(0 === '0');
console.log(0 == []);
```

**Output**:
- `true`
- `false`
- `false`

**Explanation**:
- `==` performs type coercion, converting `'0'` to `0`.
- `===` checks for strict equality.
- `[]` coerces to `false`, so `0 == []` is `false`.

---

### **48. What will this output?**

```js
console.log([2] == [2]);
console.log([2] === [2]);
console.log({} == {});
```

**Output**:
- `false`
- `false`
- `false`

**Explanation**: Arrays and objects are compared by reference. Different instances with the same content are not equal.

---

### **49. What is the result?**

```js
console.log('1' - - '1');
```

**Output**: `2`

**Explanation**: `'1' - - '1'` is equivalent to `1 - (-1)`, which equals `2`.

---

### **50. What does this code print?**

```js
console.log('foo' + +'bar');
```

**Output**: `"fooNaN"`

**Explanation**: `+'bar'` attempts to convert `'bar'` to a number, resulting in `NaN`. Concatenating `'foo'` with `NaN` results in `'fooNaN'`.

---

### **51. What’s the output of this?**

```js
console.log(null + 1);
console.log(null - 1);
console.log(null * 1);
console.log(null / 1);
```

**Output**:
- `1`
- `-1`
- `0`
- `0`

**Explanation**: 
- `null` is coerced to `0` in numerical operations, except for addition where `null + 1` results in `1`.

---

### **52. What is the output?**

```js
console.log(0.1 + 0.2 == 0.3);
console.log(Math.abs((0.1 + 0.2) - 0.3) < Number.EPSILON);
```

**Output**:
- `false

`
- `true`

**Explanation**: 
- Floating-point arithmetic may not be precise. 
- `Number.EPSILON` is used to check if two numbers are close enough to be considered equal.

---

### **53. What does this print?**

```js
console.log([1] + [2] + 3);
```

**Output**: `"123"`

**Explanation**: `[1] + [2]` results in `'12'`, and `'12' + 3` results in `'123'`.

---

### **54. What will this output?**

```js
console.log(+true);
console.log(+false);
console.log(-true);
console.log(-false);
```

**Output**:
- `1`
- `0`
- `-1`
- `-0`

**Explanation**: `+true` and `+false` convert to `1` and `0`, respectively. `-true` and `-false` convert to `-1` and `-0`.

---

### **55. What does this code print?**

```js
console.log('' + 0);
console.log(0 + '');
console.log('' - 0);
console.log(0 - '');
```

**Output**:
- `"0"`
- `"0"`
- `0`
- `0`

**Explanation**: 
- `'' + 0` and `0 + ''` result in `'0'` due to string concatenation.
- `'' - 0` results in `0` due to type coercion to numbers.

---

### **56. What is the output?**

```js
console.log([] + {});
```

**Output**: `"[object Object]"`

**Explanation**: `[]` coerces to an empty string `""`, and `{}` coerces to `[object Object]`, so the result is `"[object Object]"`.

---

### **57. What does this print?**

```js
console.log({} + []);
```

**Output**: `0`

**Explanation**: `{}` is treated as an empty block, so `{} + []` is equivalent to `0 + []`, resulting in `0`.

---

### **58. What will this return?**

```js
console.log(!!null);
console.log(!!undefined);
console.log(!!NaN);
console.log(!!0);
```

**Output**:
- `false`
- `false`
- `false`
- `false`

**Explanation**: All these values are falsy, so `!!` converts them to `false`.

---

### **59. What is the result?**

```js
console.log([] == ![]);
console.log([] === ![]);
```

**Output**:
- `true`
- `false`

**Explanation**: `![]` is `false`, and `[] == false` evaluates to `true` due to type coercion. `[] === ![]` is `false` because they are different types.

---

### **60. What does this code print?**

```js
console.log('a' + + 'b' + 'c');
```

**Output**: `"aNaNc"`

**Explanation**: `+ 'b'` coerces `'b'` to `NaN`, so `'a' + NaN` is `'aNaN'`, and `'aNaN' + 'c'` is `'aNaNc'`.

---

### **61. What’s the output of this?**

```js
console.log('1' == 1);
console.log('1' === 1);
console.log('1' != 1);
console.log('1' !== 1);
```

**Output**:
- `true`
- `false`
- `false`
- `true`

**Explanation**: 
- `==` performs type coercion, while `===` does not. 
- `'1' == 1` is `true` due to coercion. `'1' === 1` is `false` due to strict equality.

---

### **62. What will be the output?**

```js
console.log('1' + 1);
console.log('1' - 1);
console.log(1 + '1');
console.log(1 - '1');
```

**Output**:
- `"11"`
- `0`
- `"11"`
- `0`

**Explanation**: 
- `'1' + 1` and `1 + '1'` result in string concatenation.
- `'1' - 1` and `1 - '1'` result in numeric operations.

---

### **63. What does this print?**

```js
console.log([2] == [2]);
console.log([2] === [2]);
console.log({} == {});
```

**Output**:
- `false`
- `false`
- `false`

**Explanation**: 
- Arrays and objects are compared by reference, so different instances are not equal.

---

### **64. What’s the result of this?**

```js
console.log([] == ![]);
console.log([] === ![]);
```

**Output**:
- `true`
- `false`

**Explanation**: 
- `![]` evaluates to `false`, and `[] == false` is `true` due to type coercion.
- `[] === ![]` is `false` as `[]` and `false` are different types.

---

### **65. What will be the output?**

```js
console.log('5' - 3);
console.log('5' * 2);
console.log('5' / 2);
```

**Output**:
- `2`
- `10`
- `2.5`

**Explanation**: 
- `-` converts `'5'` to a number before subtraction.
- `*` and `/` also coerce `'5'` to a number.

---

### **66. What does this code print?**

```js
console.log(0.1 + 0.2 === 0.3);
```

**Output**: `false`

**Explanation**: Due to floating-point precision issues, `0.1 + 0.2` does not exactly equal `0.3`.

---

### **67. What will this return?**

```js
console.log(typeof NaN);
console.log(typeof Infinity);
console.log(typeof -Infinity);
```

**Output**:
- `"number"`
- `"number"`
- `"number"`

**Explanation**: `NaN` and `Infinity` are both of type `number` in JavaScript.

---

### **68. What is the output?**

```js
console.log(!!(1 + 1));
console.log(!!(0 + 1));
console.log(!!(0 - 1));
console.log(!!(0));
```

**Output**:
- `true`
- `true`
- `true`
- `false`

**Explanation**: 
- `!!` converts truthy values to `true` and falsy values to `false`.

---

### **69. What does this print?**

```js
console.log('1' + 1);
console.log(1 + '1');
console.log(1 - '1');
```

**Output**:
- `"11"`
- `"11"`
- `0`

**Explanation**: 
- `+` with a string converts numbers to strings for concatenation.
- `-` converts the string to a number before performing subtraction.

---

### **70. What is the result of this code?**

```js
console.log([] == ![]);
console.log([] === ![]);
```

**Output**:
- `true`
- `false`

**Explanation**: 
- `![]` converts to `false`, so `[] == false` is `true` due to type coercion.
- `[] === ![]` is `false` as they are different types.

---

### **71. What’s the output?**

```js
console.log({} + []);
console.log([] + {});
```

**Output**:
- `0`
- `"[object Object]"`

**Explanation**: 
- `{}` is treated as a block, so `{} + []` results in `0 + []`.
- `[] + {}` results in an empty string concatenated with the string representation of the object.

---

### **72. What does this code print?**

```js
console.log(+ '1' + 1);
console.log(+ '1' - 1);
console.log(+ '1' * 2);
console.log(+ '1' / 2);
```

**Output**:
- `2`
- `0`
- `2`
- `0.5`

**Explanation**: `+ '1'` converts `'1'` to the number `1`. The subsequent operations use this number.

---

### **73. What will this return?**

```js
console.log([1] == [1]);
console.log([1] === [1]);
console.log([] == false);
console.log([] === false);
```

**Output**:
- `false`
- `false`
- `false`
- `false`

**Explanation**: 
- Arrays and objects are compared by reference. Different instances with the same content are not equal.
- `[]` coerces to `false` in comparisons, but strict equality `===` is `false` for different types.

---

### **74. What’s the result of this?**

```js
console.log(1 + '1' - 1);
console.log(1 - '1' + 1);
```

**Output**:
- `10`
- `1`

**Explanation**: 
- `1 + '1'` results in `'11'`,

 and subtracting `1` coerces it back to `10`.
- `1 - '1'` results in `0`, adding `1` results in `1`.

---

### **75. What does this code print?**

```js
console.log(!!undefined);
console.log(!!NaN);
console.log(!!0);
console.log(!!(''));
```

**Output**:
- `false`
- `false`
- `false`
- `false`

**Explanation**: All these values are falsy, so `!!` converts them to `false`.

---

### **76. What will be the output?**

```js
console.log(typeof (1 + '1'));
console.log(typeof (1 - '1'));
console.log(typeof (1 * '1'));
console.log(typeof (1 / '1'));
```

**Output**:
- `"string"`
- `"number"`
- `"number"`
- `"number"`

**Explanation**: 
- `1 + '1'` results in a string.
- `1 - '1'`, `1 * '1'`, and `1 / '1'` result in numbers.

---

### **77. What does this print?**

```js
console.log([2] == [2]);
console.log([2] === [2]);
console.log({} == {});
console.log({} === {});
```

**Output**:
- `false`
- `false`
- `false`
- `false`

**Explanation**: Arrays and objects are compared by reference, so different instances are not equal.

---

### **78. What’s the result?**

```js
console.log(!!'false');
console.log(!!false);
console.log(!!'0');
console.log(!!0);
```

**Output**:
- `true`
- `false`
- `true`
- `false`

**Explanation**: Non-empty strings and `false` are falsy, while empty strings and `0` are falsy.

---

### **79. What will this return?**

```js
console.log([] + {} + []);
```

**Output**: `"[object Object]"`

**Explanation**: `[]` coerces to an empty string, `{}` to `[object Object]`, and the final result is `[object Object]`.

---

### **80. What is the output?**

```js
console.log(+[] + 1);
console.log(+{} + 1);
console.log(+null + 1);
```

**Output**:
- `1`
- `NaN`
- `1`

**Explanation**:
- `+[]` is `0`, so `0 + 1` is `1`.
- `+{}` is `NaN` because `{}` cannot be coerced to a number.
- `+null` is `0`, so `0 + 1` is `1`.

---

### **81. What does this code print?**

```js
console.log([] == false);
console.log([] === false);
console.log(false == []);
console.log(false === []);
```

**Output**:
- `false`
- `false`
- `false`
- `false`

**Explanation**: 
- `[]` is not strictly equal to `false` or equal to `false` with type coercion.

---

### **82. What’s the result of this?**

```js
console.log([1] + 1);
console.log([1] - 1);
console.log(1 + [1]);
console.log(1 - [1]);
```

**Output**:
- `"11"`
- `0`
- `"11"`
- `0`

**Explanation**: 
- `+` with a string converts numbers to strings for concatenation.
- `-` converts the array to a number for subtraction.

---

### **83. What will this return?**

```js
console.log(!!' ' === !!'');
console.log(!!'0' === !!0);
```

**Output**:
- `false`
- `true`

**Explanation**: 
- `' '` is a non-empty string and `''` is an empty string.
- `'0'` and `0` both convert to `true` when using `!!`.

---

### **84. What does this code print?**

```js
console.log(1 + [1] + 1);
console.log([1] + 1 + 1);
```

**Output**:
- `"111"`
- `"111"`

**Explanation**: Both expressions result in concatenation of `"1"` strings.

---

### **85. What is the output of this?**

```js
console.log(1 + '1' + 1);
console.log(1 + 1 + '1');
```

**Output**:
- `"111"`
- `"21"`

**Explanation**:
- `1 + '1'` results in `'11'`, and adding `1` results in `'111'`.
- `1 + 1` results in `2`, and adding `'1'` results in `'21'`.

---

### **86. What will this return?**

```js
console.log(+[] + 1);
console.log(+{} + 1);
console.log(+null + 1);
```

**Output**:
- `1`
- `NaN`
- `1`

**Explanation**:
- `+[]` is `0`, so `0 + 1` is `1`.
- `+{}` is `NaN` because `{}` cannot be coerced to a number.
- `+null` is `0`, so `0 + 1` is `1`.

---

### **87. What does this print?**

```js
console.log([] == false);
console.log([] === false);
console.log(false == []);
console.log(false === []);
```

**Output**:
- `false`
- `false`
- `false`
- `false`

**Explanation**: Arrays and booleans are different types, so neither `==` nor `===` will be true.

---

### **88. What’s the result?**

```js
console.log('1' - - '1');
console.log('1' + - '1');
```

**Output**:
- `2`
- `'0'`

**Explanation**:
- `'1' - - '1'` is equivalent to `1 - (-1)`, which is `2`.
- `'1' + - '1'` is `'1' + -1`, resulting in `'0'`.

---

### **89. What will this code print?**

```js
console.log([] == ![]);
console.log([] === ![]);
```

**Output**:
- `true`
- `false`

**Explanation**: 
- `![]` evaluates to `false`, and `[] == false` is `true` due to type coercion.
- `[] === ![]` is `false` because they are different types.

---

### **90. What does this code print?**

```js
console.log([] + {} + []);
console.log([{}] + []);
```

**Output**:
- `"[object Object]"`
- `"[object Object]"`

**Explanation**: 
- `[]` coerces to an empty string `""`, `{}` to `[object Object]`.
- `[{}] + []` results in `[object Object]`.

---

### **91. What is the output?**

```js
console.log([1] == 1);
console.log([1] === 1);
console.log([1] == [1]);
console.log([1] === [1]);
```

**Output**:
- `false`
- `false`
- `false`
- `false`

**Explanation**: 
- Arrays are compared by reference, so different instances are not equal.

---

### **92. What does this print?**

```js
console.log([] + []);
console.log([] - []);
```

**Output**:
- `""`
- `NaN`

**Explanation**:
- `[] + []` results in an empty string.
- `[] - []` results in `NaN` due to the subtraction operation with arrays.

---

### **93. What’s the result of this?**

```js
console.log(0 == '0');
console.log(0 === '0');
console.log('0' == 0);
console.log('0' === 0);
```

**Output**:
- `true`
- `false`
- `true`
- `false`

**Explanation**: 
- `==` performs type coercion, so `0 == '0'` is `true`.
- `===` checks for strict equality.

---

### **94. What will this return?**

```js
console.log('1' == 1);
console.log('1' === 1);
console.log('1' != 1);
console.log('1' !== 1);
```

**Output**:
- `true`
- `false`
- `false`
- `true`

**Explanation**:
- `==` coerces types, while `===` does not.

---

### **95. What does this code print?**

```js
console.log([1, 2] == [1, 2]);
console.log([1, 2] === [1, 2]);
```

**Output**:
- `false`
- `false`

**Explanation**: Arrays are compared by reference, so different instances are not equal.

---

### **96. What will this code return?**

```js
console.log(null == undefined);
console.log(null === undefined);
console.log(null == 0);
console.log(undefined == 0);
```

**Output**:
- `true`
- `false`
- `false`
- `false`

**Explanation**:


- `null` and `undefined` are loosely equal but not strictly equal.
- `null` and `undefined` are not equal to `0`.

---

### **97. What does this code print?**

```js
console.log('5' - 3);
console.log('5' * 2);
console.log('5' / 2);
```

**Output**:
- `2`
- `10`
- `2.5`

**Explanation**:
- `-` converts `'5'` to a number for subtraction.
- `*` and `/` also coerce `'5'` to a number for operations.

---

### **98. What will this return?**

```js
console.log([] == ![]);
console.log([] === ![]);
```

**Output**:
- `true`
- `false`

**Explanation**:
- `![]` evaluates to `false`, so `[] == false` is `true`.
- `[] === ![]` is `false` due to different types.

---

### **99. What does this print?**

```js
console.log(0.1 + 0.2 === 0.3);
```

**Output**: `false`

**Explanation**: Due to floating-point precision issues, `0.1 + 0.2` does not exactly equal `0.3`.

---

### **100. What will this code return?**

```js
console.log([] + {} + []);
console.log([{}] + []);
```

**Output**:
- `"[object Object]"`
- `"[object Object]"`

**Explanation**:
- `[] + {} + []` results in the empty string and object coercion to `[object Object]`.
- `[{}] + []` results in `[object Object]`.





### Arrays

1. **What does this code print?**
   ```js
   console.log([1] + [2]);
   ```
   **Output**: `"12"`
   **Explanation**: Arrays are coerced into strings and concatenated.

2. **What is the result of this code?**
   ```js
   console.log([1, 2, 3].slice(1, 2));
   ```
   **Output**: `[2]`
   **Explanation**: `slice` extracts elements from index 1 to 2 (exclusive).

3. **What will this code output?**
   ```js
   console.log([1, 2, 3].map(x => x * x));
   ```
   **Output**: `[1, 4, 9]`
   **Explanation**: `map` applies the function to each element.

4. **What does this code print?**
   ```js
   console.log([1, 2, 3].filter(x => x > 1));
   ```
   **Output**: `[2, 3]`
   **Explanation**: `filter` keeps elements greater than 1.

5. **What is the result of this code?**
   ```js
   console.log([1, 2, 3].reduce((a, b) => a + b));
   ```
   **Output**: `6`
   **Explanation**: `reduce` sums up the elements.

6. **What will this code print?**
   ```js
   console.log([1, 2, 3].concat([4, 5]));
   ```
   **Output**: `[1, 2, 3, 4, 5]`
   **Explanation**: `concat` merges arrays.

7. **What does this code return?**
   ```js
   console.log([1, 2, 3].includes(2));
   ```
   **Output**: `true`
   **Explanation**: `includes` checks if the element exists in the array.

8. **What is the output?**
   ```js
   console.log([1, [2, [3]]].flat(2));
   ```
   **Output**: `[1, 2, 3]`
   **Explanation**: `flat` flattens nested arrays.

9. **What will this code print?**
   ```js
   console.log([1, 2, 3].find(x => x > 1));
   ```
   **Output**: `2`
   **Explanation**: `find` returns the first element that satisfies the condition.

10. **What does this code return?**
    ```js
    console.log([1, 2, 3].findIndex(x => x === 2));
    ```
    **Output**: `1`
    **Explanation**: `findIndex` returns the index of the first element that satisfies the condition.

### Objects

11. **What does this code print?**
    ```js
    const obj = {a: 1, b: 2};
    console.log(Object.keys(obj));
    ```
    **Output**: `["a", "b"]`
    **Explanation**: `Object.keys` returns the keys of an object.

12. **What is the result of this code?**
    ```js
    const obj = {a: 1, b: 2};
    console.log(Object.values(obj));
    ```
    **Output**: `[1, 2]`
    **Explanation**: `Object.values` returns the values of an object.

13. **What will this code print?**
    ```js
    const obj = {a: 1};
    obj.a = 2;
    console.log(obj);
    ```
    **Output**: `{a: 2}`
    **Explanation**: The value of `a` is updated.

14. **What does this code return?**
    ```js
    console.log({a: 1} instanceof Object);
    ```
    **Output**: `true`
    **Explanation**: `{a: 1}` is an instance of `Object`.

15. **What will this code print?**
    ```js
    const obj1 = {a: 1};
    const obj2 = Object.create(obj1);
    console.log(obj2.a);
    ```
    **Output**: `1`
    **Explanation**: `Object.create` creates an object with `obj1` as its prototype.

16. **What does this code return?**
    ```js
    console.log({...{a: 1}});
    ```
    **Output**: `{a: 1}`
    **Explanation**: The spread operator creates a shallow copy of the object.

17. **What is the output?**
    ```js
    const obj = {a: 1};
    delete obj.a;
    console.log(obj);
    ```
    **Output**: `{}`
    **Explanation**: `delete` removes a property from an object.

18. **What does this code print?**
    ```js
    console.log({a: 1, a: 2});
    ```
    **Output**: `{a: 2}`
    **Explanation**: Duplicate keys in objects are overwritten.

19. **What will this code output?**
    ```js
    console.log(Object.entries({a: 1, b: 2}));
    ```
    **Output**: `[["a", 1], ["b", 2]]`
    **Explanation**: `Object.entries` returns an array of key-value pairs.

20. **What does this code return?**
    ```js
    console.log(Object.assign({}, {a: 1}, {b: 2}));
    ```
    **Output**: `{a: 1, b: 2}`
    **Explanation**: `Object.assign` merges objects.

### Functions

21. **What does this code print?**
    ```js
    function foo() {
        return
        {
            bar: 1
        };
    }
    console.log(foo());
    ```
    **Output**: `undefined`
    **Explanation**: The function implicitly returns `undefined` because of the newline.

22. **What is the result of this code?**
    ```js
    function foo(a, b) {
        console.log(a, b);
    }
    foo(1);
    ```
    **Output**: `1 undefined`
    **Explanation**: `b` is `undefined` because it was not provided.

23. **What will this code print?**
    ```js
    const add = (a, b = 2) => a + b;
    console.log(add(3));
    ```
    **Output**: `5`
    **Explanation**: The default value for `b` is used.

24. **What does this code print?**
    ```js
    function foo(a, b = () => a) {
        return b();
    }
    console.log(foo(1));
    ```
    **Output**: `1`
    **Explanation**: `b` is a function returning `a`.

25. **What will this code return?**
    ```js
    function add(a, ...rest) {
        return a + rest.reduce((acc, num) => acc + num, 0);
    }
    console.log(add(1, 2, 3, 4));
    ```
    **Output**: `10`
    **Explanation**: `...rest` collects remaining arguments into an array.

26. **What does this code print?**
    ```js
    const obj = {a: 1};
    function bar() {
        console.log(this.a);
    }
    bar.call(obj);
    ```
    **Output**: `1`
    **Explanation**: `call` sets `this` to `obj`.

27. **What will this code output?**
    ```js
    const obj = {a: 1};
    function bar() {
        console.log(this.a);
    }
    bar.bind(obj)();
    ```
    **Output**: `1`
    **Explanation**: `bind` sets `this` permanently.

28. **What does this code print?**
    ```js
    function foo(a, b = (a = 2) => a) {
        return b();
    }
    console.log(foo(1));
    ```
    **Output**: `2`
    **Explanation**: The default function parameter modifies `a`.

29. **What is the output?**
    ```js
    const add = (a, b) => a + b;
    console.log(add(2, 3));
    ```
    **Output**: `5`
    **Explanation**: Arrow function returns the sum of `a` and `b`.

30. **What does this code print?**
    ```js
    const multiply = (a, b = 1) => a * b;
    console.log(multiply(5));
    ```
    **Output**: `5`
    **Explanation**: Default value for `b` is used.

### Call Stack

31. **What does this code print?**
    ```js
    function foo() {
        console.log('foo');
    }
    function bar() {
        foo();
    }
    bar();
    ```
    **Output**: `foo`
    **Explanation**: `bar` calls `foo`, which prints `foo`.

32

. **What will this code output?**
    ```js
    function baz() {
        console.log('baz');
        foo();
    }
    function foo() {
        console.log('foo');
    }
    baz();
    ```
    **Output**:
    ```
    baz
    foo
    ```
    **Explanation**: `baz` prints `baz`, then calls `foo`.

33. **What does this code print?**
    ```js
    function a() {
        b();
    }
    function b() {
        console.log('b');
    }
    a();
    ```
    **Output**: `b`
    **Explanation**: `a` calls `b`, which prints `b`.

34. **What will this code output?**
    ```js
    function one() {
        setTimeout(() => console.log('one'), 0);
    }
    function two() {
        console.log('two');
    }
    one();
    two();
    ```
    **Output**:
    ```
    two
    one
    ```
    **Explanation**: `two` prints first, then `setTimeout` executes.

35. **What does this code print?**
    ```js
    function foo() {
        console.log('foo');
    }
    function bar() {
        console.log('bar');
    }
    foo();
    bar();
    ```
    **Output**:
    ```
    foo
    bar
    ```
    **Explanation**: `foo` and `bar` are called sequentially.

36. **What will this code output?**
    ```js
    function foo() {
        bar();
        console.log('foo');
    }
    function bar() {
        console.log('bar');
    }
    foo();
    ```
    **Output**:
    ```
    bar
    foo
    ```
    **Explanation**: `foo` calls `bar`, then prints `foo`.

37. **What does this code print?**
    ```js
    function a() {
        console.log('a');
    }
    function b() {
        console.log('b');
        a();
    }
    b();
    ```
    **Output**:
    ```
    b
    a
    ```
    **Explanation**: `b` prints `b`, then calls `a`.

38. **What will this code output?**
    ```js
    function foo() {
        bar();
    }
    function bar() {
        console.log('bar');
    }
    foo();
    ```
    **Output**: `bar`
    **Explanation**: `foo` calls `bar`.

39. **What does this code print?**
    ```js
    function foo() {
        console.log('foo');
        setTimeout(() => console.log('foo timeout'), 0);
    }
    foo();
    ```
    **Output**:
    ```
    foo
    foo timeout
    ```
    **Explanation**: `setTimeout` executes after the stack is clear.

40. **What will this code print?**
    ```js
    function foo() {
        console.log('foo');
        bar();
    }
    function bar() {
        console.log('bar');
    }
    foo();
    ```
    **Output**:
    ```
    foo
    bar
    ```
    **Explanation**: `foo` prints `foo`, then calls `bar`.

### Promises

41. **What does this code print?**
    ```js
    new Promise(resolve => resolve('done'))
        .then(result => console.log(result));
    ```
    **Output**: `done`
    **Explanation**: `resolve` triggers the `then` callback.

42. **What is the result of this code?**
    ```js
    new Promise((resolve, reject) => reject('error'))
        .catch(err => console.log(err));
    ```
    **Output**: `error`
    **Explanation**: `catch` handles rejected promises.

43. **What will this code output?**
    ```js
    const promise = new Promise(resolve => resolve(1));
    promise.then(x => x + 1).then(x => console.log(x));
    ```
    **Output**: `2`
    **Explanation**: Chained promises process `x` sequentially.

44. **What does this code print?**
    ```js
    new Promise(resolve => setTimeout(() => resolve('done'), 1000))
        .then(result => console.log(result));
    ```
    **Output**: `done` (after 1 second)
    **Explanation**: `setTimeout` delays the promise resolution.

45. **What will this code output?**
    ```js
    const promise = Promise.resolve('resolved');
    promise.then(console.log).catch(console.error);
    ```
    **Output**: `resolved`
    **Explanation**: `Promise.resolve` immediately resolves.

46. **What does this code print?**
    ```js
    new Promise((resolve, reject) => resolve('done'))
        .then(() => { throw new Error('error'); })
        .catch(err => console.log(err.message));
    ```
    **Output**: `error`
    **Explanation**: Error thrown in the `then` is caught by `catch`.

47. **What will this code output?**
    ```js
    Promise.all([Promise.resolve(1), Promise.resolve(2)])
        .then(results => console.log(results));
    ```
    **Output**: `[1, 2]`
    **Explanation**: `Promise.all` resolves when all promises resolve.

48. **What does this code print?**
    ```js
    Promise.race([Promise.resolve(1), new Promise(resolve => setTimeout(() => resolve(2), 1000))])
        .then(result => console.log(result));
    ```
    **Output**: `1`
    **Explanation**: `Promise.race` returns the result of the first resolved promise.

49. **What will this code output?**
    ```js
    const promise = new Promise((resolve, reject) => {
        setTimeout(() => resolve('done'), 500);
        setTimeout(() => reject('error'), 100);
    });
    promise.then(console.log).catch(console.error);
    ```
    **Output**: `error`
    **Explanation**: The first `setTimeout` rejects the promise before the second resolves.

50. **What does this code print?**
    ```js
    const p1 = new Promise((resolve, reject) => setTimeout(resolve, 1000));
    const p2 = new Promise((resolve, reject) => setTimeout(resolve, 2000));
    Promise.all([p1, p2]).then(() => console.log('done'));
    ```
    **Output**: `done` (after 2 seconds)
    **Explanation**: `Promise.all` waits for all promises to resolve.

### Asynchronous Functions

51. **What does this code print?**
    ```js
    async function foo() {
        return 1;
    }
    foo().then(console.log);
    ```
    **Output**: `1`
    **Explanation**: `async` functions return a promise with the resolved value.

52. **What is the result of this code?**
    ```js
    async function foo() {
        return Promise.resolve(2);
    }
    foo().then(console.log);
    ```
    **Output**: `2`
    **Explanation**: The returned promise resolves to `2`.

53. **What will this code output?**
    ```js
    async function foo() {
        throw new Error('error');
    }
    foo().catch(console.error);
    ```
    **Output**: `Error: error`
    **Explanation**: Errors in `async` functions are caught in `catch`.

54. **What does this code print?**
    ```js
    async function foo() {
        await new Promise(resolve => setTimeout(() => resolve('done'), 1000));
        console.log('foo');
    }
    foo();
    ```
    **Output**: `foo` (after 1 second)
    **Explanation**: `await` waits for the promise to resolve before printing.

55. **What will this code output?**
    ```js
    async function foo() {
        const result = await Promise.all([
            new Promise(resolve => setTimeout(() => resolve('a'), 100)),
            new Promise(resolve => setTimeout(() => resolve('b'), 200))
        ]);
        console.log(result);
    }
    foo();
    ```
    **Output**: `['a', 'b']`
    **Explanation**: `Promise.all` waits for all promises to resolve.

56. **What does this code print?**
    ```js
    async function foo() {
        console.log(await 1);
    }
    foo();
    ```
    **Output**: `1`
    **Explanation**: `await` resolves immediately for non-promise values.

57. **What will this code output?**
    ```js
    async function foo() {
        const x = await 1;
        console.log(x);
    }
    foo();
    ```
    **Output**: `1`
    **Explanation**: `await` returns the resolved value directly.

58. **What does this code print?**
    ```js
    async function foo() {
        const x = await new Promise(resolve => setTimeout(() => resolve('done'), 500));
        console.log(x);
    }
    foo();
    ```
    **Output**: `done` (after 0.5 seconds)
    **Explanation**: `await` waits for the promise to resolve.

59. **What will this code output?**
    ```js
    async function foo() {
        const x = await Promise.reject('error');
        console.log(x);
    }
    foo

().catch(console.error);
    ```
    **Output**: `error`
    **Explanation**: Rejected promises are caught in `catch`.

60. **What does this code print?**
    ```js
    async function foo() {
        try {
            const result = await new Promise((resolve, reject) => reject('error'));
            console.log(result);
        } catch (e) {
            console.log(e);
        }
    }
    foo();
    ```
    **Output**: `error`
    **Explanation**: Errors are caught in `catch` block.

### Event Phases

61. **What does this code print?**
    ```js
    document.body.addEventListener('click', () => console.log('clicked'), true);
    document.body.addEventListener('click', () => console.log('clicked again'));
    document.body.click();
    ```
    **Output**:
    ```
    clicked
    clicked again
    ```
    **Explanation**: The event captures and bubbles through phases.

62. **What is the result of this code?**
    ```js
    document.addEventListener('click', function(event) {
        console.log('Event at document');
    }, true);
    document.body.addEventListener('click', function(event) {
        console.log('Event at body');
    }, true);
    document.body.click();
    ```
    **Output**:
    ```
    Event at document
    Event at body
    ```
    **Explanation**: The event is captured at each phase.

63. **What will this code output?**
    ```js
    document.body.addEventListener('click', () => console.log('body'), false);
    document.body.addEventListener('click', () => console.log('body again'), true);
    document.body.click();
    ```
    **Output**:
    ```
    body again
    body
    ```
    **Explanation**: `true` indicates capturing phase, `false` is bubbling phase.

64. **What does this code print?**
    ```js
    document.addEventListener('click', function() {
        console.log('clicked');
    }, false);
    document.body.click();
    ```
    **Output**: `clicked`
    **Explanation**: The event is propagated to the document from the body.

65. **What will this code output?**
    ```js
    document.body.addEventListener('click', function() {
        console.log('body clicked');
    });
    document.body.addEventListener('click', function(event) {
        event.stopImmediatePropagation();
        console.log('immediate stop');
    });
    document.body.click();
    ```
    **Output**:
    ```
    immediate stop
    ```
    **Explanation**: `stopImmediatePropagation` prevents further propagation.

66. **What does this code print?**
    ```js
    document.body.addEventListener('click', () => console.log('body'));
    document.body.removeEventListener('click', () => console.log('body'));
    document.body.click();
    ```
    **Output**: (Nothing)
    **Explanation**: `removeEventListener` does not remove the listener due to a different function reference.

67. **What will this code output?**
    ```js
    document.body.addEventListener('click', function() {
        console.log('event handler');
    });
    document.body.dispatchEvent(new Event('click'));
    ```
    **Output**: `event handler`
    **Explanation**: `dispatchEvent` triggers the event handler.

68. **What does this code print?**
    ```js
    document.body.addEventListener('click', function() {
        console.log('event fired');
    }, true);
    document.body.click();
    ```
    **Output**: `event fired`
    **Explanation**: Capturing phase is used, so the event is caught.

69. **What will this code output?**
    ```js
    const handler = () => console.log('handler');
    document.body.addEventListener('click', handler);
    document.body.removeEventListener('click', handler);
    document.body.click();
    ```
    **Output**: (Nothing)
    **Explanation**: Event handler is removed before being called.

70. **What does this code print?**
    ```js
    document.addEventListener('click', function(event) {
        event.stopPropagation();
        console.log('stop propagation');
    }, true);
    document.body.addEventListener('click', function() {
        console.log('body click');
    });
    document.body.click();
    ```
    **Output**:
    ```
    stop propagation
    ```
    **Explanation**: `stopPropagation` prevents bubbling.

### DOM Manipulation

71. **What does this code print?**
    ```js
    document.body.innerHTML = '<div id="test">Test</div>';
    console.log(document.getElementById('test').innerText);
    ```
    **Output**: `Test`
    **Explanation**: `innerText` returns the content of the element.

72. **What is the result of this code?**
    ```js
    const div = document.createElement('div');
    div.setAttribute('class', 'my-class');
    console.log(div.className);
    ```
    **Output**: `my-class`
    **Explanation**: `className` returns the class attribute.

73. **What will this code output?**
    ```js
    document.body.innerHTML = '<p id="para">Hello</p>';
    const p = document.getElementById('para');
    p.textContent = 'World';
    console.log(p.innerHTML);
    ```
    **Output**: `World`
    **Explanation**: `textContent` updates the text inside the element.

74. **What does this code print?**
    ```js
    document.body.innerHTML = '<button id="btn">Click me</button>';
    const button = document.getElementById('btn');
    button.onclick = () => console.log('Button clicked');
    button.click();
    ```
    **Output**: `Button clicked`
    **Explanation**: `onclick` triggers the event handler.

75. **What will this code output?**
    ```js
    const div = document.createElement('div');
    div.style.color = 'red';
    document.body.appendChild(div);
    console.log(getComputedStyle(div).color);
    ```
    **Output**: `rgb(255, 0, 0)`
    **Explanation**: `getComputedStyle` returns the computed style.

76. **What does this code print?**
    ```js
    document.body.innerHTML = '<ul><li>Item 1</li><li>Item 2</li></ul>';
    const items = document.querySelectorAll('li');
    items.forEach(item => console.log(item.textContent));
    ```
    **Output**:
    ```
    Item 1
    Item 2
    ```
    **Explanation**: `querySelectorAll` selects multiple elements.

77. **What will this code output?**
    ```js
    const div = document.createElement('div');
    div.textContent = 'Hello World';
    document.body.appendChild(div);
    div.remove();
    console.log(document.body.contains(div));
    ```
    **Output**: `false`
    **Explanation**: `remove` detaches the element from the DOM.

78. **What does this code print?**
    ```js
    document.body.innerHTML = '<input type="text" id="input" value="default">';
    const input = document.getElementById('input');
    input.value = 'changed';
    console.log(input.getAttribute('value'));
    ```
    **Output**: `default`
    **Explanation**: `getAttribute` returns the initial attribute value.

79. **What will this code output?**
    ```js
    document.body.innerHTML = '<div id="test"></div>';
    const div = document.getElementById('test');
    div.setAttribute('data-test', 'value');
    console.log(div.dataset.test);
    ```
    **Output**: `value`
    **Explanation**: `dataset` accesses `data-*` attributes.

80. **What does this code print?**
    ```js
    const p = document.createElement('p');
    p.innerHTML = '<strong>Strong</strong>';
    document.body.appendChild(p);
    console.log(p.querySelector('strong').innerHTML);
    ```
    **Output**: `Strong`
    **Explanation**: `querySelector` selects nested elements.

### Core JavaScript Concepts

81. **What does this code print?**
    ```js
    console.log(typeof null);
    ```
    **Output**: `object`
    **Explanation**: `null` is considered an object due to a historical bug.

82. **What is the result of this code?**
    ```js
    console.log(0.1 + 0.2 === 0.3);
    ```
    **Output**: `false`
    **Explanation**: Floating-point arithmetic can lead to precision issues.

83. **What will this code output?**
    ```js
    console.log([1] == [1]);
    ```
    **Output**: `false`
    **Explanation**: Arrays are compared by reference, not value.

84. **What does this code print?**
    ```js
    console.log(1 + '1');
    ```
    **Output**: `11`
    **Explanation**: `1` is coerced into a string, resulting in concatenation.

85. **What will this code output?**
    ```js
    console.log('5' - 2);
    ```
    **Output**: `3`
    **Explanation**: The `-` operator converts the string to a number.

86. **What does this

 code print?**
    ```js
    console.log(true + 1);
    ```
    **Output**: `2`
    **Explanation**: `true` is coerced to `1` before addition.

87. **What will this code output?**
    ```js
    console.log([] + {});
    ```
    **Output**: `[object Object]`
    **Explanation**: `[]` is coerced to an empty string, `{}` to `[object Object]`.

88. **What does this code print?**
    ```js
    console.log({} + []);
    ```
    **Output**: `0`
    **Explanation**: `{}` is interpreted as a block, `[]` is coerced to `0`.

89. **What will this code output?**
    ```js
    console.log(NaN === NaN);
    ```
    **Output**: `false`
    **Explanation**: `NaN` is not equal to itself.

90. **What does this code print?**
    ```js
    console.log(typeof typeof 1);
    ```
    **Output**: `string`
    **Explanation**: `typeof 1` is `number`, `typeof` of that is `string`.

91. **What will this code output?**
    ```js
    console.log([1, 2] + [3, 4]);
    ```
    **Output**: `1,23,4`
    **Explanation**: Arrays are converted to strings and concatenated.

92. **What does this code print?**
    ```js
    console.log(1 + '2' + 3);
    ```
    **Output**: `123`
    **Explanation**: The `+` operator performs string concatenation when one operand is a string.

93. **What will this code output?**
    ```js
    console.log(1 - '1');
    ```
    **Output**: `0`
    **Explanation**: The `-` operator converts the string to a number.

94. **What does this code print?**
    ```js
    console.log(typeof [] === 'object');
    ```
    **Output**: `true`
    **Explanation**: Arrays are objects in JavaScript.

95. **What will this code output?**
    ```js
    console.log([] == ![]);
    ```
    **Output**: `true`
    **Explanation**: `![]` is `false`, `[]` is coerced to `false`.

96. **What does this code print?**
    ```js
    console.log([1] + [2]);
    ```
    **Output**: `12`
    **Explanation**: Arrays are converted to strings and concatenated.

97. **What will this code output?**
    ```js
    console.log({a: 1} + {b: 2});
    ```
    **Output**: `[object Object][object Object]`
    **Explanation**: Objects are coerced to strings and concatenated.

98. **What does this code print?**
    ```js
    console.log(2 + 3 + '4');
    ```
    **Output**: `54`
    **Explanation**: Addition with a string converts the entire result to a string.

99. **What will this code output?**
    ```js
    console.log(0.1 + 0.2);
    ```
    **Output**: `0.30000000000000004`
    **Explanation**: Floating-point arithmetic can cause precision issues.

100. **What does this code print?**
    ```js
    console.log([] == false);
    ```
    **Output**: `false`
    **Explanation**: `[]` is coerced to a falsy value, but not `false`.

---

 
