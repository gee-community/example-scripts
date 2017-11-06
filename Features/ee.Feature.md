# ee.Feature *or* ee.Algorithms.Feature
- Both create a new feature from a specified geometry and (optional) set of metadata properties.

## Syntax

#### Javascript
```
newFeature = ee.Algorithms.Feature ( oldGeometry, properties )
newFeature = ee.Feature( oldGeometry, properties )  
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature. 
- Optional: *properties* is a dictionary of properties to be ascribed to the new feature.  Default: { }

Arguments used in documentation:
```
newFeature = ee.Algorithms.Feature ( geometry, metadata )
newFeature = ee.Feature( geometry, properties )  
```

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ] );  // Colorado
var ThisFEATURE  = ee.Feature(            TheGEOMETRY, {label:'My New Feature', author:'Me'} );  
var ThatFEATURE  = ee.Algorithms.Feature( TheGEOMETRY, {label:'My New Feature', author:'Me'} );              
Map.centerObject( TheGEOMETRY );
Map.addLayer( ThisFEATURE );
Map.addLayer( ThatFEATURE );
print( ThisFEATURE.getInfo( ) );
print( ThatFEATURE.getInfo( ) ); 
```
