# ee.Algorithms.Describe _AND_ dateRange.getInfo
- Each creates a JSON-compatible text object representing a specified dateRange.

## Syntax

#### Javascript
```
newObject = ee.Algorithms.Describe( oldDateRange ) AND oldDateRange.getInfo( )
```

- *newObject* is the new object.
- *ee.Algorithms.Describe( oldDateRange )* is the specified starting date, given as a Date object, a number (interpreted as milliseconds since the beginning of January 1, 
1970),  or a string (in YYYY-MM-DD, YYYY-DDD, or YYYY-MM-DD-TTTTTT format such as '1996-01-01' or '1996-001' or '1996-01-01T08:00').
- *oldDateRange.getInfo( )* is the specified dateRange.
## Example

#### Javascript
```javascript
var TheDATERANGE   = ee.DateRange( '1990-07-16', '1950-12-25');
print( 'From print:',                     TheDATERANGE );
print( 'From ee.Algorithms.Describe( ):', ee.Algorithms.Describe( TheDATERANGE ) );
print( 'From getInfo( ):',                TheDATERANGE.getInfo( ) );
```
