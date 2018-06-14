# ee.FeatureCollection
- creates a new feature collection from a specified geometry or list of geometries.

## Syntax

#### Javascript
```
newFeatureCollection = ee.FeatureCollection ( oldGeometry )
```
- *newFeatureCollection* is the new feature collection.
- *oldGeometry* is the specified geometry or list of geometries.

## Example

#### Javascript
```javascript
var ColoGEOMETRY = ee.Geometry.Polygon([[-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ] );
var WyomGEOMETRY = ee.Geometry.Polygon([[-111.05,41],[-111.05,45],[-104.10,45],[-104.10,41] ] );
var UtahGEOMETRY = ee.Geometry.Polygon([[-114.05,37],[-109.05,37],[-109.05,41],[-111.05,41],[-111.05,42],[-114.05,42] ] );
var TheFEATURES  = ee.FeatureCollection( [ColoGEOMETRY, WyomGEOMETRY, UtahGEOMETRY] );
Map.setCenter( -109.05, 41, 5 );
Map.addLayer( TheFEATURES );
```
