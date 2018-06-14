# dateRange.contains
- Creates a new Boolean set to true (only) if a specified dateRange contains another specified date or dateRange.

## Syntax

#### Javascript
```
newBoolean = oldDateRange.contains( anotherDateOrDateRange )
```

- *newBoolean* is the new Boolean
- *oldDateRange.contains* is the specified “container” dateRange
- *anotherDateOrDateRange* is the specified “containee” date or dateRange

## Example

#### Javascript
```javascript
var MozartDATERANGE    = ee.DateRange( '1756-1-27', '1791-12-5' );
var BeethovenDATERANGE = ee.DateRange( '1770-12-17', '1827-3-26' );
var TheBOOLEAN         = MozartDATERANGE.contains( BeethovenDATERANGE );
print( 'DateRange for Mozart', MozartDATERANGE );
print( 'DateRange for Beethoven', BeethovenDATERANGE );
print( 'Is it true that Mozart’s lifespan contain Beethoven’s?', TheBOOLEAN );
```
