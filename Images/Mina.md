# image.clamp
- Creates a new image on which each pixel is set t each value on a specified image unless that value is greater than a specified maximum or lower than a specified minimum, in which case the pixel is set to the closest of those specified maximum and minimum values.
- Masked pixels will appear as transparent in subsequent displays and eliminated from subsequent processing.

## Syntax

#### Javascript
```
newImage = oldImage.clamp( minimumValue, maximumValue )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *regionToBeKept* is the specified region, given as a Geometry or Feature. Use image.clipToCollection for clipping an image to a FeatureCollection.

Argument names used in documentation:
```
newImage = oldImage.clip( geometry )
```

## Example

#### Javascript
```javascript
var SatelliteIMAGE = ee.Image( 'LC8_L1T/LC80140332013216LGN00' );  // Delmarva Penninsula
var StateFEATURES  = ee.FeatureCollection( 'ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8' );
var ClipFEATURE    = StateFEATURES.filter( ee.Filter.eq('Name','Delaware') );
var ClippedIMAGE   = SatelliteIMAGE.clip( ClipFEATURE );
Map.centerObject( ClipFEATURE, 8);
Map.addLayer( SatelliteIMAGE, {bands: ['B5','B6','B2'], opacity:0.8}, 'Whole Scene'   );
Map.addLayer( ClipFEATURE,    {color: 'ff0000'},                      'Clipper'       );
Map.addLayer( ClippedIMAGE,   {bands: ['B4','B3','B2'], gain:0.015},  'Clipped Scene' );
```
