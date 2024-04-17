Compare two arrays and return a new array with any items only found in one
of the two given arrays, but not both. In other words, return the symmetric
difference of the two arrays.

Note: You can return the array with its elements in any order.

```javascript
function diffArray(arr1, arr2) {
  const newArr = [];
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]) should return an array.
Waiting:["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] should return ["pink wool"].
Waiting:["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] should return an array with one item.
Waiting:["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] should return ["diorite", "pink wool"].
Waiting:["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] should return an array with two items.
Waiting:["andesite", "grass", "dirt", "dead shrub"], ["andesite", "grass", "dirt", "dead shrub"] should return [].
Waiting:["andesite", "grass", "dirt", "dead shrub"], ["andesite", "grass", "dirt", "dead shrub"] should return an empty array.
Waiting:[1, 2, 3, 5], [1, 2, 3, 4, 5] should return [4].
Waiting:[1, 2, 3, 5], [1, 2, 3, 4, 5] should return an array with one item.
Waiting:[1, "calf", 3, "piglet"], [1, "calf", 3, 4] should return ["piglet", 4].
Waiting:[1, "calf", 3, "piglet"], [1, "calf", 3, 4] should return an array with two items.
Waiting:[], ["snuffleupagus", "cookie monster", "elmo"] should return ["snuffleupagus", "cookie monster", "elmo"].
Waiting:[], ["snuffleupagus", "cookie monster", "elmo"] should return an array with three items.
Waiting:[1, "calf", 3, "piglet"], [7, "filly"] should return [1, "calf", 3, "piglet", 7, "filly"].
Waiting:[1, "calf", 3, "piglet"], [7, "filly"] should return an array with six items.
