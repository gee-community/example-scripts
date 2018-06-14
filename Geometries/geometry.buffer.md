# geometry.buffer
- creates a new polygonal geometry whose boundaries are all at a specified distance from those of a specified geometry.

## Syntax

#### Javascript
```
newGeometry = oldGeometry.buffer ( distanceOutward, errorMargin, coordinateSystem )

```

- *newGeometry* is the new geometry.
- *oldGeometry* is the specified geometry.
- *distanceOutward* is the specified distance, given as a number in meters or, if specified, the units of coordinateSystem.  Positive distances are measured outward (and negative distances inward) from specified geometry boundaries.
- *errorMargin* is an ErrorMargin indicating the maximum allowable placement error in meters.  Default: distance * 0.1
- *coordinateSystem* is a specified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default:  'EPSG4326' (WGS84) 

## Example

#### Javascript
```javascript
var AllStateCOLLECTION = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'Colorado') );
var OneStateELEMENT    = OneStateCOLLECTION.first( );
var OneStateFEATURE    = ee.Feature( OneStateELEMENT );
var OneStateGEOMETRY   = OneStateFEATURE.geometry();
var NewGEOMETRY  = OneStateGEOMETRY.centroid().buffer( 50000 );  
Map.centerObject( OneStateGEOMETRY, 6 );                         
Map.addLayer( OneStateGEOMETRY, {color:'331188'} );
Map.addLayer( NewGEOMETRY,      {color:'ffffff'} );
```
