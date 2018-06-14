# geometry.area
-  creates a new floating-point number indicating the total area of (all parts of) a specified polygonal geometry, measured in the squared units of a specified coordinate system (or square meters if no coordinate system is specified).  Point and line geometries result in an area of 0. Polygons with clockwise vertices are regarded as holes in a global polygon for purposes of area measurement.

## Syntax

#### Javascript
```
newNumber = oldGeometry.area ( errorMargin, coordinateSystem )
```

- *newNumber* is the new number.
- *oldGeometry* is the specified geometry.
- *errorMargin* is an ErrorMargin object indicating the maximum allowable reprojection error in meters.
- *coordinateSystem* is a specified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default:  'EPSG4326' (WGS84) 

## Example

#### Javascript
```javascript
var UpperPOLYGON     = ee.Geometry( { "type": "Polygon",
                           "coordinates": [ [ [31.1330,29.9782],[31.1353,29.9782],[31.1353,29.9802],[31.1330,29.9802] ], 
                                            [ [31.1342,29.9792],[31.1352,29.9801],[31.1331,29.9801]                   ] ] } );
var LowerPOLYGON     = ee.Geometry( { "type": "Polygon", 
                           "coordinates": [ [ [31.1319,29.9770],[31.1296,29.9770],[31.1296,29.9750],[31.1319,29.9750] ] ] } );
var ClockwisePOLYGON = ee.Geometry(
      { "type": "Polygon", "coordinates": [ [ [31.1330,29.9802],[31.1353,29.9802],[31.1353,29.9782],[31.1330,29.9782] ] ] } );
var UpperNUMBER      = UpperPOLYGON.area( ); 
var LowerNUMBER      = LowerPOLYGON.area( ); 
var ClockwiseNUMBER  = ClockwisePOLYGON.area( );
Map.setCenter( 31.1342, 29.9792, 15 );   
Map.addLayer( UpperPOLYGON, null, 'Upper Polygon' );
Map.addLayer( LowerPOLYGON, null, 'Lower Polygon'  );
Map.addLayer( ClockwisePOLYGON, null, 'Clockwise Polygon'  );
print( UpperNUMBER, LowerNUMBER, ClockwiseNUMBER );
```
