# ee.ImageCollection
- Creates a new image collection from an image collection asset identified by a specified asset ID.

## Syntax

#### Javascript
```
newImageCollection =  ee.ImageCollection ( assetID )
```

- *newImageCollection* is the new image collection.
- *assetID* the specified asset ID, given as a string.

## Example

#### Javascript
```javascript
var NewIMAGES = ee.ImageCollection( 'NOAA/DMSP-OLS/NIGHTTIME_LIGHTS' );
Map.setCenter( 126, 39, 6 );                                  // Korea
Map.addLayer( NewIMAGES, {min:0, max:100, opacity:0.7} );
```
