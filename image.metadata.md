# image.metadata
- Creates a new image in which each pixel is set to the (type double) value of a specified numerical property of a specified image.

## Syntax

#### Javascript
```
newImage = oldImage.metadata( property, newBandName )
```

- *newImage* is the new image.
- *oldImage1* is the first specified image.
- *property* The specified numerical property, given as a string indicating to its name
- Optional: *newBandName* A name for the output band, given as a string. Default: the name of the specified property


## Example

#### Javascript
```javascript
var OldIMAGE = ee.Image( 'LC8_L1T/LC80150332014322LGN00' );  // Chesapeake Image
var NewIMAGE = OldIMAGE.metadata('CLOUD_COVER', 'Cloudiness');
print( OldIMAGE, NewIMAGE );  
Map.centerObject( OldIMAGE, 8 );
Map.addLayer( OldIMAGE, { bands:['B4','B3','B2'], gain:0.025}, 'Cloudy Scene'     );
Map.addLayer( NewIMAGE, {palette:'ff0000', opacity:0.5},       'Cloudiness Value' );
```
