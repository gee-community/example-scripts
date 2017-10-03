# ee.Image.load
- Creates a new image from an image asset identified by a specified asset ID and (optional) version.

## Syntax

#### Javascript
```
newImage = ee.Image.load(assetID, version)
```

- *assetID* is the specified asset ID, given as a string.
- Optional: *version* is the version number. Default: -1 (calling from the current version)


## Example

#### Javascript
```javascript
var NewIMAGE = ee.Image.load( 'CGIAR/SRTM90_V4',-1 );
Map.setCenter( -98, 39, 4 );
Map.addLayer(NewIMAGE, {min:0, max: 2500} );
```
