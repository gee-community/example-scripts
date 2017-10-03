# ee.Image.pixelArea
- Creates a new image in which each pixel is set to a value indicating its area in meters.

## Syntax

#### Javascript
```
newImage = ee.Image.pixelArea(  )
```

- *newImage* is the new image.

## Example

#### Javascript
```javascript
var NewIMAGE = ee.Image.pixelArea( );
print( NewIMAGE.getInfo( ) );   
Map.addLayer( NewIMAGE, {min: 2e8, max: 4e8, opacity: 0.85});
```
