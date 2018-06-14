# geometry.edgesAreGeodesics
-   creates a new Boolean set to True (only) if the lines in a specified geometry are spheroidal rather than planar.

## Syntax

#### Javascript
```
newBoolean = oldGeometry.edgesAreGeodesics ( )
```
- *newBoolean* is the new Boolean.
- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript
var OldGEOMETRY = ee.Geometry.Polygon( [ [-109.05, 41], [-109.05, 37], [-102.05, 37], [-102.05, 41] ] );  // Colorado
var OldBOOLEAN  = OldGEOMETRY.edgesAreGeodesics ( );
var NewGEOMETRY = OldGEOMETRY.transform( 'EPSG:2772', 100 );  
var NewBOOLEAN  = NewGEOMETRY.edgesAreGeodesics ( );
Map.centerObject( OldGEOMETRY );
Map.addLayer( OldGEOMETRY );
Map.addLayer( NewGEOMETRY );
print( OldGEOMETRY, OldBOOLEAN );
print( NewGEOMETRY, NewBOOLEAN );

```
