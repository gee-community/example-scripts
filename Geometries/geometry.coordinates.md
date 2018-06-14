# geometry.coordinates
- creates a new list containing the vertex coordinates for a specified geometry in a GeoJSON format.

## Syntax

#### Javascript
```
newList = oldGeometry.coordinates ( )     
```

- *newList* is the new list.
- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript
var OldGEOMETRY   = ee.Geometry.Polygon(
                               [ [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ], 
                                 [ [-111.05,41],[-111.05,45],[-104.10,45],[-104.10,41] ],
                                 [ [-114.05,37],[-109.05,37],[-109.05,41],[-111.05,41],[-111.05,42],[-114.05,42.0] ]
                                ]      );
var NewLIST = OldGEOMETRY.coordinates( );  
print( OldGEOMETRY, NewLIST );

```
