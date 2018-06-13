# ee.Geometry.Polygon
- creates a new polygon geometry from a specified sequence of longitude-latitude pairs of coordinates. Though coordinates may be specified in either clockwise or counterclockwise order, the latter is usually preferable for reasons described here [MISSING LINK].

## Syntax

#### Javascript
```
newGeometry = ee.Geometry.Polygon ( coordinatePairs )
```
- *newGeometry* is the new polygon geometry.
- *coordinatePairs* is the specified set of coordinate pairs, given as a list of one or more sub-lists.  The first sub-list defines the polygon’s exterior perimeter by listing its vertices, each given as a [lon,lat] sub-sublist of coordinates.  Any subsequent sub-list defines one of the polygon’s holes in the same manner.



## Example

#### Javascript
```javascript
var ThePOLYGON  = ee.Geometry.Polygon( [ [ [31.1330,29.9802], [31.1353,29.9802], [31.1353,29.9782], [31.1330,29.9782] ], 
                                         [ [31.1331,29.9801], [31.1352,29.9801], [31.1342,29.9792]                    ]  ] );
Map.setCenter( 31.1342, 29.9792, 17 );         
Map.addLayer( ThePOLYGON );
```
