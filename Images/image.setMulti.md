# image.setMulti
- Creates a new image by replicating a specified image after setting or resetting one or more specified properties to specified values. 

## Syntax

#### Javascript
```
newImage = oldImage.setMulti( dictionaryOfPropertiesAndValues )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *dictionaryOfPropertiesAndValues* is the specified properties and new values, given as a dictionary of property name strings and new values.

Argument names used in Docs:
```
newImage = oldImage.setMulti( dictionary )
```

## Example

#### Javascript
```javascript
var OldIMAGE = ee.Image( 0 );
var NewIMAGE = OldIMAGE.setMulti( {'author':'Me', 'label':'My Image Collection'} );             
print( OldIMAGE, NewIMAGE );
```
