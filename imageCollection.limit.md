# imageCollection.limit
- creates new image collection that contains only the first of a specified number of elements from a specified image collection 

## Syntax

#### Javascript
```
newImageCollection = oldImageCollection.limit ( max, property, ascending )
```

- *newImageCollection* is the new image collection.
- *oldImageCollection* is the specified image collection.
- *max* is the specified number of elements, given as an integer.
- Optional: *property* is the specified property, given as a string.
- Optional: *ascending* is the specified order, given as a Boolean set to True for ascending or False for descending.

## Example

#### Javascript
```javascript
var OldIMAGES    = ee.ImageCollection( 'LC8_L1T_TOA' ).filterDate( '2014-10-03','2014-10-04' );    
var NewIMAGES    = OldIMAGES.limit( 15 );
print( OldIMAGES, NewIMAGES );
Map.setCenter( -73.015, 41.228, 3 );                                                         
Map.addLayer( OldIMAGES, {bands:'B4,B3,B2', min:0, max:0.2, opacity:0.4}, 'Original Images' );
Map.addLayer( NewIMAGES, {bands:'B4,B3,B2', min:0, max:0.4, opacity:1.0}, 'Limited Images'  );

```
