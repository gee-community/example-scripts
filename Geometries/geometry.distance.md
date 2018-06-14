# geometry.distance
- creates a new floating-point number indicating the distance in meters between the closest parts of two specified geometries.

## Syntax

#### Javascript
```
newNumber = 1stGeometry.distance ( 2ndGeometry, errorMargin, coordinateSystem )
```

- *newNumber* is the new number.
- *1stGeometry* is the first specified geometry.
- *2ndGeometry* is the second specified geometry.
- *errorMargin* is an ErrorMargin object indicating the maximum allowable reprojection error in meters.
- *coordinateSystem* is a specified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default:  'EPSG4326' (WGS84) 

## Example

#### Javascript
```javascript
var UpperPOLYGON = ee.Geometry( { "type": "Polygon",
                           "coordinates": [ [ [31.1330,29.9782],[31.1353,29.9782],[31.1353,29.9802],[31.1330,29.9802] ], 
                                            [ [31.1342,29.9792],[31.1352,29.9801],[31.1331,29.9801]                   ] ] } );
var LowerPOLYGON = ee.Geometry( { "type": "Polygon", 
                           "coordinates": [ [ [31.1319,29.9770],[31.1296,29.9770],[31.1296,29.9750],[31.1319,29.9750] ] ] } );
var TheNUMBER    = UpperPOLYGON.distance( LowerPOLYGON );     
Map.setCenter( 31.1342, 29.9792, 15 );   
Map.addLayer( UpperPOLYGON );   
Map.addLayer( LowerPOLYGON );
print( TheNUMBER

```
