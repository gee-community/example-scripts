# Map.getBounds
- reports the longitude and latitude coordinates of the four edges of the current map display.

## Syntax

#### Javascript
```
bounds = Map.getBounds( )
```

- *bounds* is a list ( or GeoJSON object )  of four numbers respectively indicating the map’s current westerly, southerly, easterly, and northerly coordinates in decimal degrees

## Examples

#### Javascript
```javascript
var TheCOORDINATES = Map.getBounds( );
print( TheCOORDINATES );
```
