# image.atan2
- Creates a new image on which each pixel’s value is computed as the arctangent (angle whose tangent matches the ratio) of two specified numbers:
  - A numerator drawn from the value of the corresponding pixel of the corresponding band* of one specified image, and 
  - A denominator drawn from the value of the corresponding pixel of the corresponding band of another specified image.
- If either of two specified images has only one band, then that band is used against all the bands in the other image. If the images have the same number of bands, but not the same names, they are used in pairwise order. The output bands are named for the longer of the two specified images, or the first image if they're equal in length.      


## Syntax

#### Javascript
```
newImage = 1stImage.atan2(2ndImage) 
```

- *newImage* is the new image, whose values are given in radians as floating-point numbers.
- *1stImage* the specified numerator image.
- *2ndImage* the specified denominator image.


## Example

#### Javascript
```javascript
var YshiftIMAGE = ee.Image.pixelLonLat().select('latitude'); 
var XshiftIMAGE = ee.Image.pixelLonLat().select('longitude'); 
var AngleIMAGE  = XshiftIMAGE.atan2( YshiftIMAGE );
Map.setCenter( 0, 0, 14 );
Map.addLayer( XshiftIMAGE, {min:-0.02,max:0.02, palette:'0000ff, ff0000'}, 'X'          );
Map.addLayer( YshiftIMAGE, {min:-0.01,max:0.01, palette:'0000ff, ff0000'}, 'Y'          );
Map.addLayer( AngleIMAGE,  {min:-3.14,max:3.14, palette:'0000ff, ff0000'}, 'ArcTan(Y/X)');
```
