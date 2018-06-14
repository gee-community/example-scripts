 # ee.Algorithms.Landsat.simpleCloudScore.md
- creates a new image by replicating a specified Landsat image after adding to it a band on which each pixel is set to a value ranging from 0 through 100 to indicate to indicate the percent likelihood that the pixel is part of a cloud. 


## Syntax

#### Javascript
```
newImage = ee.Algorithms.Landsat.simpleCloudScore( oldImage ) 
```

- *newImage* is the new image.
- *oldImage* is the specified Landsat image. 

Argument names used in documentation:
```
https://developers.google.com/earth-engine/api_docs#eealgorithmslandsatsimplecloudscore
```

## Example

#### Javascript
```
var TheALGORITHM = function ( TypicalIMAGE ) 
     {var TheIMAGE = TypicalIMAGE.select( ['B2','B3','B4','B5','B6','B7','B10','B11'] );
      var OldScore = ee.Algorithms.Landsat.simpleCloudScore( TheIMAGE );
      var NewScore = ee.Image( 1 ).subtract( OldScore ).select( [0], ['cloudscore'] );
      return TypicalIMAGE.addBands( NewScore );
     };
var OldIMAGES = ee.ImageCollection('LC8_L1T_TOA').filterDate('2013-05-01', '2013-06-01');
var NewIMAGES = OldIMAGES.map( TheALGORITHM );
var NewIMAGE  = NewIMAGES.qualityMosaic('cloudscore');
Map.setCenter(-120.24487, 37.52280, 9);
Map.addLayer( OldIMAGES, {'bands':['B4','B3','B2'], 'max':0.4, 'gamma':1.6}, 'Original Image Collection'  );
Map.addLayer( NewIMAGE,  {'bands':['B4','B3','B2'], 'max':0.4, 'gamma':1.6}, 'Less Cloudy Mosaicked Image');

``` 
