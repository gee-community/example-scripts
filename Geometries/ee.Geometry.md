# ee.Geometry
- creates a new geometry from a specified GeoJSON object as described [here](http://en.wikipedia.org/wiki/GeoJSON).

## Syntax

#### Javascript
```
newGeometry = ee.Geometry ( oldObject, coordinateSystem, geodesic? )
```

- *newGeometry* is the new geometry.
- *oldObject* is the specified GeoJSON object.
- *coordinateSystem* is a coordinate system that will override whatever one may have been part of the specified GeoJSON object, given as a named (rather than "linked")  CRS code or as a WKT string.  Default: "EPSG:4326" (spheroidal)
- *geodesic* is a Boolean set to True (only) if line segments in the specified coordinate system are to be regarded as drawn on a sphere rather than a plane.  Default: True for spheroidal coordinate systems and False for planar coordinate systems.

## Example

#### Javascript
```javascript
var MultiPOLYGON = ee.Geometry(
  { "type": "MultiPolygon", 
    "coordinates": [ [ [ [31.1319,29.9770], [31.1296,29.9770], [31.1296,29.9750], [31.1319,29.9750] ] 
                     ], 
                     [ [ [31.1330,29.9782], [31.1353,29.9782], [31.1353,29.9802], [31.1330,29.9802] ], 
                       [ [31.1342,29.9792], [31.1352,29.9801], [31.1331,29.9801]                    ]  
                     ] 
                   ]
  }                           );
Map.setCenter( 31.1342, 29.9792, 15 );         
Map.addLayer( MultiPOLYGON );
```
