# image.mask
- Creates a new image by applying a specified mask to a specified image. 
- A mask is an image with values ranging from 0 through 1. When applied to another image, these indicate the degree to which that other images pixels should appear as transparent (0) or opaque(1). Pixels with mask values of 0 are also eliminated from subsequent processing.

## Syntax

#### Javascript
```
newImage = oldImage.mask( maskImage )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *maskImage* is the specified mask.


## Example

#### Javascript
```javascript
var OldIMAGE  = ee.Image( 'CGIAR/SRTM90_V4' );
var MaskIMAGE = ee.Image( 'MCD12Q1/MCD12Q1_005_2001_01_01').select(['Land_Cover_Type_1']).neq(9);
var MaskedIMAGE  = OldIMAGE.mask( MaskIMAGE );
print( 'Original Image', OldIMAGE    );  
print( 'Mask Image',     MaskIMAGE   );  
print( 'Masked Image',   MaskedIMAGE );  
Map.setCenter(26.499, -1, 4);
Map.addLayer( OldIMAGE,    { min:0, max:1400, palette:['000000','ff00ff']}, 'Original Elevation' );
Map.addLayer( MaskIMAGE,   { min:0, max:1,    palette:['ff0000','00ff00']}, 'Mask Elevation'     ); 
Map.addLayer( MaskedIMAGE, { min:0, max:1400, palette:['000000','0000ff']}, 'Masked Elevation'   );  
```
