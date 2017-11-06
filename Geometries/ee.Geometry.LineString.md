# ee.Geometry.LineString
- creates a new lineString geometry from a specified sequence of longitude and latitude coordinates.

## Syntax

#### Javascript
```
newGeometry = ee.Geometry.LineString ( coordinatePairs )  
```

- *newGeometry* is the new lineString geometry.
- *coordinatePairs* is the specified set of coordinate pairs, given as a list of [lng, lat] lists or as a comma-separated sequence of (lng, lat, lng, lat...) numbers.

Arguments used in documentation:
```
newGeometry = ee.Geometry.LineString ( coordinatePairs )  
```

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.LineString( [ [31.1330, 29.9802], [31.1353, 29.9802],  [31.1353, 29.9782], [31.1330, 29.9782] ]] );
Map.centerObject( TheGEOMETRY, 17 );
Map.addLayer( TheGEOMETRY );
```
