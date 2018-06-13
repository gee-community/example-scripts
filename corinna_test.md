# image.clamp
- Creates a new image on which each pixel is set to its value on a specified image unless that value is greater than a specified maximum.

## Syntax

#### Javascript
```
newImage = oldImage.clamp( minimumValue, maximumValue )  
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *minimumValue* is the specified minimum value
- *maximumValue* is the specified maximum value

Argument names used in documentation:
```

```

## Example

#### Javascript
```javascript
var OldIMAGE = ee.Image('srtm90_v4');
var NewIMAGE = OldIMAGE.clamp(200, 650);
Map.setCenter( -83.518, 39.504, 6 );
Map.addLayer(OldIMAGE, { min:0, max:1000, palette:['0000aa,00aa00,ffff00,990000'] }, 'Unclamped');
Map.addLayer(NewIMAGE, { min:0, max:1000, palette:['0000aa,00aa00,ffff00,990000'] }, 'Clamped');
