# Name of Method
- reports the Map ID and token associated with a specified asset

## Syntax

#### Javascript
```
newObject = ee.data.getMapId ( settings )
```

- *newObject* is a dictionary of strings associated with two keys: “mapid” and “token” 
- *settings* is instructions identifying data and data-display options in the same manner as Map.addlayer settings but with an additional setting given as 'id':  followed by the asset ID for a feature, feature collection, image, or image collection

## Examples

#### Javascript
```javascript
var TheMAPID = ee.data.getMapId( {'id':'srtm90_v4', min:0, max:700, palette:'001100,009900'} );
print( TheMAPID );
```
