# imageCollection.qualityMosaic
- Creates a new image by combining the images of an image collection such that each pixel's value is drawn from whichever of those images is of highest quality according to the image collection's quality band. 

## Syntax 

#### Javascript
```
newImage = oldImageCollection.qualityMosaic( qualityBand ) 
```

- *newImage* is the new image.
- *oldImageCollection* is the specified image collection.
- *qualityBand* is the specified quality band, given by its name. 

Argument names used in documentation:

```
https://developers.google.com/earth-engine/api_docs#eeimagecollectionqualitymosaic
```

## Example

#### Javascript
```javascript
var OldIMAGES = ee.ImageCollection('LC8_L1T_TOA').filterDate('2014-06-01','2014-07-01')
                  .filterBounds(ee.Feature.Rectangle(-109.05, 37.0, -102.05, 41.0)  );
var NewIMAGE  = OldIMAGES.qualityMosaic('BQA');
print( OldIMAGES, NewIMAGE );
Map.setCenter( -109.05, 37.0, 5 );
Map.addLayer( NewIMAGE, {'bands':['B4','B3','B2'], min:0, max:0.4, gamma:1.0 } ); 
```
