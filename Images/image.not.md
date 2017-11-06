# image.not
- Creates a new image on which each pixel is set to 0 or 1 each pixel is set to 1 if its value on a specified image is 0, or to 0 if its value on that specified image is other than 0.


## Syntax

#### Javascript
```
newImage = oldImage.not( )
```

- *newImage* is the new image.
- *oldImage* is the specified image.

## Example

#### Javascript
```javascript
var UrbanIMAGE    = ee.Image( 'MCD12Q1/MCD12Q1_005_2001_01_01' ).select(['Land_Cover_Type_1']).eq(13) ;
var NonUrbanIMAGE = UrbanIMAGE.not();
Map.setCenter(-75.3662, 39.8802, 8);
Map.addLayer( UrbanIMAGE,    {palette:['ffffff,660000'],opacity:0.6}, 'Urban'    );  
Map.addLayer( NonUrbanIMAGE, {palette:['ffffff,444400'],opacity:0.4}, 'NonUrban' );
```
