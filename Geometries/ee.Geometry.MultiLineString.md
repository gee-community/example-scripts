# ee.Geometry.MultiLineString.md
-  creates a new multiLineString geometry from a specified sequence of longitude-latitude pairs of coordinates.

## Syntax

#### Javascript
```
newGeometry = ee.Geometry.MultiLineString ( coordinatePairs )
```

- *newGeometry* is the new MultiLineString geometry.
- *coordinatePairs* is the specified set of coordinate pairs, given as a list of linestrings (or ee.Geometry.LineString inputs)


## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.MultiLineString( [ [ [31.1330,29.9802], [31.1353,29.9802], [31.1353,29.9782], [31.1330,29.9782] ], 
       			                             [ [31.1319,29.9770], [31.1296,29.9770], [31.1296,29.9750], [31.1319,29.9750] ] 
                                                  ]
                                                 );
Map.centerObject( TheGEOMETRY,15 );       
Map.addLayer( TheGEOMETRY ); 


```
