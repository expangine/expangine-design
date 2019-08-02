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
  - select: takes a raw value and returns the best fitting sub-type
 - **Function**: takes arguments of certain types and produces a result
 - **Iterable**: takes arguments of certain types and generates results upon request
 - **Condition**: something that evaluates to boolean. Can be multiple conditions or any function which returns boolean
 - **Query**: an iterable that takes an array and condition and returns a subset of that array
 - **Transformation**: a function which takes on data type and converts it to another
 
 ## Thoughts
- A condition is a type? A query is a type?
- Creating a Query
  1. Select/build the type used as query parameters.
  2. Select an instance or type of an array.
  3. Select a chain of transformations/operations that produce a result (filter, group, aggregate, etc).
    - The type used for references is { params, list, item, index}
  4. The query is now a "function" which takes a list and parameters and produces a result.
    - It can be used as a subquery now
- Functions have categories to be organized in UI. 
