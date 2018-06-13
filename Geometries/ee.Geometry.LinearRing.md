# ee.Geometry.LinearRing      
-  creates a new linearRing geometry from a specified sequence of longitude-latitude pairs of coordinates.

## Syntax

#### Javascript
```
newGeometry = ee.Geometry.LinearRing ( coordinatePairs )

```
- *newGeometry* is the new linearRing geometry.
- *coordinatePairs* is the specified set of coordinate pairs, given as a list of [lon,lat] lists or as a comma-separated sequence of (lon,lat,lon,lat…) numbers.


## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.LinearRing( 31.1330,29.9802,  31.1353,29.9802,  31.1353,29.9782,  31.1330,29.9782 );
Map.centerObject( TheGEOMETRY,17 );         
Map.addLayer( TheGEOMETRY );
```
