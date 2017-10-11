# image.slice
- Creates a new image containing only those bands of a specified image that are stored at or after a specified starting position and before (but not including) a specified stopping position among all such bands.

## Syntax

#### Javascript
```
newImage = oldImage.slice( startingPosition, stoppingPosition )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *startingPosition* is the specified starting position, given as an integer with negative integers counted backwards from the end.
- Optional: *stoppingPosition* is the specified stopping position, given as an integer with negative integers counted backwards from the end.  Default: the final band.

Argument names used in Docs:
```
newImage = oldImage.slice( start, end )
```

## Example

#### Javascript
```javascript
var RedBandIMAGE   = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B4'] );     // Los Angeles
var GreenBandIMAGE = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B3'] );
var BlueBandIMAGE  = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B2'] );
var MultibandIMAGE = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).slice( 1,4 );
print( MultibandIMAGE );
Map.setCenter( -118.2733, 34.0942, 12 ); 
Map.addLayer( RedBandIMAGE,   {min:0, max:0.17, palette:'000000,ff5555'},     'RednessImage'   );
Map.addLayer( GreenBandIMAGE, {min:0, max:0.17, palette:'000000,77ff77'},     'Greenness Image');
Map.addLayer( BlueBandIMAGE,  {min:0, max:0.17, palette:'000000,7777ff'},     'Blueness Image' );
Map.addLayer( MultibandIMAGE, {min:0, max:0.17, gamma:0.5, bands:'B4,B3,B2'}, 'Multiband Image');
```
