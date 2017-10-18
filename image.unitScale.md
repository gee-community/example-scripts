# image.clamp
- Creates a new image of floating-point values on which 
  - each pixel at or below a specified minimum value is set to 0.0, 
  - each pixel at or above a specified maximum value is set to 1.0, 
  - and all other pixels are set to values between 0.0 and 1.0 in proportion to their position between those extremes.
 

## Syntax

#### Javascript
```
newImage = oldImage.unitScale( minimumValue, maximumValue ) 
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *minimumValue* is the specified minimum value, given as a Double.
- *maximumValue* is the specified maximum value, given as a Double.


Argument names used in Docs:
```
newImage = oldImage.unitScale( low, high ) 
```

## Example

#### Javascript
```javascript
var ElevationIMAGE = ee.Image('srtm90_v4').unitScale( 0,1000 );
var AspectIMAGE    = ee.Terrain.aspect( ElevationIMAGE ).unitScale( 0,360 );
var NewIMAGE       = ElevationIMAGE.add(AspectIMAGE).divide(2);
Map.setCenter( -83.518, 39.504, 6 );
Map.addLayer(ElevationIMAGE, { min:0, max:1, palette:['0000aa,00aa00,ffff00,990000'] }, 'Elevation');
Map.addLayer(AspectIMAGE,    { min:0, max:1, palette:['0000aa,00aa00,ffff00,990000'] }, 'Aspect');
Map.addLayer(NewIMAGE,       { min:0, max:1, palette:['0000aa,00aa00,ffff00,990000'] }, 'Elevation-Aspect Mean');
```
