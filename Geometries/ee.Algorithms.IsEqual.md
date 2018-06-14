# ee.Algorithms.IsEqual
- creates a new Boolean set to True (only) if the first of two specified geometries is identical to the second in both structure and content.

## Syntax

#### Javascript
```
newBoolean = ee.Algorithms.IsEqual ( 1stGeometry, 2ndGeometry )
```
- *newBoolean* is the new Boolean.
- *1stGeometry* is the first specified geometry.
- *2ndGeometry* is the second specified geometry. 
`
## Example

#### Javascript
```javascript
var FirstGEOMETRY  = ee.Geometry.Point( 31.134204, 29.979241 );
var SecondGEOMETRY = ee.Geometry.Point( 31.000000, 29.979241 );
var TrueOrFalse    = ee.Algorithms.IsEqual( FirstGEOMETRY, SecondGEOMETRY );
print( FirstGEOMETRY, SecondGEOMETRY );
print( 'Is it true or false that those two geometries are equal?' );
print( TrueOrFalse );

```
