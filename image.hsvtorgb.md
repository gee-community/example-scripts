# image.hsvtorgb
- Creates a new image by converting a specified image from HSV to RGB color format, one in which each of three bands (respectively representing red, green, and blue color components) is represented by a floating point value ranging from 0 to 1.    

## Syntax

#### Javascript
```
newImage = oldImage.hsvtorgb( ) 
```

- *newImage* is the new image.
- *oldImage* is the specified image.

## Example

#### Javascript
```javascript
var OldIMAGE = ee.Image( 'LC8_L1T/LC80150332014322LGN00' ).select([3,2,1]).unitScale(0,32767);
var HsvIMAGE = OldIMAGE.rgbtohsv( );
var RgbIMAGE = OldIMAGE.hsvtorgb( );
print( OldIMAGE.getInfo(), HsvIMAGE.getInfo(), RgbIMAGE.getInfo()  );
Map.setCenter(-75.8369, 39.4526, 12 );
Map.addLayer( OldIMAGE, { bands:'B4,B3,B2',             min:0,   max:0.5},  'Original Image' );
Map.addLayer( RgbIMAGE, { bands:['red','green','blue'], min:0.1, max:0.55}, 'RGB Image'      );
```
