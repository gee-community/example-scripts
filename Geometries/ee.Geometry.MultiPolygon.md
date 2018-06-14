# ee.Geometry.MultiPolygon
- creates a new multiPolygon geometry from a specified sequence of longitude-latitude pairs of coordinates.

## Syntax

#### Javascript
```
newGeometry = ee.Geometry.MultiPolygon ( coordinatePairs )
```

- *newGeometry* is the new MultiPolygon geometry.
- *coordinatePairs* is the specified set of coordinate pairs, given as a list of linestrings (or ee.Geometry.LineString inputs)

## Example

#### Javascript
```javascript
var MultiPOLYGON = ee.Geometry.MultiPolygon( [        
                   ee.Geometry.Polygon([[31.1330,29.9802],[31.1353,29.9802],[31.1353,29.9782],[31.1330,29.9782]]),  
                   ee.Geometry.Polygon([[31.1319,29.9770],[31.1296,29.9770],[31.1296,29.9750],[31.1319,29.9750]])  
                                             ] 
                                           );
Map.setCenter( 31.1342, 29.9792, 15 );     
Map.addLayer( MultiPOLYGON );

```
