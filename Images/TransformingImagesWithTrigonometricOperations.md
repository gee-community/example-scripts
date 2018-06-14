# image.sin,  image.cos,  image.tan,  image.sinh,  image.cosh,  image.tanh,  image.asin, image.acos,  *and*  image.atan
- Create a new image by applying a specified trigonometric function to the value of each pixel on each band of a specified image.

## Syntax

#### Javascript
```
newImage = oldImage.sin()
newImage = oldImage.cos()
newImage = oldImage.tan()
newImage = oldImage.sinh()
newImage = oldImage.cosh()
newImage = oldImage.tanh()
newImage = oldImage.asin()
newImage = oldImage.acos()
newImage = oldImage.atan()
```

- *newImage* is the new image.
- *oldImage* is the specified image, with values assumed to be in radians.
- *.sin .cos .tan .sinh .cosh .tanh .asin .acos .atan* are the specified trigoonometric function .


## Example

#### Javascript
```javascript
var YshiftIMAGE = ee.Image.pixelLonLat( ).select( 'latitude'  ); 
var XshiftIMAGE = ee.Image.pixelLonLat( ).select( 'longitude' ); 
var AngleIMAGE  = XshiftIMAGE.atan2( YshiftIMAGE );
var SinIMAGE    = AngleIMAGE.sin( );
var CosIMAGE    = AngleIMAGE.cos( );
Map.setCenter( 0, 0, 14 );
Map.addLayer( XshiftIMAGE, {min:-0.02,max:0.02, palette:'0000ff, ff0000'}, 'X'          );
Map.addLayer( YshiftIMAGE, {min:-0.01,max:0.01, palette:'0000ff, ff0000'}, 'Y'          );
Map.addLayer( AngleIMAGE,  {min:-3.14,max:3.14, palette:'0000ff, ff0000'}, 'ArcTan(Y/X)');
Map.addLayer( SinIMAGE,    {min:-1,   max:1   , palette:'0000ff, ff0000'}, 'Sine'       );
Map.addLayer( CosIMAGE,    {min:-1,   max:1   , palette:'0000ff, ff0000'}, 'Cosine'     );
```
