# image.interpolate
- Creates a new image on which which each pixel’s value is calculated as a specified function of its value in the first band of a specified image. This function is specified by explicitly identifying the output value it associates with each of a selected sample set of input values. Other output values are then inferred by interpolating or extrapolating from these samples.

## Syntax

#### Javascript
```
newImage = oldImage.interpolate( listOfTypicalInputs, listOfTypicalOutputs, extrapolationMethod ) 
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *listOfTypicalInputs* is the specified input value samples, given as an array of Doubles in strictly increasing order.
- *listOfTypicalOutputs* is the specified output value samples, given as an array of Doubles in an order corresponding to that of listOfTypicalOutputs. 
- *extrapolationMethod* is the method by which outputs are to be inferred for inputs above or below the range specified in listOfTypicalInputs, given as one of the following four strings.
  - "extrapolate" means extrapolate from the two nearest inputs.
  - "clamp" means use the nearest input.
  - "input" means use the pixel’s original value.
  - "mask" means mask the pixel.
  
Argument names used in Docs:
```
newImage = oldImage.interpolate( x, y, behavior )
```


## Example

#### Javascript
```javascript
var AllFEATURES         = ee.FeatureCollection( 'ft:1G3RZbWoTiCiYv_LEwc7xKZq8aYoPZlL5_KuVhyDM' );    // U.S. Cities
var SomeFEATURES        = AllFEATURES.filterMetadata('city_name', 'contains', 'Houston' );
var DistanceIMAGE       = SomeFEATURES.distance( 800000 );
var DistanceEffectIMAGE = DistanceIMAGE.interpolate( [ 0.0, 100000.0, 200000.0, 300000.0, 400000.0 ],
                                                     [ 0,       60,       90,      100,       75 ], 'extrapolate' );
Map.centerObject( SomeFEATURES, 5 );	
Map.addLayer( DistanceIMAGE,       {min:0, max:800000, palette:'0000dd,ff0000'}, 'Distance' );
Map.addLayer( DistanceEffectIMAGE, {min:0, max:100,    palette:'0000dd,ff0000'}, 'Distance Effect'   );
```
