# ConfusionMatrix.array
- creates a creates a new two-dimensional array from a specified confusion matrix.
       
## Syntax

#### Javascript

```
newArray = oldConfusionMatrix.array()
```
- *newArray* is the new array.
- *oldConfusionMatrix* is the specified confusion matrix.

## Example

#### Javascript
```javascript
var TheARRAY           = ee.Array( [ [0,2,0,0],  
                                     [0,1,0,0],  
                                     [0,1,3,1], 
                                     [0,1,3,4]   ] ); 
var TheCONFUSIONMATRIX = ee.ConfusionMatrix( TheARRAY ); 
var NewARRAY           = TheCONFUSIONMATRIX.array(); 
print( NewARRAY ); 
```
