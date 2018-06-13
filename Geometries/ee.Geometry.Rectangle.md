# ee.Geometry.Rectangle 
- creates a new rectangle geometry from a specified set of minimum and maximum longitude and latitude coordinates.

## Syntax

#### Javascript
```
newGeometry = ee.Geometry.Rectangle ( minimumLon, minimumLat, maximumLon, maximumLat )
```
- *newGeometry* is the new rectangle geometry.
- *minimumLon, minimumLat, maximumLon,  maximumLat * is the specified set of westerly, southerly, easterly, and northerly coordinates, each given as a number.

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Rectangle(  31.1330, 29.9782, 31.1353, 29.9802  ); 
Map.centerObject( TheGEOMETRY,17 );         
Map.addLayer( TheGEOMETRY );
```
