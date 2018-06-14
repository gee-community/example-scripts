# geometry.bounds
- creates a new rectangular geometry extending from the northerly to the southerly and the westerly to the easterly extent of a specified geometry.

## Syntax

#### Javascript
```
newGeometry = oldGeometry.bounds ( errorMargin, coordinateSystem )
```

- *newGeometry* is the new point geometry.
- *oldGeometry* is the specified geometry.
- *errorMargin* is an ErrorMargin object indicating the maximum allowable placement error in meters.
- *coordinateSystem* is a specified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default:  'EPSG4326' (WGS84) 


## Example

#### Javascript
```javascript
var AllStateCOLLECTION = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'Florida') );
var OneStateELEMENT    = OneStateCOLLECTION.first( );
var OneStateFEATURE    = ee.Feature( OneStateELEMENT );
var OneStateGEOMETRY   = OneStateFEATURE.geometry();
Map.centerObject( OneStateGEOMETRY, 6 );        Map.addLayer( OneStateGEOMETRY, {color:'331188'} );
var NewGEOMETRY  = OneStateGEOMETRY.bounds( );  Map.addLayer( NewGEOMETRY,      {color:'ffffff'} );
```
