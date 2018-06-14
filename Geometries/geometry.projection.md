# ee.Geometry.Point
- creates a new projection matching that of a specified geometry.

## Syntax

#### Javascript
```
newProjection = oldGeometry.projection ( )
```
- *newProjection* is the new projection.
- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05, 41], [-109.05, 37], [-102.05, 37], [-102.05, 41] ] );  // Colorado
var ThePROJECTION  = TheGEOMETRY.projection ( );
print( ThePROJECTION );
```
