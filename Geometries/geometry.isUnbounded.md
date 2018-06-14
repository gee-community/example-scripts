# geometry.isUnbounded
-  creates a new Boolean set to True (only) a specified geometry is unbounded.

## Syntax

#### Javascript
```
newBoolean = oldGeometry.isUnbounded ( )
```

- *newNumber* is the new Boolean.
- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05, 41], [-109.05, 37], [-102.05, 37], [-102.05, 41] ] );  // Colorado
var TheBOOLEAN  = TheGEOMETRY.isUnbounded ( );
print( TheBOOLEAN );

```
