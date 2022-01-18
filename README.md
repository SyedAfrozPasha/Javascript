# Data Structures and Algorithms in JavaScript

## Big O Notation

- Big O notation is used to measure how the run time or space requirements for your program grow as input size grows.

- Big O Notation can give us a high level understanding of the time or space complexity of an algorithm.

- Big O Notation doesn't care about precision, only about general trends (linear? quadratic? constant?)

- The time or space complexity (as measured by Big O) depends only on the algorithm, not the hardware used to run the algorithm.

### Time Complexity - General Explanation

- In time complexity, we analyze the runtime of an algorithm/program as the size of the inputs increases.

- Let us consider a function with input `n` -> `f(n)`

  - `f(n)` is said to be *linear* (`f(n) = m`), if number of operations required is equal to `m`.
  - `f(n)` could be *quadratic* (`f(n) = m^2`), if number of operations required is equal to `m^2`.
  - `f(n)` could be *constant* (`f(n) = 1`), if number of operations required is equal to 1 or any constant value.

### Time Complexity - Example

- Let us consider a function with two different approaches which adds up to `n` numbers and give back the results.

  ```javascript
  // Approach 1 - Using simple formula
  function addUpTo(n) {
    return n * (n + 1) / 2;
  }

  // Approach 2 - Using loop
  function addUpTo(n) {
    let sum = 0;
    for (let i = 0; i <= n; i++) {
      sum += i;
    }
    return sum;
  }
  ```

- Both these functions calculate the sum of numbers up to `n`. But how will you identify which approach is better. Here comes the Big O notation to the picture. Big O notation help to identifies the best approach by fuzzy calculations of number of operations a particular function/program required to given an output.

- Approach 1 has total three operations (`*`, `+` and `/`). A computer/system need to perform only 3 operation irrespective of the size of the input `n`. So the Big O (time) complexity of this approach is `O(1)`.

  ```javascript
  // Approach 1
  function addUpTo(n) {
    return n * (n + 1) / 2; // Always 3 constant operations
  }
  ```

- In approach 2, number of operations are bounded by a multiple of `n`. Lets say `n = 5`, then two separate addition operation (`i++` and `sum += i`) will get executed `n` times (i.e. 5 times), which makes the total of `5n` + `5n` = `10n` operations. We ignore the constant value `10` and consider only `n`. So the Big O (time) complexity of this approach will be `O(n)`.

  ```javascript
  // Approach 2
  function addUpTo(n) {
    let sum = 0;
    for (let i = 0; i <= n; i++) { // `+` is part of loop, so it's a n times `+` operations
      sum += i; // `+` is inside a loop, so it's a n times `+` operations
    }
    return sum;
  }
  ```

- Let us consider another example where we have nested loops. What will be Big O notation of this function?

  ```javascript
  function printAllPairs(n) {
    for(let i = 0; i < n; i++) { // Loop 1 -> O(n) operations
      for(let j = 0; i < n; j++) { // Loop 2 -> O(n) operations
        console.log(i, j);
      
    }
  }
  ```

- Here we have nested loop which means we are performing `O(n)` operation (loop 1) inside an `O(n)` operation (loop 2). So here the overall complexity is `O(n) * O(n) = O(n * n) = O(n^2)`.

### Simplifying Big O Expressions

- Counting the number operations in a program can be hard.
- Number of operations are grows roughly proportionally with `n` (number of inputs). i.e. If `n` doubles, the number of operations will also roughly doubles.
- Constants doesn't matters. `O(2n)` can simplified as `O(n)`. Likewise `O(500)` can simplified as `O(1)`. And also smaller terms doesn't matter.
  
  ```javascript
  O(2n)           => O(n)
  O(500)          => O(1)
  O(2n^2)         => O(n^2)
  O(n + 10)       => O(n)
  O(1000n + 50)   => O(n)
  O(n^2 + 5n + 8) => O(n^2)
  ```

- Arithmetic operations (`+`, `-`, `*`, etc.) are constant.

- Variable assignment is constant.

