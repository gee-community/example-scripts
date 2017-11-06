# image.where
- Creates a new image on which each pixel is set to the value of that pixel on one of two specified images.  The choice depends on whether the pixel’s value on a specified “test” image is	
    - equal to 0, in which case its new value is drawn from the first specified image; or
    - other than 0, in which case its new value is drawn from the second specified image.

## Syntax

#### Javascript
```
newImage = nonZeroImage.where( testImage, zeroImage ) 
```

- *newImage* is the new image.
- *nonZeroImage* is the specified image whose values are to be assigned wherever testImage values are equal to 0.  
- *testImage* is the specified "test" image.
- *zeroImage* is the specified image whose values are to be assigned where testImage values are other than 0.  This can also be specified as a number to represent an image of constant value.


Argument names used in Docs:
```
newImage = nonZeroImage.where( test, value ) 
```

## Example

#### Javascript
```javascript
var LandcoverPALETTE  = ['aec3d4','152106','225129','369b47','30eb5b','387242','6a2325','c3aa69','b76031','d9903d',
                         '91af40','111149','cdb33b','cc0013','33280d','d7cdcc','f7e084','6f6f6f','000000'].join(',');
var LandcoverIMAGE    = ee.Image('MCD12Q1/MCD12Q1_005_2001_01_01').select('Land_Cover_Type_1');
var ElevationIMAGE    = ee.Image('srtm90_v4');
var UplandIMAGE       = ElevationIMAGE.gt( 100 );
var LowlandcoverIMAGE = LandcoverIMAGE.where( UplandIMAGE, 18 );
Map.setCenter( 19.644, 45.784, 6 );
Map.addLayer( LandcoverIMAGE,    {palette:LandcoverPALETTE,opacity:0.3, min:0, max:18  }, 'Landcover'         );
Map.addLayer( ElevationIMAGE,    {palette:'000000,ffffff', opacity:0.3, min:0, max:1000}, 'Elevation'         );
Map.addLayer( UplandIMAGE,       {palette:'ffffff,000000', opacity:0.3, min:0, max:1,  }, 'Uplands'           );
Map.addLayer( LowlandcoverIMAGE, {palette:LandcoverPALETTE,opacity:1.0, min:0, max:18  }, 'Lowland Landcover' );
```
