# feature.transform 
- creates a new feature by reprojecting a specified feature to a specified coordinate system, with lines interpreted as either planar or spheroidal according to the planar or spheroidal nature of that coordinate system.

## Syntax

#### Javascript
```
newFeature = oldFeature.transform ( coordinateSystem, errorMargin )
```

- *newFeature* is the new feature.
- *oldGeometry* is the specified geometry, given as an EE geometry object or as a GeoJSON object representing either a geometry or a feature.
- *coordinateSystem* is the specified coordinate system, given as an EPSG code ( as described here ) or as a WKT string ( as described here ).  Default: WGS84
- *errorMargin* is a ErrorMargin object indicating the maximum allowable reprojection error in meters



Arguments used in documentation:
```
newFeature = oldFeature.transform (gproj, maxError) 
```

## Example

#### Javascript
```javascript
var OldGEOMETRY = ee.Geometry.Polygon( [ [-109.05, 41], [-109.05, 37], [-102.05, 37], [-102.05, 41] ] ); // Colorado
var OldFEATURE  = ee.Feature( OldGEOMETRY, {name:'Colorado'} );
var NewFEATURE  = OldFEATURE.transform( 'EPSG:2772', 100 );
print( OldFEATURE, NewFEATURE );
Map.centerObject( OldFEATURE ); 
Map.addLayer( OldFEATURE );
Map.addLayer( NewFEATURE );
```
