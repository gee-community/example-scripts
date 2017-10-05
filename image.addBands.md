# image.addBands
- Creates a new image by replicating the first of two specified images and adding to it whatever bands of a second specified image have any of a specified set of names.

## Syntax

#### Javascript
```
newImage = oldImage1.addBands( oldImage2, bandNames, overwrite? )  
```

- *newImage* is the new image.
- *oldImage1* is the first specified image.
- *oldImage2* is the second specified image.
- Optional: *bandNames* is a list of the names of bands to be added.  Default: all bands
- Optional: *overwrite?* is a Boolean set to True (only) if second image’s bands are to overwrite first image’s bands of the same name.  Otherwise, any such band will be renamed by adding the suffix '_1' 
(or '_2', '_3', etc.) to its name.  Default: False 

## Example

#### Javascript
```javascript
var ElevationIMAGE = ee.Image( 'CGIAR/SRTM90_V4' );	
var LandCoverIMAGE = ee.Image( 'MCD12Q1/MCD12Q1_005_2001_01_01' ).select(['Land_Cover_Type_1']).multiply(100) ;
var TwoBandIMAGE = ElevationIMAGE.addBands( LandCoverIMAGE );
print( ElevationIMAGE.getInfo() );  print( LandCoverIMAGE.getInfo() ); print( TwoBandIMAGE.getInfo() );   
Map.setCenter( -97.12, 39.23, 3 );
Map.addLayer( ElevationIMAGE, {min:0, max:1234, opacity:0.5 , gamma:1}, 'Elevation' );
Map.addLayer( LandCoverIMAGE, {min:0, max:1500,   opacity:0.3},           'LandCover' );
Map.addLayer( TwoBandIMAGE,  { bands:['elevation','Land_Cover_Type_1'], gain:0.4, bias:[1,9] }, 'Composite');
```
