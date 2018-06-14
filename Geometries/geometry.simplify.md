# geometry.simplify
- creates a new geometry by removing points from a specified geometry without exceeding a specified error margin.

## Syntax

#### Javascript
```
newGeometry = oldGeometry.simplify ( errorMargin, coordinateSystem )
```

- *newGeometry* is the new geometry.
- *oldGeometry* is the specified geometry.
- *errorMargin* is an ErrorMargin object indicating the maximum allowable placement error in meters.  This will maintained regardless of zoom level.
- *coordinateSystem* is A specified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default:  Same as OldGeometry.


## Example

#### Javascript
```javascript
var AllStateCOLLECTION = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'Idaho') );
var OneStateELEMENT    = OneStateCOLLECTION.first( );
var OneStateFEATURE    = ee.Feature( OneStateELEMENT );
var OneStateGEOMETRY   = OneStateFEATURE.geometry();
Map.centerObject( OneStateGEOMETRY, 6 );                Map.addLayer( OneStateGEOMETRY, {color:'331188'} );
var NewGEOMETRY  = OneStateGEOMETRY.simplify( 50000 );  Map.addLayer( NewGEOMETRY,      {color:'ffffff'} );

```
