# feature.convexHull 
- Creates a new feature encompassing a specified feature by connecting its outermost vertices.
## Syntax

#### Javascript
```
newFeature = oldFeature.convexHull ( errorMargin, coordinateSystem )
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature. 

Arguments used in documentation:
```
newFeature = oldFeature.convexHull (maxError, proj)
```

## Example

#### Javascript
```javascript
var AllStateCOLLECTION = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'New York') );
var OneStateELEMENT    = OneStateCOLLECTION.first( );
var OneStateFEATURE    = ee.Feature( OneStateELEMENT ); 
var NewFEATURE  = OneStateFEATURE.convexHull(  );  
Map.centerObject( OneStateFEATURE, 5 );            
Map.addLayer( OneStateFEATURE, {color:'331188'} );
Map.addLayer( NewFEATURE, {color:'ffffff', opacity:0.1} );  
```
