# dateRange.intersects
- Creates a new Boolean set to true (only) if one specified dateRange overlaps at all with another specified dateRange.

## Syntax

#### Javascript
```
newBoolean = 1stDateRange.intersects( 2ndDateRange )
```

- *newBoolean* is the new Boolean.
- *1stDateRange.intersects* is the first specified dateRange.
- *2ndDateRange* is the second specified dateRange.

## Example

#### Javascript
```javascript
var MozartDATERANGE    = ee.DateRange( '1756-1-27', '1791-12-5' );
var BeethovenDATERANGE = ee.DateRange( '1770-12-17', '1827-3-26' );
var TheBOOLEAN         = MozartDATERANGE.intersects( BeethovenDATERANGE );
print( 'DateRange for Mozart', MozartDATERANGE );
print( 'DateRange for Beethoven', BeethovenDATERANGE );
print( 'Is it true that Mozart’s lifespan overlaps Beethoven’s?', TheBOOLEAN );
```
