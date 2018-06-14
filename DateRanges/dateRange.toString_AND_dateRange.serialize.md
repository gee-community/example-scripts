# dateRange.toString_AND_dateRange.serialize	
- Each creates a new string presenting information on a specified dateRange.

## Syntax

#### Javascript
```
newString = oldDateRange.toString ( ) AND oldDateRange.serialize( )
```

- *newString* is the new string.
- *oldDateRange.toString ( )* is the specified dateRange.
- *oldDateRange.serialize( )* is the specified dateRange.

## Example

#### Javascript
```javascript
var TheDATERANGE   = ee.DateRange( '1990-07-16', '1950-12-25');
print( 'From print:',        TheDATERANGE );
print( 'From toString( ):',  TheDATERANGE.toString( )  );
print( 'From serialize( ):', TheDATERANGE.serialize( ) );
```
