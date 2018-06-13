# ee.DateRange
- Creates a DateRange object extending from a specified starting date to a specified stopping date and including both of those dates.

## Syntax

#### Javascript
```
newDateRange = ee.DateRange( startingDate, stoppingDate, timeZone )
```

- *newDateRange* is The new DateRange.

## Example

#### Javascript
```javascript
var TheDATERANGE = ee.DateRange( '1950-12-25', '1990-07-16' );
print( TheDATERANGE );
```
