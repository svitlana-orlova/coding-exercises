Find the smallest common multiple of the provided parameters that can be
evenly divided by both, as well as by all sequential numbers in the range
between these parameters.

The range will be an array of two numbers that will not necessarily be in
numerical order.

For example, if given 1 and 3, find the smallest common multiple of both 1
and 3 that is also evenly divisible by all numbers between 1 and 3. The
answer here would be 6.

```javascript
function smallestCommons(arr) {
  return arr;
}

smallestCommons([1,5]);
```

```javascript
function smallestCommons(arr) {
  const [min, max] = arr.sort((a, b) => a - b);
  const gcd = (a, b) =>
   (b === 0) ? a : gcd(b, a % b);
  const lcm = (a, b) => a * b / gcd(a, b);
  const nums = Array(max - min + 1)
    .fill(0)
    .map((x, i) => i + min);

  return nums.reduce((a, x) => lcm(a, x));
}

console.log(smallestCommons([1,5]));
console.log(smallestCommons([5, 1]));
```

```
smallestCommons([1, 5]) should return a number.
smallestCommons([1, 5]) should return 60.
smallestCommons([5, 1]) should return 60.
smallestCommons([2, 10]) should return 2520.
smallestCommons([1, 13]) should return 360360.
smallestCommons([23, 18]) should return 6056820.
```

