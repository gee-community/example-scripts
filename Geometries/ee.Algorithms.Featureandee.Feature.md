# ee. Algorithms.Feature 	  and    ee.Feature     
- both create a new feature from a specified geometry and (optional) set of metadata properties.

## Syntax

#### Javascript
```
newFeature = ee.AlgorithmsFeature ( oldGeometry, properties )
             or  .ee.Feature(oldGeometry, properties )  
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature. 
- *properties* is a dictionary of properties to be ascribed to the new feature.  Default: { }

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ] );  // Colorado
var ThatFEATURE  = ee.Algorithms.Feature( TheGEOMETRY, {label:'My New Feature', author:'Me'} );        
var ThisFEATURE  = ee.Feature(            TheGEOMETRY, {label:'My New Feature', author:'Me'} );        
print( ThisFEATURE.getInfo( ) );
print( ThatFEATURE.getInfo( ) );
```
