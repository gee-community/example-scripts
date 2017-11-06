# image.set
- Creates new image by replicating a specified image after setting or resetting one or more specified properties to specified values.

## Syntax

#### Javascript
```
newImage = oldImage.set ( pairsOfPropertiesAndValues )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *pairsOfPropertiesAndValues* is the specified properties and new values, given as a comma-separated sequence 
(or a dictionary) of property name strings, each immediately followed by its new value

## Example

#### Javascript
```javascript
var OldIMAGE = ee.Image( 0 );
var NewIMAGE = OldIMAGE.set( 'author','Me','label','My Image Collection' );             
print( OldIMAGE.getInfo( ), NewIMAGE.getInfo( ) );
```
