# ee.DateRange.unbounded
- Creates a dateRange that encompasses all possible dates.

## Syntax

#### Javascript
```
newDateRange = ee.DateRange.unbounded( )
```

- *newDateRange* is The new DateRange.

## Example

#### Javascript
```javascript
var TheDATERANGE = ee.DateRange( '1950-12-25', '1990-07-16' );
var TheBOOLEAN   = TheDATERANGE.isUnbounded( );
print( TheDATERANGE, "Is this dataRange unbounded?", TheBOOLEAN );
```
