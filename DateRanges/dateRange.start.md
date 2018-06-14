# dateRange.start
- Creates a new date set to the (inclusive) start of a specified dateRange.

## Syntax

#### Javascript
```
newDate = oldDateRange.start( )
```

- *newDate* is The new Date.
- *oldDateRange.start( )* is the specified dateRange.

## Example

#### Javascript
```javascript
var MozartDATERANGE = ee.DateRange( '1756-1-27', '1791-12-5' );
var MozartBirthDATE = MozartDATERANGE.start( );
print( 'DateRange for Mozart', MozartDATERANGE );
print( 'So he was born on the following date.', MozartBirthDATE );
```
