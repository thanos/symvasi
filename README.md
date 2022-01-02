# symvasi
A simple but effective contract language

## The Types

All types in the `SymVasi` langaued are influced by the the various contexts that are used when the contract run. So unlike most programming language documenation we can not strt describing this langaues by it's "basic" types, but by its most fundemental execution element, the `contract`.

```
contract {

  preamble {
    
  
  }
  
  

}

```


### Booleans
There are two Boolean values, and a literal for each one.
```
true  // Not false.
false // Not *not* false.
```

### Numbers

#### Integers
In `SymVasi`, `integers` are zero, positive or negative whole numbers without a fractional part and having ranging precision upto 128bits, e.g. 0, 100, -10. Integers can be expressed as binary, octal, and hexadecimal values.
```
isv>  0b11011000 # binary
216
isv> 0o12 # octal
10
isv> 0x12 # hexadecimal

```


#### Decimal
To avoid precision ambiguity `SymVasi` doesn not offer float but instead `Decimal` which offers fast fast correctly-rounded decimal fixed point arithmetic. Some values cannot be exactly represented in a float data type. For instance, storing the 0.1 value in "classic" float (which is a binary floating point value) variable we get only an approximation of the value. We want to avoid such problems as we see in rust and other languages, such as when `0.1 + 0.2` is not equal to `0.3`. Similarly, the 1/3 value cannot be represented exactly in decimal floating point type. To mitigate these problems all decimal operations are carried out under the constraints and strategies set by the contracts decimal context. The decimal context of a contract is immutable and always required to be set.


```
$
precision: 9
exponent_max: 999
exponent_min:
rounding: ROUND_DOWN
$
```




#### Rational

#### Complex

### Date & Time
#### DateTime
#### Timezone

### Address

### Contract

### Transaction



