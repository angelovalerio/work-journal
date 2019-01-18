###Learnings

#### Functional Programming
- When we pipe transformations than intermeditate arrays are created after each transformation but we compose transformations then a single output array is created with after applying all transformations
Piping of transformations
```
  arr
    .map(fn1)
    .filter(fn1)
    .reduce(fn1)
```

Composing Transformations
```
  compose(
    map(fn1),
    filter(fn2),
    reduce(fn3)
  )
```