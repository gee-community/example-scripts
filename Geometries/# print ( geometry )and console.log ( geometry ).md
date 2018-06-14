# print ( geometry )and console.log ( geometry )	      
- present JSON-formatted text renditions of a specified geometry in the console.

## Syntax

#### Javascript
```
print( oldGeometry ) or console.log( oldGeometry )
```

- *oldGeometry* is the specified geometry.

## Example

#### Javascript
```javascript
var TheGEOMETRY = ee.Geometry.Polygon( [ [-109.05, 41], [-109.05, 37], [-102.05, 37], [-102.05, 41] ] );  // Colorado
print( TheGEOMETRY );
console.log( TheGEOMETRY );

```
