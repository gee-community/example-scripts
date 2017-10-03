# ee.Image
- Creates a new image from an image asset identified by a specified asset ID.

## Syntax

#### Javascript
```
newImage = ee.Image('assetID')
```

assetID is the specified asset ID, given as a string.

## Example

#### Javascript
```javascript
var NewIMAGE = ee.Image( 'CGIAR/SRTM90_V4' );
Map.setCenter( -98, 39, 4 );
Map.addLayer( NewIMAGE, {min:0, max: 2500} );
```
