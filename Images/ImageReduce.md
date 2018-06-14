# image.reduce
- Create a new image on which each pixel’s value is calculated by applying a specified reducer to its values on all bands of a specified image.


## Syntax

#### Javascript
```
newImage = oldImage.reduce(reducer)
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *reducer* is the specified reducer.


## Example

#### Javascript
```javascript
var TheREDUCER     = ee.Reducer.std_dev( );
var MultibandIMAGE = ee.Image( 'LC8_L1T_TOA/LC80410362015107LGN00' ).select( ['B4','B3','B2'] );   // Los Angeles
var ReducedIMAGE   = MultibandIMAGE.reduce( TheREDUCER );
Map.setCenter( -118.5054, 34.2016, 10 ); 
Map.addLayer( MultibandIMAGE, {min:0, max:0.17, gamma:0.5, bands:'B4,B3,B2'}, 'Multiband Image' );
Map.addLayer( ReducedIMAGE,   {min:0, max:0.015, palette:'000000,ffffff'},    'Deviation Image' );
```
