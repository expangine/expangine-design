# List<T>

## Static Parameters
*none*
  
## Constants
*none*

## Type Parameters
- Minimum
- Maximum
- Allow Null
- T

## Sub Types
- `length`: Number
- `item`: T

## Operations
- `+` add (a, b: T) => List<T>
- `-` subtract (a, b: T) => List<T>
- `addFirst` (a, b: T) => List<T>
- `addLast` (a, b: T) => List<T>
- `where` filter (a, b: (T) => Boolean) => List<T>
- `not` filter not (a, b: (T) => Boolean) => List<T>
- `transform` transform (a, b: (T) => R) => List<R>
- `reverse` reverse item order (a) => List<T>
- `exclude` the items from this list and not in the given list (a, b: List<T>, c: (T, T) => Boolean) => List<T>
- `intersect` the items they have in common (a, b: List<T>, c: (T, T) => Boolean) => List<T>
- `sort` sort values by comparator (a, sorter: (T, T) => Number) => List<T>
- `shuffle` move values around (a, times: Number) => List<T>
- `unique` return only unique values (a, b: (T, T) => Boolean) => List<T>
- `duplicates` return only the duplicates (a, b: (T, T) => Boolean, onlyOnce: Boolean> => List<T>
- `take` take first # items (a, count: Number) => List<T>
- `skip` skip first # items (a, count: Number) => List<T>
- `drop` ignore last # items (a, count: Number) => List<T>
- `append` add list to end (a, b: List<T>) => List<T>
- `prepend` add list to beginning (a, b: List<T>) => List<T>
- `split` split list into two based on condition (a, splitter: (T) => Boolean) => { pass: List<T>, fail: List<T> }
- `delete` removes all values in list (a) => List<T>
- `extract` removes all values from underlying list and returns new (a) => List<T>
- `indexOf` index of (a, b: (T) => Boolean) => Number       
- `lastIndexOf` last index of (a, b: (T) => Boolean) => Number
- `first` return first item (a) => T
- `last` return last item (a) => T
- `count` (a) => Number
- `objectify` convert to object<K, R> (a, b: (T) => K, c: (T) => R) => { [K]: R }
- `group` convert to object<K: Text> (a, b: (T) => K): { [K]: { list: List<T>, key: K } }
- `reduceSimple` reduce using simple operation (a, b: (T, T) => T) => T
- `reduce` reduce more complex<R> (a, b: (T, R) => R, initial: R) => R
- `randomList` choose # number items (a, b: Number) => List<T>
- `random` choose random item (a) => T

## Comparisons
- `=`
- `!=`
- `empty` is list empty (a) => Boolean
- `has` is list not empty (a) => Boolean
- `contains` list has item (a, b: T) => Boolean
