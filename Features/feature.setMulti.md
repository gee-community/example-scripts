# feature.setMulti 
- creates new feature by replicating a specified feature after setting or resetting one or more specified properties to specified values.

## Syntax

#### Javascript
```
newFeature = oldFeature.setMulti ( dictionaryOfPropertiesAndValues )
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature.
- *dictionaryOfPropertiesAndValues* are the specified properties and new values, given as a dictionary of property name strings and new values.



Arguments used in documentation:
```
newFeature = oldFeature.setMulti(properties) 
```

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ] );  // Colorado
var OldFEATURE  = ee.Feature( TheGEOMETRY, {label:'My New Feature', author:'Me'} );        
var NewFEATURE  = OldFEATURE.setMulti( {'author':'You','label':'Your New Feature'} );        
print( OldFEATURE.getInfo( ), NewFEATURE.getInfo( ) );
```
