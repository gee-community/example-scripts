# feature.set 
- creates new feature by replicating a specified feature after setting or resetting one or more specified properties to specified values.

## Syntax

#### Javascript
```
newFeature = oldFeature.set ( pairsOfPropertiesAndValues )
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature.
- *pairsOfPropertiesAndValues* are the specified properties and new values, given as a comma-separated sequence (or a dictionary) of property name strings, each immediately followed by its new value.




Arguments used in documentation:
```
newFeature = oldFeature.set(var_args) 
```

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ] );  // Colorado
var OldFEATURE  = ee.Feature( TheGEOMETRY, {label:'My New Feature', author:'Me'} );        
var NewFEATURE  = OldFEATURE.set( 'author','You', 'label','Your New Feature' );        
print( OldFEATURE.getInfo( ), NewFEATURE.getInfo( ) );
```
