# ee.Image
- Creates a new image from an image asset identified by a specified asset ID.

## Syntax

#### Javascript
```
newImage = ee.Image('assetID')
```

- *assetID* is the specified asset ID, given as a string.

According to the Docs in the Code Editor:
```
This constructor accepts a variety of arguments:
- A string: an EarthEngine asset id,
- A string and a number - an EarthEngine asset id and version,
- A number or EEArray: creates a constant image,
- A list: creates an image out of each list element and combines them into a single image,
- An ee.Image: returns the argument,
- Nothing: results in an empty transparent image.
```

## Example

#### Javascript
```javascript
var NewIMAGE = ee.Image( 'CGIAR/SRTM90_V4' );
Map.setCenter( -98, 39, 4 );
Map.addLayer( NewIMAGE, {min:0, max: 2500} );
```
#### python
````python
NewIMAGE = ee.Image( 'CGIAR/SRTM90_V4' )
print(NewIMAGE.getThumbUrl({'min':0, 'max':2500}))
````
