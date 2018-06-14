# dateRange.end
- Creates a new date set to the (exclusive) end of a specified dateRange.

## Syntax

#### Javascript
```
newDate = oldDateRange.end( )
```

- *newDate* is the new Date.
- *oldDateRange.end( )* is the specified dateRange.
## Example

#### Javascript
```javascript
var MozartDATERANGE = ee.DateRange( '1756-1-27', '1791-12-5' );
var MozartDeathDATE = MozartDATERANGE.end( );
print( 'DateRange for Mozart', MozartDATERANGE );
print( 'So he died on the following date.', MozartDeathDATE );
```
