# image.rgbtohsv
- Creates a new image by converting a specified image from RGB to HSV color format, one in which each of three bands (respectively representing hue, saturation, and value) is represented by a floating point value ranging from 0 to 1.    

## Syntax

#### Javascript
```
newImage = oldImage.rgbtohsv( )
```

- *newImage* is the new image.
- *oldImage* is the specified image.

## Example

#### Javascript
```javascript
var OldIMAGE = ee.Image( 'LC8_L1T/LC80150332014322LGN00' ).select([3,2,1]).unitScale(0,32767);
var NewIMAGE = OldIMAGE.rgbToHsv( );
print( OldIMAGE , NewIMAGE );
Map.setCenter( -75.8369, 39.4526, 12 );
Map.addLayer( OldIMAGE, { bands:'B4,B3,B2', min:0, max:0.5}, 'Original'  );
Map.addLayer( OldIMAGE.select(0), {min:0.1, max:0.8, palette:'ffffff,990000'},  'Redness'   );
Map.addLayer( OldIMAGE.select(1), {min:0.1, max:0.8, palette:'ffffff,009900'},  'Greenness' );
Map.addLayer( OldIMAGE.select(2), {min:0.1, max:0.8, palette:'ffffff,000099'},  'Blueness'  );
Map.addLayer( NewIMAGE.select('hue'),        {palette:'0000ff,ff0000,00ff00,ff0000,0000ff'}, 'Hue'         );
Map.addLayer( NewIMAGE.select('saturation'), {min:0.0,max:0.3,  palette:'000000,ff00ff'},    'Saturation'  );
Map.addLayer( NewIMAGE.select('value'),      {min:0.2,max:0.4,  palette:'000000,ffff00'},    'Brightness'  );
```
