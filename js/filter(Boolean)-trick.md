# The filter(Boolean) Trick

Here’s my favourite way to quickly remove all empty items from an array:

```
const array = [{ good }, null, { great }, undefined]

const truthyArray = array.filter(Boolean)
// truthyArray = [{ good }, { great }]
```

The `filter(Boolean)` step does the following:

Each item in the array is passed to the `Boolean` constructor
The Boolean constructor coerces each item to `true` or `false` depending on whether it’s `truthy` or `falsy`
If the item is `truthy`, we keep it

The main thing to know is that, in JavaScript, this:

```
array.filter(item => Boolean(item))
```

is exactly the same as this:

```
array.filter(Boolean)
```

(Original full source)[https://michaeluloth.com/javascript-filter-boolean/]
