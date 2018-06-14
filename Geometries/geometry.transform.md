# geometry.transform
-  creates a new geometry by reprojecting a specified geometry to a specified coordinate system, with lines interpreted as either planar or spheroidal according to the planar or spheroidal nature of that coordinate system.

## Syntax

#### Javascript
```
newGeometry = oldGeometry.transform ( coordinateSystem, errorMargin )
```

- *newGeometry* is the new  geometry.
- *oldGeometry* is the specified geometry.
- *coordinateSystem* is The specified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default: WGS84 .
- *errorMargin* is an ErrorMargin object indicating the maximum allowable reprojection error in meters.

  
```

## Example

#### Javascript
```javascript
var OldGEOMETRY = ee.Geometry.Polygon( [ [-109.05, 41], [-109.05, 37], [-102.05, 37], [-102.05, 41] ] );  // Colorado
var NewGEOMETRY = OldGEOMETRY.transform( 'EPSG:2772', ee.ErrorMargin(100) );  
print( OldGEOMETRY, NewGEOMETRY );
Map.centerObject ( NewGEOMETRY, 5 ); 
Map.addLayer( OldGEOMETRY );
Map.addLayer( NewGEOMETRY );
```
