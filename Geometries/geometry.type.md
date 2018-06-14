# geometry.type
- creates a new string indicating the GeoJSON type of a specified geometry.

## Syntax

#### Javascript
```
newString = oldGeometry.type ( )
```

- *newString* is the new string.
- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript

var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05, 41], [-109.05, 37], [-102.05, 37], [-102.05, 41] ] );  // Colorado
var TheSTRING   = TheGEOMETRY.type( );
print( TheSTRING );
```
