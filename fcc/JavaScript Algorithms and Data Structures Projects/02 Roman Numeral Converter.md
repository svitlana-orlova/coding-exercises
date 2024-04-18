Convert the given number into a roman numeral.

```
Roman numerals	Arabic numerals
M	1000
CM	900
D	500
CD	400
C	100
XC	90
L	50
XL	40
X	10
IX	9
V	5
IV	4
I	1
```

All roman numerals answers should be provided in upper-case.

```javascript
function convertToRoman(num) {
  const romans = {
    1000: 'M',
    900: 'CM',
    500: 'D',
    400: 'CD',
    100: 'C',
    90: 'XC',
    50: 'L',
    40: 'XL',
    10: 'X',
    9: 'IX',
    5: 'V',
    4: 'IV',
    1: 'I'
  };

  const keysOrder = [1000, 900, 500, 400, 100,
                    90, 50, 40, 10, 9, 5, 4, 1];
  const result = [];

  for (const i of keysOrder) {
   // console.log(i)
    while (num >= i) {
      num -= i;
      result.push(romans[i]);
    }
  }

 return result.join('');
}

console.log(convertToRoman(16));
console.log(convertToRoman(36));
```

```
convertToRoman(2) should return the string II.
convertToRoman(3) should return the string III.
convertToRoman(4) should return the string IV.
convertToRoman(5) should return the string V.
convertToRoman(9) should return the string IX.
convertToRoman(12) should return the string XII.
convertToRoman(16) should return the string XVI.
convertToRoman(29) should return the string XXIX.
convertToRoman(44) should return the string XLIV.
convertToRoman(45) should return the string XLV.
convertToRoman(68) should return the string LXVIII
convertToRoman(83) should return the string LXXXIII
convertToRoman(97) should return the string XCVII
convertToRoman(99) should return the string XCIX
convertToRoman(400) should return the string CD
convertToRoman(500) should return the string D
convertToRoman(501) should return the string DI
convertToRoman(649) should return the string DCXLIX
convertToRoman(798) should return the string DCCXCVIII
convertToRoman(891) should return the string DCCCXCI
convertToRoman(1000) should return the string M
convertToRoman(1004) should return the string MIV
convertToRoman(1006) should return the string MVI
convertToRoman(1023) should return the string MXXIII
convertToRoman(2014) should return the string MMXIV
convertToRoman(3999) should return the string MMMCMXCIX
```

