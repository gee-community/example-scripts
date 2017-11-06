# feature.bounds 
- Creates a new rectangular feature extending from the northerly to the southerly and the westerly to the easterly extent of a specified feature.
## Syntax

#### Javascript
```
newFeature = oldFeature.bounds ( errorMargin, coordinateSystem )
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature. 

Arguments used in documentation:
```
newFeature = oldFeature.bounds (maxError, proj)
```

## Example

#### Javascript
```javascript
var AllStateCOLLECTION = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'Florida') );
var OneStateELEMENT    = OneStateCOLLECTION.first( );
var OneStateFEATURE    = ee.Feature( OneStateELEMENT ); 
var NewFEATURE         = OneStateFEATURE.bounds(  );  
Map.centerObject( OneStateFEATURE, 5 );        
Map.addLayer( OneStateFEATURE, {color:'331188'} );
Map.addLayer( NewFEATURE, {color:'ffffff', opacity:0.1} );
```
