# ee.Algorithms.Landsat.simpleComposite.md
- simpleComposite  creates a new image by replicating a specified Landsat image collection after recalibrating its scenes, computing cloud scores, and limiting it to the least cloudy scenes as defined by specified parameters.

## Syntax

#### Javascript
```
newImage = ee.Algorithms.Landsat.simpleComposite ( oldImageCollection, percentileLimit, cloudScoreRangeLimit, scenesLimit, floatingPoint)
```

- *newImage* is the new image.
- *oldImageCollection* is the specified the Landsat image collection 
- *percentileLimit* is the percentile limit on acceptable cloud scores, given as an integer.  Default: 50. 
- *cloudScoreRangeLimit* is the maximum acceptable range of cloud scores per pixel, given as an integer. Default: 10
- *scenesLimit* is the (approximate) limit on how many scenes are to be considered  for any one pixel, given as an integer.  Default: 40
- *floatingPoint* is A Boolean set to true (only) if output is to employ the same units as Landsat.TOA operation. Otherwise, they are integers. Default: false


Argument names used in documentation:
```
https://developers.google.com/earth-engine/api_docs#eealgorithmslandsatsimplecomposite
```

## Example

#### Javascript
```
var OldIMAGES = ee.ImageCollection('LANDSAT/LC8_L1T').filterDate('2015-1-1', '2015-5-1');
var NewIMAGE  = ee.Algorithms.Landsat.simpleComposite( OldIMAGES, 50, 10, 40, true );
Map.setCenter( -66.4261, 18.2505, 9 );
Map.addLayer( NewIMAGE, {bands: 'B7,B6,B1', max: [0.3, 0.4, 0.3]});


var ClassifiedIMAGE     = BandSelectedIMAGE.classify( TrainedCLASSIFIER );
print( 'Image of All Bands',            OriginalIMAGE );
print( 'Image of Selected Bands',       BandSelectedIMAGE );
print( 'Features by Class',             ClassCodedFEATURES );
print( 'Features with Band Properties', BandCodedFEATURES );
print( 'Untrained Classifier',          UntrainedCLASSIFIER );
print( 'Trained Classifier',            TrainedCLASSIFIER );
Map.centerObject( BandSelectedIMAGE, 8 );
Map.addLayer( OriginalIMAGE,      
    {bands:['B4','B3','B2'], max: 0.4},           'Original Image');
Map.addLayer( ClassifiedIMAGE,    
    {min:0, max:1, palette:['007700', '999900']}, 'Classified Image');
Map.addLayer( ClassCodedFEATURES, 
    {color:'0000ff'},                             'Training Points' );

```