- Accessing elements in an array (by index) or object (by key) is constant.

- In a loop, the the complexity is the length of the loop times the complexity of whatever happens inside of the loop.

- For Big O complexity always consider the scenario where input (`n`) grows larger or infinity.

### Space Complexity - General Explanation

- In space complexity, we analyze how much additional memory do we need to allocate in order to run the code in our algorithm.

- For space complexity, we only care about the auxiliary space complexity. Auxiliary space complexity refer to the space required by the algorithm, not including space taken up by the inputs.

- Most primitives (`booleans`, `numbers`, `undefined`, `null`) are constant space.

- Strings require `O(n)` space (where `n` is the string length).

- Reference types (objects and arrays) are generally `O(n)`, where `n` is the length (for arrays) or the number of keys (for objects).

### Space Complexity - Example

- Let's analyze the space complexity for the below example. Here we are using two variables to assign the values (`sum` and `i`) with the complexity of `O(1)` each. So the overall space complexity will be `O(1) + O(1) = O(1+1) = O(2) => O(1)`.

  ```javascript
  function sum(arr) {
    let sum = 0; // O(1)
    for (let i = 0; i < arr.length; i++) { // O(1)
      sum += arr[i];
    }
    return sum;
  }
  ```

- Another example with `O(n)` space complexity.

  ```javascript
  function double(arr) {
    let newArr = []; // O(1)
    for (let i = 0; i < arr.length; i++) { // O(1)
      newArr.push(2 * arr[i]); // O(n) - space taken by array is directly proportional to input length.
    }
    return newArr;
  }
  ```

- In the above example, as the array length grows space also grows in proportion. So the space complexity is `O(n)`.

### Logarithmic Big O Expressions

- Sometimes big O expressions involve more complex mathematical expressions like logarithm.

- The **Logarithm** of a number roughly measures the number of times you can divide that number by 2 **before you get a value that's less than or equal to one**.

- Logarithmic time complexity (`O(log n)`) is great.

- Certain searching algorithms have logarithmic time complexity.

- Efficient sorting algorithms involve logarithms.

- Recursion sometimes involves logarithmic space complexity.

## Analyzing Performance of Arrays and Objects in JavaScript

### Objects

- **Objects** are unordered data structure which stores the values as key-value pairs.

### When to use objects

- When you don't need order.
- When you need fast access / insertion and removal.

### Object operations and Big O Expression

| Operation    | Big O Expression |
|--------------|:----------------:|
| Insertion    | `O(1)`           |
| Removal      | `O(1)`           |
| Searching    | `O(N)`           |
| Access       | `O(1)`           |

### Object methods and Big O Expression

| Methods          | Big O Expression |
|------------------|:----------------:|
| `Object.keys`    | `O(N)`           |
| `Object.values`  | `O(N)`           |
| `Object.entries` | `O(N)`           |
| `hasOwnProperty` | `O(1)`           |

### Arrays

- **Arrays** are ordered data structure which stores the values in each index.

### When to use arrays

- When you need order
- When you need fast access / insertion and removal.

### Array operations and Big O Expression

| Operation    | Big O Expression |
|--------------|:----------------|
| Insertion    | It depends (faster if we are inserting at the last of an array `O(1)`, otherwise it may be slower (`O(N)`))      |
| Removal      | It depends (faster if we are removing at the last of an array `O(1)`, otherwise it may be slower (`O(N)`))      |
| Searching    | `O(N)`           |
| Access       | `O(1)`           |

### Array methods and Big O Expression

| Methods          | Big O Expression |
|------------------|:----------------:|
| `push`           | `O(1)`           |
| `pop`            | `O(1)`           |
| `shift`          | `O(N)`           |
| `unshift`        | `O(N)`           |
| `concat`         | `O(N)`           |
| `slice`          | `O(N)`           |
| `splice`         | `O(N)`           |
| `sort`           | `O(N * log N)`   |
| `forEach`/`map`/`filter`/`reduce`/etc. | `O(N)`|

