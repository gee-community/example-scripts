# dateRange.union
- Creates a new dateRange encompassing the union of two specified dateRanges.

## Syntax

#### Javascript
```
newDateRange = 1stDateRange.union( 2ndDateRange )
```

- *newDateRange* is The new DateRange.
- *1stDateRange.union* is the first specified dateRange.
- *2ndDateRange* is the first specified dateRange.

## Example

#### Javascript
```javascript
var MozartDATERANGE     = ee.DateRange( '1756-1-27', '1791-12-5' );
var BeethovenDATERANGE  = ee.DateRange( '1770-12-17', '1827-3-26' );
var TheirTotalDATERANGE = MozartDATERANGE.union( BeethovenDATERANGE );
print( 'DateRange for Mozart', MozartDATERANGE );
print( 'DateRange for Beethoven', BeethovenDATERANGE );
print( 'DateRange when Either Was Alive', TheirTotalDATERANGE );
```
