# ee.Geometry.Point
- creates a new point geometry from specified longitude and latitude coordinates.

## Syntax

#### Javascript
```
newGeometry = ee.Geometry.Point ( longitudeCoordinate, latitudeCoordinate )  
```

- *newGeometry* is the new point geometry.
- *longitudeCoordinate* is the specified longitude, given as a number representing degrees
- *latitudeCoordinate* is specified latitude, given as a number representing degrees.

Arguments used in documentation:
```
newGeometry = ee.Geometry.Point ( lng, lat )  
```

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Point( 31.134204, 29.979241 );
Map.centerObject( TheGEOMETRY,17 );         
Map.addLayer( TheGEOMETRY );
```
