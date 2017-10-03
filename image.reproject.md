# image.reproject
- creates a new image by reprojecting a specified image to a specified coordinate system, geographical placement, and pixel size.

## Syntax

#### Javascript
```
newImage = oldImage.reproject ( coordinateSystem, placementCoefficients, pixelSize )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- Optional: *coordinateSystem* is the specified coordinate system, given as an [EPSG code](http://spatialreference.org/) or as a [WKT string](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT).  Default: WGS84 
- Optional: *placementCoefficients* is a sequence of six numbers (of type Double) that indicate how the image is to be resized, reoriented, and repositioned with respect to the specified coordinate system.  If pixelSize is specified, this should not.
- Optional: *pixelSize* is a number indicating the width of the new image’s pixels in meters.  If placementCoefficients is specified, this should not.

## Example

#### Javascript
```javascript
var OldIMAGE    = ee.Image( 'CGIAR/SRTM90_V4'  ); 
var NewIMAGE = OldIMAGE.reproject( 'EPSG:3191', null, 50000 );
print( OldIMAGE, NewIMAGE );
Map.setCenter ( 10, 10, 3 );
Map.addLayer( OldIMAGE, { min:0, max:2000, palette:['000000','ffffff']          }, 'Original'    );
Map.addLayer( NewIMAGE, { min:0, max:1200, palette:['ff0000','00ff00','0000ff'] }, 'Reprojected' );
```
