# ee.Feature *or* ee.Algorithms.Feature
- creates a new feature by replicating a specified feature but only with a specified set of properties.

## Syntax

#### Javascript
```
newFeature = oldFeature.select (propertyList, propertyNameList, retainGeometry?) 
```

- *newFeature* is the new feature.
- *oldFeature* is the specified feature.
- *propertyList* is the specified properties, given as a list of property names
- *propertyNameList* are the new names for the selected properties, given as a list corresponding to propertyList
- *retainGeometry?* is a Boolean set to rue (only) if the primary geometry key is be regarded as selected even when unselected.  Default: true

Arguments used in documentation:
```
newFeature = oldFeature.select(propertySelectors, newProperties, retainGeometry) 
```

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ] );  // Colorado
var OldFEATURE  = ee.Feature( TheGEOMETRY, {label:'My New Feature', author:'Me'} );        
var NewFEATURE  = OldFEATURE.select( ['author'], ['WHO'] );        
print( OldFEATURE, NewFEATURE );
```
