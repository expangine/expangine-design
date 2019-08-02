# Number

## Static Parameters
- Base Prefixes
  - 0x = 16
  - 0X = 16
  - 0b = 2
  - 0B = 2
  - 0o = 8
  - 0O = 8
  - '' = 10
  
## Constants
- PI
- PI2
- HALF_PI
- E
- SQRT2
- SQRT1_2
- LN2
- LN10
- LOG2E
- LOG10E

## Type Parameters
- Base (default 10)
- Minimum
- Maximum
- Whole

## Operations
- `+` add (a, b: Number) => Number
- `-` subtract (a, b: Number) => Number
- `/` divide (a, b: Number) => Number
- `*` multiply (a, b: Number) => Number
- `%` modulus (a, b: Number) => Number
- `min` min (a, b: Number) => Number
- `max` max (a, b: Number) => Number
- `sqrt` square root (a) => Number
- `cbrt` cube root (a) => Number
- `^` power (a, b: Number) => Number
- `floor` floor (a) => Number
- `ceil` ceil (a) => Number
- `up` up (a) => Number
- `down` down (a) => Number
- `round` round (a) => Number
- `abs` abs (a) => Number
- `neg` negate (a) => Number
- `sign` sign (a) => Number
- `log` log (a, base: Number = E) => Number
- `sin` sine (a) => Number
- `cos` cosine (a) => Number
- `sinh` hyperbolic sine (a) => Number
- `cosh` hyperbolic cosine (a) => Number
- `hypot` hypotenuse of right angle triangle with two sides (a, b: Number) => Number
- `tan` tangent (a) => Number
- `asin` inverse sine (a) => Number
- `acos` inverse cosine (a) => Number
- `atan` inverse tangent (a) => Number
- `atan2` angle between two radians (y: Number, x: Number) => Number
- `rnd` random (a, b: Number) => Number
- `!` factorial (a, b: Number) => Number
- `choose` choose (a, b: Number) => Number
- `gcd` greatest common denominator (a, b: Number) => Number
- `&` bitwise and (a, b: Number) => Number
- `~` bitwise flip (a) => Number
- `^` bitwise xor (a, b: Number) => Number
- `|` bitwise or (a, b: Number) => Number
- format to base (a, base: Number, minDigits: Number) => Text
- format number (a, prefix: Text, suffix: Text, minPlaces: Number, maxPlaces: Number, roundUp: Boolean, allowExponent: Boolean, alwaysExponent: Boolean) => Text
- cast to boolean (a) => Boolean
- with unit (a, unit: UnitClass) => UnitValue

## Comparisons
- `=`
- `!=`
- `<`
- `<=`
- `>`
- `>=`
- `[]`
- `[}`
- `{}`
- `{]`
- `is whole`
- `has decimal`
- `is fractional`
- `positive`
- `negative`
- `divisible by`
- `one of`
- `not one of`

## Functions
- `rnd` (a: Number = 0, b: Number = 1) => Number



## TODO
- More random generation functions (noise?)
