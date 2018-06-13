# image.abs,  image.round ,  image.floor ,  image.ceil ,  image.sqrt ,  image.exp ,  image.log,  *and*  image.log10
- Create a new image by applying a specified mathematical function to the value of each pixel on each band of a specified image.

## Syntax

#### Javascript
```
newImage = oldImage.abs()
newImage = oldImage.round()
newImage = oldImage.floor()
newImage = oldImage.ceil()
newImage = oldImage.sqrt()
newImage = oldImage.exp()
newImage = oldImage.log()
newImage = oldImage.log10()
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *.abs .round .floor .ceil .sqrt .exp .log .log10* are the specified mathematical function .


## Example

#### Javascript
```javascript
var AllFEATURES       = ee.FeatureCollection( 'ft:1G3RZbWoTiCiYv_LEwc7xKZq8aYoPZlL5_KuVhyDM' ); // U.S. Cities
var FairbanksFEATURES = AllFEATURES.filterMetadata('city_name', 'contains', 'Fairbanks' );
var DistanceIMAGE     = FairbanksFEATURES.distance( 450000 );
var TransformedIMAGE  = DistanceIMAGE.mod(100000);
Map.setCenter( -147.39, 65.15, 5 );	
Map.addLayer( DistanceIMAGE,    {max:450000, palette:'ff0000,0000ff', opacity:0.8}, 'Distance' );
Map.addLayer( TransformedIMAGE, {max:100000, palette:'ff0000,0000ff'             }, 'Modular Distance' ); 
```
