Convert a string to spinal case. Spinal case is all-lowercase-words-joined-by-dashes.

```javascript
function spinalCase(str) {
  return str
  .split(/\s|_|(?=[A-Z])/)
  .join('-')
  .toLowerCase();
}

console.log(spinalCase('This Is Spinal Tap'));
console.log(spinalCase("thisIsSpinalTap"))
console.log(spinalCase("The_Andy_Griffith_Show"))
console.log(spinalCase("Teletubbies say Eh-oh"))
```

```
spinalCase("This Is Spinal Tap") should return the string this-is-spinal-tap.
spinalCase("thisIsSpinalTap") should return the string this-is-spinal-tap.
spinalCase("The_Andy_Griffith_Show") should return the string the-andy-griffith-show.
spinalCase("Teletubbies say Eh-oh") should return the string teletubbies-say-eh-oh.
spinalCase("AllThe-small Things") should return the string all-the-small-things.
```

