# Relationships between values of two images
- Each of these operations create a new grid on which each pixel is set to either 0 or 1 according to whether a specified relationship between its values on two specified images is either true (1) or false (0). 

| Relationship | Operations |
| --- | --- | 
| Equal to | ```.eq()``` |
| Not equal to | ``` .neq()``` |
| Greater than | ``` .gt()``` |
| Greater than or equal to | ``` .gte()``` |
| Less than | ```.lt()``` |
| Less than or equal to | ``` .lte()``` 

## Syntax

#### Javascript
```
newImage = 1stImage.eq(2ndImage) etc.
```

- *newImage* is the new image.
- *1stImage* is the first specified image.
- *2ndImage* is the second specified image.
- *.eq* or any other operation in the table above, questions whether the relationship between the first specified value and the second specified value is true (1) or false (0).

## Example

#### Javascript
```javascript
var UrbanIMAGE   = ee.Image( 'MCD12Q1/MCD12Q1_005_2001_01_01' ).select(['Land_Cover_Type_1']).eq(13) ;
var CoastalIMAGE = ee.Image( 'CGIAR/SRTM90_V4' ).lt(50);
Map.setCenter(-75.3662, 39.8802, 8);
Map.addLayer( UrbanIMAGE,   {palette:['ffffff,dd0000'],opacity:0.6}, 'Urban'   );  
Map.addLayer( CoastalIMAGE, {palette:['ffffff,0000dd'],opacity:0.3}, 'Coastal' );
```
