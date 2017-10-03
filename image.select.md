# image.select
- Creates a new image containing only those bands of a specified image that have a specified name, index, or RE2-compatible regex.
- Since selections cannot be made from an image collection, such a collection would have to be reduced to an image in order to select bands.

## Syntax

#### Javascript
```
newImage = oldImage.select( bandSelectors, bandOrder )  
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *bandSelectors* are the specified names, indices, or regexes, given as an array of strings.
- Optional: *bandOrder* is an array of new names to be ascribed to (all of) the bands of the new image, given as an array of strings.


## Example

#### Javascript
```javascript
var RedBandIMAGE   = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B4'] );   // Los Angeles
var GreenBandIMAGE = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B3'] );
var BlueBandIMAGE  = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B2'] );
var MultibandIMAGE = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B4','B3','B2'] );
Map.setCenter( -118.2733, 34.0942, 12 ); 
Map.addLayer( RedBandIMAGE,   {min:0, max:0.17, palette:'000000,ff5555'},     'RednessImage'   );
Map.addLayer( GreenBandIMAGE, {min:0, max:0.17, palette:'000000,77ff77'},     'Greenness Image');
Map.addLayer( BlueBandIMAGE,  {min:0, max:0.17, palette:'000000,7777ff'},     'Blueness Image' );
Map.addLayer( MultibandIMAGE, {min:0, max:0.17, gamma:0.5, bands:'B4,B3,B2'}, 'Multiband Image');
```
