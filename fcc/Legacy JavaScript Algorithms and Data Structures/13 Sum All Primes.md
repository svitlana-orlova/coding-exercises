A prime number is a whole number greater than 1 with exactly two divisors:
1 and itself. For example, 2 is a prime number because it is only divisible
by 1 and 2. In contrast, 4 is not prime since it is divisible by 1, 2 and
4.

Rewrite sumPrimes so it returns the sum of all prime numbers that are less
than or equal to num.

```javascript
function sumPrimes(num) {
  const isPrime = function(n) {
    for (let i = 2; i <= Math.sqrt(n); i++)
      if (n % i === 0) return false;
    return n <= 1 ? false: true;
  };

  let sum = 0;
  for (let i = 2; i <= num; i++)
    if (isPrime(i))
      sum += i;

  return sum;
}

console.log(sumPrimes(10));
```

```
sumPrimes(10) should return a number.
sumPrimes(10) should return 17.
sumPrimes(977) should return 73156.
```

