# ConfusionMatrix.order
- creates a new list indicating the name and order of the rows and columns of a specified confusion matrix.
       
## Syntax

#### Javascript

```
newList = oldConfusionMatrix.order()
```
- *newList* is the new list of name and order of rows and columns.
- *oldConfusionMatrix* is the specified confusion matrix.

## Example

#### Javascript
```javascript
var TheARRAY           = ee.Array( [ [0,2,0,0],  
                                     [0,1,0,0],  
                                     [0,1,3,1], 
                                     [0,1,3,4]   ] ); 
var TheCONFUSIONMATRIX = ee.ConfusionMatrix( TheARRAY, [3,2,1,0] ); 
var NewLIST            = TheCONFUSIONMATRIX.order(); 
print( TheCONFUSIONMATRIX ); 
print( NewLIST ); 
```
