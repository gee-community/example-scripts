# dateRange.intersection
- Creates a new dateRange encompassing the intersection of two specified dateRanges.

## Syntax

#### Javascript
```
newDateRange = 1stDateRange.intersection( 2ndDateRange )
```

- *newDateRange* is The new DateRange.
- *1stDateRange.intersection* is the first specified dateRange
- *2ndDateRange* is the second specified dateRange.

## Example

#### Javascript
```javascript
var MozartDATERANGE      = ee.DateRange( '1756-1-27', '1791-12-5' );
var BeethovenDATERANGE   = ee.DateRange( '1770-12-17', '1827-3-26' );
var TheirSharedDATERANGE = MozartDATERANGE.intersection( BeethovenDATERANGE );
print( 'DateRange for Mozart', MozartDATERANGE );
print( 'DateRange for Beethoven', BeethovenDATERANGE );
print( 'DateRange when Both Were Alive', TheirSharedDATERANGE );
```
