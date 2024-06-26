Create a function that sums two arguments together. If only one argument is
provided, then return a function that expects one argument and returns the
sum.

For example, addTogether(2, 3) should return 5, and
addTogether(2) should return a function.

Calling this returned function with a single argument will then return the
sum:

```javascript
var sumTwoAnd = addTogether(2);
sumTwoAnd(3) returns 5.
```

If either argument isn't a valid number, return undefined.


```javascript
function addTogether() {
  return false;
}

addTogether(2,3);
```

```
addTogether(2, 3) should return 5.
addTogether(23.4, 30) should return 53.4.
addTogether("2", 3) should return undefined.
addTogether(5, undefined) should return undefined.
addTogether("https://www.youtube.com/watch?v=dQw4w9WgXcQ") should return undefined.
addTogether(5) should return a function.
addTogether(5)(7) should return 12.
addTogether(2)([3]) should return undefined.
addTogether(2, "3") should return undefined.
```

