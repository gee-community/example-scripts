# feature.centroid 
- Creates a new point feature at the centroid of a specified feature.

## Syntax

#### Javascript
```
newFeature = oldFeature.centroid ( errorMargin, coordinateSystem )
```

- *newFeature* is the new feature.
- *oldFeature* is the specified feature
- *coordinateSystem* is the specified coordinate system, given as an EPSG code or as a WKT string. Default: WGS84 
-*errorMargin* is an object indicating the maximum allowable reprojection error in meters
- Optional: *properties* is a dictionary of properties to be ascribed to the new feature.  Default: { }

Arguments used in documentation:
```
newFeature = oldFeature.centroid (maxError, proj)
```

## Example

#### Javascript
```javascript
var AllStateCOLLECTION = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'Iowa') );
var OneStateELEMENT    = OneStateCOLLECTION.first( );
var OneStateFEATURE    = ee.Feature( OneStateELEMENT ); 
var NewFEATURE         = OneStateFEATURE.centroid( );  
Map.centerObject( OneStateFEATURE, 6 );         
Map.addLayer( OneStateFEATURE, {color:'331188'} );
Map.addLayer( NewFEATURE, {color:'ff0000'} );
```
