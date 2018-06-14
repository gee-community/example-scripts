# geometry.length
-  creates a new floating-point number indicating the length of (all parts of) a specified linestring or linearring feature, measured in the units of a specified coordinate system (or meters if no coordinate system is specified).

## Syntax

#### Javascript
```
newNumber = oldFeature.length ( errorMargin, coordinateSystem )
```
- *newNumber* is the new number.
- *oldFeature* is the specified feature.
- *errorMargin* is an ErrorMargin object indicating the maximum  
allowable reprojection error in meters.
- *coordinateSystem* is a specified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here] (http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default:  'EPSG4326' (WGS84) 

## Example

#### Javascript
```javascript
var UpperGEOMETRY = ee.Geometry.LineString( 31.1330,29.9802,  31.1353,29.9802,  31.1353,29.9782,  31.1330,29.9782 );
var LowerGEOMETRY = ee.Geometry.LinearRing( 31.1319,29.9770,  31.1296,29.9770,  31.1296,29.9750,  31.1319,29.9750 );
var UpperNUMBER   = UpperGEOMETRY.length( );   
var LowerNUMBER = LowerGEOMETRY.length( );
Map.setCenter( 31.1342, 29.9792, 15 );   
Map.addLayer( UpperGEOMETRY ); 
Map.addLayer( LowerGEOMETRY );
print( UpperNUMBER, LowerNUMBER );

```
