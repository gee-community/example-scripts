# image.and *or* image.or 
- Create a new image on which each pixel is set to 0 or 1 according to whether it is true (1) or false (0) that either (in the case of *or*) or both (in the case of *and*) of its values on two specified images are non-zero (true).


## Syntax

#### Javascript
```
newImage = 1stImage.and(2ndImage)
newImage = 1stImage.or(2ndImage)
```

- *newImage* is the new image.
- *1stImage* is the first specified image.
- *2ndImage* is the second specified image.
- *.and* is the specified relationship, questioning whether *both* of a pixel's values are non-zero.
- *.or* is the specified relationship, questioning whether *either* of a pixel's values are non-zero


## Example

#### Javascript
```javascript
var UrbanIMAGE           = ee.Image( 'MCD12Q1/MCD12Q1_005_2001_01_01' ).select(['Land_Cover_Type_1']).eq(13) ;
var CoastalIMAGE         = ee.Image( 'CGIAR/SRTM90_V4' ).lt(50);
var UrbanAndCoastalIMAGE = UrbanIMAGE.and(CoastalIMAGE);
var UrbanOrCoastalIMAGE  = UrbanIMAGE.or(CoastalIMAGE);
Map.setCenter(-75.3662, 39.8802, 8);
Map.addLayer( UrbanIMAGE,           {palette:['ffffff,dd0000'],opacity:0.6}, 'Urban'   );  
Map.addLayer( CoastalIMAGE,         {palette:['ffffff,0000dd'],opacity:0.3}, 'Coastal' );
Map.addLayer( UrbanAndCoastalIMAGE, {palette:['ffffff,00ff00'],opacity:0.6}, 'Both'    );
Map.addLayer( UrbanOrCoastalIMAGE,  {palette:['ffffff,000000'],opacity:0.3}, 'Either'  );
```
