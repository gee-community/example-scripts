# feature.simplify 
- Creates a new feature by removing points from the geometry of a specified feature without exceeding a specified error margin.
## Syntax

#### Javascript
```
newFeature = oldFeature.simplify ( errorMargin, coordinateSystem )
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature. 

Arguments used in documentation:
```
newFeature = oldFeature.simplify (maxError, proj)
```

## Example

#### Javascript
```javascript
var AllStateCOLLECTION = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'Idaho') );
var OneStateELEMENT    = OneStateCOLLECTION.first( );
var OneStateFEATURE    = ee.Feature( OneStateELEMENT ); 
Map.centerObject( OneStateFEATURE, 5 );               Map.addLayer( OneStateFEATURE, {color:'331188'} );
var NewFEATURE  = OneStateFEATURE.simplify( 50000 );  Map.addLayer( NewFEATURE, {color:'ffffff', opacity:0.1} );
```
