# image.add,  image.subtract,  image.multiply,  image.divide,  image.max,  image.min,  image.mod,  image.pow,  image.hypot,  image.first,  *and*  image.first_nonzero
- Create a new image by applying a specified mathematical function the values of corresponding pixels on corresponding bands of two specified images.
  - If either of two specified images has only one band, then that band is used against all the bands in the other image.  
  - If the images have the same number of bands, but not the same names, they are used in pairwise order. 
  - The output bands are named for the longer of the two specified images, or the first image if they're equal in length.      


## Syntax

#### Javascript
```
newImage = 1stImage.add(2ndImage)
newImage = 1stImage.subtract(2ndImage)
newImage = 1stImage.multiply(2ndImage)
newImage = 1stImage.divide(2ndImage)
newImage = 1stImage.max(2ndImage)
newImage = 1stImage.min(2ndImage)
newImage = 1stImage.mod(2ndImage)
newImage = 1stImage.pow(2ndImage)
newImage = 1stImage.hypot(2ndImage)
newImage = 1stImage.first(2ndImage)
newImage = 1stImage.first_nonzero(2ndImage)
```

- *newImage* is the new image, whose pixel type is defined by the union of the pixel types of the two specified images.
- *1stImage* is the specified first image.
- *2ndImage* is the specified second image.
- *.add .subtract .multiply .divide .max .min .mod .pow hypot first first_nonzero* are the specified mathematical function .


## Example

#### Javascript
```javascript
var AllFEATURES          = ee.FeatureCollection( 'ft:1G3RZbWoTiCiYv_LEwc7xKZq8aYoPZlL5_KuVhyDM' ); // U.S. Cities
var FairbanksFEATURES    = AllFEATURES.filterMetadata('city_name', 'contains', 'Fairbanks' );
var AnchorageFEATURES    = AllFEATURES.filterMetadata('city_name', 'contains', 'Anchorage' );
var FairbanksIMAGE       = FairbanksFEATURES.distance( 450000 );
var AnchorageIMAGE       = AnchorageFEATURES.distance( 450000 );
var MinimumDistanceIMAGE = FairbanksIMAGE.min(AnchorageIMAGE);
var TotalDistanceIMAGE   = FairbanksIMAGE.add(AnchorageIMAGE);
Map.setCenter( -148.623, 63.47, 5 );	
Map.addLayer( FairbanksIMAGE,       {max:450000, palette:'ff0000,ffffff', opacity:0.5}, 'Distance to Fairbanks' );
Map.addLayer( AnchorageIMAGE,       {max:450000, palette:'0000ff,ffffff', opacity:0.5}, 'Distance to Proximity' );
Map.addLayer( MinimumDistanceIMAGE, {max:450000, palette:'444444,ffffff'},              'Distance to Nearest'   );
Map.addLayer( TotalDistanceIMAGE,   {min:400000, max:900000, gamma:2.5, },              'Distance to Both'      );	
```
