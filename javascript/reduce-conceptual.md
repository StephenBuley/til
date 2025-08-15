# Reduce revisited

I've understood and used `reduce` for a long time, but I was watching a video yesteday and something clicked for me again. The second parameter in the function (initial value) is optional, and the function works slightly differently. With a second parameter, the callback function is called on the first element in the array. Without the second parameter, the callback function is called on the _second_ element in the array, but with the first value as the original initial value.

```javascript
const arr = [1, 2, 3, 4]
// this starts calling the callback function with the second element in the array
// and the "total" param set to the first element in the array
arr.reduce((total, curr) => total + curr) // starts with 1 + 2

// this starts calling the callback function with the first element in the array
// and the "total" param set to the initial value provided
arr.reduce((total, curr) => total + curr, 1) // starts with 1 + 1
```

Note that if the first option is used (without the initial value specified), there must be at least two elements in the array, or the function throws a `TypeError`.
