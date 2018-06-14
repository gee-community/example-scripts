# geometry.toString ,   . toGeoJSONString ,    and  .serialize

- all create a new strings presenting information on a specified geometry.

## Syntax

#### Javascript
```
newString = oldGeometry.toString ( )
            oldGeometry.toGeoJSONString( )
            and oldGeometry.serialize( )

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
print( 'New string from geometry.toString( )',        OldGEOMETRY.toString( )        );
print( 'New string from geometry.toGeoJSONString( )', OldGEOMETRY.toGeoJSONString( ) );
print( 'New string from geometry.serialize( )',       OldGEOMETRY.serialize( )       );

```
