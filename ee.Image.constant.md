# ee.Image.constant *or* ee.Image
- Create a new image in which all pixels are set to the same specified value.

## Syntax

#### Javascript
```
newImage = ee.Image(value)
newImage = ee.Image.constant(value)
```

- *newImage* is the new image.
- *value* is the specified value.


## Example

#### Javascript
```javascript
var FirstIMAGE  = ee.Image(1);   
var SecondIMAGE = ee.Image.constant(2);
print(FirstIMAGE.getInfo(), SecondIMAGE.getInfo());
```
