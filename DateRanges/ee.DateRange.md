# ee.DateRange
- creates a DateRange object extending from a specified starting date to a specified stopping date and including both of those dates.

## Syntax

#### Javascript
```
newDateRange = ee.DateRange( startingDate, stoppingDate, timeZone )
```

- *newDateRange* is The new DateRange.
- *startingDate* is the specified starting date, given as a Date object, a number (interpreted as milliseconds since the beginning of January 1, 
1970),  or a string (in YYYY-MM-DD, YYYY-DDD, or YYYY-MM-DD-TTTTTT format such as '1996-01-01' or '1996-001' or '1996-01-01T08:00').
- *timeZone* is a time zone to be assumed when either startingDate or stoppingDate is specified as a string.  Default: UTC
- *stoppingDate* is A specified stopping date, given as a Date object, a number (interpreted as milliseconds since the beginning of January 1, 1970), 
or a string (in YYYY-MM-DD, YYYY-DDD, or YYYY-MM-DD-TTTTTT format such as '1996-01-01' or '1996-001' or '1996-01-01T08:00'). Default: one millisecond after startingDate 


## Example

#### Javascript
```javascript
var TheDATERANGE = ee.DateRange( '1950-12-25', '1990-07-16' );
print( TheDATERANGE );
```
