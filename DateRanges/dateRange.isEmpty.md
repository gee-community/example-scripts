# dateRange.isEmpty
- Creates a new Boolean set to true (only) if a specified dateRange contains no dates (because its ending date precedes 

## Syntax

#### Javascript
```
newBoolean = oldDateRange.isEmpty( )
```

- *newBoolean* is the new Boolean.
- *oldDateRange.isEmpty( )* is the specified dateRange.

## Example

#### Javascript
```javascript
var TheDATERANGE = ee.DateRange( '1990-07-16', '1950-12-25');
var TheBOOLEAN   = TheDATERANGE.isEmpty( );
print( TheDATERANGE );
print( 'Is it true that this dateRange is empty?', TheBOOLEAN );
```
