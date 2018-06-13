# image.clamp
- Creates a new image on which each pixel is set t each value on a specified image unless that value is greater than a specified maximum or lower than a specified minimum, in which case the pixel is set to the closest of those specified maximum and minimum values.

## Syntax

#### Javascript
```
newImage = oldImage.clamp( minimumValue, maximumValue )
```
- *newImage* is the new image.
- *The specified image* is the old image.
- *The specified minimum value* is the specified minimum value.
- *The specified maximum value* is the specified maximum value.
```

## Example

#### Javascript
```javascript
var OldIMAGE = ee.Image('srtm90_v4');
var NewIMAGE = OldIMAGE.clamp(200, 650);
Map.setCenter( -83.518, 39.504, 6 );
Map.addLayer(OldIMAGE, { min:0, max:1000, palette:['0000aa,00aa00,ffff00,990000'] }, 'Unclamped');
Map.addLayer(NewIMAGE, { min:0, max:1000, palette:['0000aa,00aa00,ffff00,990000'] }, 'Clamped');
```
