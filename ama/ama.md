### 1. Difference between '==' and '==='.

- While trying to equate values of 2 variables that are of different types,

  - `==`, converts one of the types to the type of another variable and check for their equality. (type coercion), so returns true if the value is same even though they are of different data types.

  - `===`, is a strict equality operator, which means it strictly check for same data type values, and returns true only when both type and values are same.

### 2. Why is typeof `[]` gives an object?

- Arrays are specialised objects in Js.
- Arrays inherit from `Array.prototype` which is in `Object.prototype`, which means arraya are objects at their core.
- To check the type accurately, `Array.isArray([])` holds true, or `[] instanceof Array`, holds true.

### 3. Disadvantages of closure

- Memory consumption

  - As long as closures are active in the program, the memory can't be garbage collected.
  - If we are using closure in ten places, unless all the ten process complete it holds the memory which cause memory leak
  - **Solution** - When we are done using closure at any point in our program, we need to set the closure to `null`.

- Increases code complexity

### 4. Why using global variables is not a best practice in Js?

- When a variable in declared in global scope, it is available at any part in program, which may give chances to unintensionally override the variable with different values.
- Also makes it difficult to debugg when any error occurs with such variables.
  - So instead declare variables in any function or block where it needs to be used.

### 5. How to extract certain properties from an array of objects to create a new array ?

- Map method on arrays return an array as a result with the specification provided to it.

### 6. Difference between charAt() and at() method in js ?

- `charAt()`, returns the character at the specified index in a string.
  - doesn't handle negative indexes, they are treated as 0.
  - returns an empty string if the index is out of range.
- `at()`, returns the character at a specified index in a string, or an element at a specified index in an array.
  - handles negative indexes as well, which count from the end of the string.
  - returns undefined for the index that is out of range.
- `charAt()`, is older method in js,
- `at()`, is most recently added in js and provides more flexibility with negative indexes.

### 7. How to reset initial or 1st commit in git, if its possible ?

- Using `git rebase`

  - identify the commit hash with `git log --oneline`,
  - rebase to the commit, `git rebase -i <commit_hash>`, (can also use HEAD~n, where n is the no.of commits to traverse back)
  - modify commit with `git commit --amend` or `git reset`,
  - countinue the rebase `git rebase --continue`

- using `git reset`,

  - using `git reset --hard <commit_hash>`, this will erase the history and rewrites with the new changes.

  - best practice for shared repository
    - `git checkout -b new-branch-name`, creates a new branch and make changes using `git rebase -i`

### 8. console.log(typeof []) returns 'object', then why can not we use (.) operator in array to accesss its values just like objects,where we use (.) operator in objects for accessing key and values.

- Dot notation expects a valid JavaScript identifier following the dot (`.`).
- Numeric indices are not valid identifiers in JavaScript, hence you cannot use dot notation directly with array elements.
- Bracket notation (`[]`) allows you to dynamically access properties or array elements using expressions, including numeric indices.

### 9. Why 'forEach' loop skips 'not defined' whereas 'for' loop gives 'undefined' ?

- `for` Loop: Accesses the array directly by index.
- If the index does not have a defined value, it returns undefined.

- `forEach` Loop: Calls the provided callback function only for array elements that are actually present.
- If an index in the array is missing, forEach skips it.

### 10. How can we mimic the action Array.splice and 'Array.slice' on objcts.

- there are no built-in methods like `splice` or `slice` for objects.
- we can do the operations by writing custom functions.

### 11. What is "Callback Hell" problem and how to avoid it ?

- "Callback Hell," also known as "Pyramid of Doom," refers to the situation in JavaScript where multiple nested callbacks make the code difficult to read and maintain.

- This problem arises when asynchronous operations are chained together in a way that each callback depends on the result of the previous one, leading to deeply nested and hard-to-follow code structures.

**solution** Breaking down code into smaller, reusable functions can help manage complexity.

- promises for async operations,
- async / await
- try / catch to handle error

### 12.

### //file1.js

```
let ar = [1,2,3];
console.log("Hello");
module.exports.ar = ar;
```

### //file2.js

```
const {ar} = require('file1.js');
let print = ar;
console.log(print);
```

### Output: "Hello"

### [1,2,3]

### why "Hello" is also printing ? when we have exported array('ar') only!

- The reason "Hello" is being printed when you run file2.js is because the require function in Node.js executes the entire module (in this case, file1.js) when it is first required.
- This means that all the code in file1.js is executed, not just the part that assigns to module.exports.
