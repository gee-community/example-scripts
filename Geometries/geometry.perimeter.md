# geometry.perimeter
- creates a new floating-point number indicating the perimeter of (all parts of) a specified polygonal geometry, measured in the units of a specified coordinate system (or meters if no coordinate system is specified).  Point and line geometries result in a perimeter of 0.

## Syntax

#### Javascript
```
newNumber = oldGeometry.perimeter ( errorMargin, coordinateSystem )
```

- *newNumber* is the new number.
- *oldGeometry* is the specified geometry.
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
var UpperNUMBER  = UpperPOLYGON.perimeter( );   
var LowerNUMBER  = LowerPOLYGON.perimeter( );
Map.setCenter( 31.1342, 29.9792, 15 );   
Map.addLayer( UpperPOLYGON );   
Map.addLayer( LowerPOLYGON );
print( UpperNUMBER, LowerNUMBER );
```
