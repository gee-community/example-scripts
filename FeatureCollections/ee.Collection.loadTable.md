# ee.Collection.loadTable
- Creates a new feature collection from a specified fusion table.

## Syntax

#### Javascript
```
newFeatureCollection = ee.Collection.loadTable ( fusionTableID, geometryFieldName, version )

```

- *newFeatureCollection* is the new feature collection.
- *fusionTableID* is the asset ID of the specified fusion table, given as a string beginning with "ft:". 
- *geometryFieldName* is the name of the fusion table column to be used to define feature geometries. Default: 'geometry'.
- *version* is the fusion table version number, given as a number. Default: -1 (the current version).


## Example

#### Javascript
```javascript
var polygonFEATURES = ee.Collection.loadTable( 'ft:1xa2PvKTf7ynyAAEXEeHoltriaHFkyFJpvd74BLc6' );  // CT Census Tracts
var pointFEATURES   = ee.Collection.loadTable( 'ft:1xa2PvKTf7ynyAAEXEeHoltriaHFkyFJpvd74BLc6', 'geometry_pos' );
Map.centerObject( polygonFEATURES, 11 );
Map.addLayer( polygonFEATURES, { color: '113355' }, 'The Geometry Column' );
Map.addLayer( pointFEATURES,   { color: 'ff00ff' }, 'The Geometry_pos Column' );  
```
