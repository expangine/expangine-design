# expangine-design

## Organization
- **Definitions**: The programmatic interface of types, functions, actions, etc are defined based on types.
- **Runtime**: The definitions are given implementation code, either producing the raw output with javascript data types - or it produces a query string.
- **Designer**: A user interface which allows you to define complex types.
- **Visuals**: A library which supplies one or more components for each type, condition, etc.
- **Builder**: A user interface which uses the types, designed types, and visuals to create instances of the types.

## Terms
- **Type**: a data type
  - name: an encoded name & human friendly name
  - operation: a function which takes a value and optionally other parameters and produces a result
  - comparison: a function which evaluates a value to some input and produces a boolean result
  - validation: takes a raw value and determines if it fits the data type
  - normalize: takes a raw value and returns the normalized representation to be used in functions
  - fit: takes a raw value and returns the best fitting sub-type
  - sub types: an array has length and item, an object has any number
  - superset: if another type is a superset of this type. if it is, it can be used interchangeably with this type
 - **Function**: takes arguments of certain types and produces a result
 - **Iterable**: takes arguments of certain types and generates results upon request
 - **Condition**: something that evaluates to boolean. Can be multiple conditions or any function which returns boolean
 - **Query**: an iterable that takes an array and condition and returns a subset of that array
 - **Transformation**: a function which takes a data type and converts it to another
 
 ## Thoughts
- A condition is a type? A query is a type? A function a type?
- Creating a Query
  1. Select/build the type used as query parameters.
  2. Select an instance or type of an array.
  3. Select a chain of transformations/operations that produce a result (filter, group, aggregate, etc).
    - The type used for references is { params, list, item, index}
  4. The query is now a "function" which takes a list and parameters and produces a result.
    - It can be used as a subquery now
- Functions have categories to be organized in UI. 
- Once you select a function, each input lists by category all other things which return a value in the expected type.
- A function definition has a unique name, arguments { name, type, default } and return type. Some functions are "for a type" and some are for operating on multiple types.
- A function runtime implements the function given the parameters.
- A function visual describes the function and arguments with human friendly text.
- The runtime has a global scope. On a webpage it would the the URL, the current user, etc. Plugins can add to the scope.
- A function can be transformed into another function. The new function takes 0 or more parameters of the existing function as it's parameters while the other parameters get values to use. This is so something like a condition with two values can be changed to a condition with one value and a constant/reference.
- A Dynamic is a type which takes a context and returns a value. 
- You can extend types. There should be an Integer type which extends Number and adds bitwise operations.
- Serialization goes to an array, where the first element maps to a parser and the remaining elements are the payload. Examples:
  - `['number']` number type with no arguments
  - `['number', { min: 0, max: 1 }]` number type with min/max arguments
  - `['function', 'min', ['number'], [['a', ['number']], ['b', ['number'], 0]]]` min function
  - `['list', ['number'], { min: 3 }]` list of numbers with atleast 3 items
  - `['object', {a: 'number', b: ['list', 'text']}]` object with sub list
  - a good rule of thumb, if the parameter is required make it part of the array, at the end place the optional payload items in object
  - perhaps when ready/writing if an array is a single value reduce it, when parsing and a parseable object is detected that's not an array wrap it in one.
- In the UI you can start with any value in scope - as you place values in arguments it tells you what the expected type is and if there are any available operations to get there it suggests them. You could customize this further and add these suggestions to the back-end. 
- There should be a way to specify a reference to a list and it produces a list of the sub items.
  - These examples assume this structure: `{ b: [text], c: [{d: text, e: number}] }`
  - `b` returns list of text
  - `c` returns list of objects
  - `c.length` returns length of c
  - `c.item` synonomous to `c`
  - `c.item.d` returns list of d with type List<Text>
