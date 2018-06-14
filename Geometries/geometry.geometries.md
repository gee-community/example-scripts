# geometry.geometries
- creates a list of the component geometries within a specified geometry.

## Syntax

#### Javascript
```
newList = oldGeometry.geometries ( ) 
```

- *newList* is the new list.
- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon([ [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ], 
                                        [ [-111.05,41],[-111.05,45],[-104.10,45],[-104.10,41] ],
                                        [ [-114.05,37],[-109.05,37],[-109.05,41],[-111.05,41],[-111.05,42],[-114.05,42.0] ]
                                      ] );
var GeometryLIST = TheGEOMETRY.geometries( );    
print( GeometryLIST );

```
