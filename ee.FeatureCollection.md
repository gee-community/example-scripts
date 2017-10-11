# ee.FeatureCollection
- Creates a new feature collection from a specified fusion table.

## Syntax

#### Javascript
```
newFeatureCollection = ee.FeatureCollection ( fusionTableID, geometryFieldName )
```

- *newFeatureCollection* is the new feature collection.
- *fusionTableID* is the asset ID specified fusion table, given as a string beginning with "ft:". 
- *geometryFieldName* is the name of a fusion table column to be used to define geometries. Default: 'geometry'. 

Arguments used in documentation:
```
newFeature = ee.Algorithms.Feature ( geometry, metadata )
newFeature = ee.Feature( geometry, properties )  
```

## Example

#### Javascript
```javascript
var polygonFEATURES = ee.FeatureCollection( 'ft:1xa2PvKTf7ynyAAEXEeHoltriaHFkyFJpvd74BLc6' );  // CT Census Tracts
var pointFEATURES   = ee.FeatureCollection( 'ft:1xa2PvKTf7ynyAAEXEeHoltriaHFkyFJpvd74BLc6', 'geometry_pos' );
Map.centerObject( polygonFEATURES, 11 );
Map.addLayer( polygonFEATURES, { color: '220099' }, 'The Geometry Column' );
Map.addLayer( pointFEATURES,   { color: 'ffff00' }, 'The Geometry_pos Column' );
Map.addLayer( pointFEATURES,   { color: 'ff00ff' }, 'The Geometry_pos Column' );  
```
