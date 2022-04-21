## De-structure

When we de-structure using ES6, watch out that the object being de-structured cannot be `null` or `undefined`, so it's wise to give it a default value.

```js
const { a, b, c, d, e } = obj || {};
```

## Merging array and object

```js
const a = [1, 2, 3];
const b = [1, 5, 6];
// Using `Set` to remove duplicate items
const c = [...new Set([...a, ...b])]; // [1,2,3,5,6]

const obj1 = { a: 1 };
const obj2 = { b: 1 };
const obj = { ...obj1, ...obj2 }; // { a:1, b:1 }
```

## Condition checks

Instead of

```js
if (
    type == 1 ||
    type == 2 ||
    type == 3 ||
    type == 4 ||
){
   //...
}
```

Use `includes` method on array.

```js
const conditions = [1, 2, 3, 4];

if (conditions.includes(type)) {
  //...
}
```

## Flatten array

```js
const deps = {
  采购部: [1, 2, 3],
  人事部: [5, 8, 12],
  行政部: [5, 14, 79],
  运输部: [3, 64, 105],
};

// Use .flat(Infinity) to flatten nested array 
// Result => [1, 2, 3, 5, 8, 12, 5, 14, 79, 3, 64, 105];
const member = Object.values(deps).flat(Infinity);
```

## Dynamic object key

```js
const obj = {};
const index = 1;

obj[`topic${index}`] = "topic content";
```

