# ee.Algorithms.Describe ,   geometry.getInfo ,  and   geometry.toGeoJSON
- each creates a JSON-compatible text object representing a specified geometry.

## Syntax

#### Javascript
```
newObject = ee.Algorithms.Describe ( oldGeometry )
            oldGeometry.getInfo( )
            and oldGeometry.toGeoJSON( )

```

- *newObject* is the new object.
- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript
var OldGEOMETRY   = ee.Geometry.Polygon(
                               [ [ [-109.05,41],[-109.05,37],[-102.05,37],[-102.05,41] ], 
                                 [ [-111.05,41],[-111.05,45],[-104.10,45],[-104.10,41] ],
                                 [ [-114.05,37],[-109.05,37],[-109.05,41],[-111.05,41],[-111.05,42],[-114.05,42.0] ]
                                ]      );
print( 'New Dictionary from original geometry',      OldGEOMETRY                           );
print( 'New Dictionary from ee.Algorithms.Describe', ee.Algorithms.Describe( OldGEOMETRY ) );
print( 'New Dictionary from geometry.getInfo( )',    OldGEOMETRY.getInfo( )                );
print( 'New Dictionary from geometry.toGeoJSON( )',  OldGEOMETRY. toGeoJSON( )             );

```
