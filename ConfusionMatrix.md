# ConfusionMatrix
- creates a new confusion matrix from a specified two-dimensional array whose
        a) horizontal rows (axis 1) represent known classes
        b) vertical columns (axis 0) represent predicted classes
        c) values indicate the number cases in which a given known value was classfified as a given predicted value
        
## Syntax

#### Javascript

```
newConfusionMatrix = ee.ConfusionMatrix(array,order)
```
- *newConfusionMatrix* is the new confusion matrix.
- *array* is the specified array.
- *order* is the row and column size and order of a non-contiguous or non-zero matrix, given as a list.

## Example

#### Javascript

var TheARRAY           = ee.Array( [ [0,2,0,0],  
                                     [0,1,0,0],  
                                     [0,1,3,1], 
                                     [0,1,3,4]   ] ); 
var TheCONFUSIONMATRIX = ee.ConfusionMatrix( TheARRAY ); 
print( TheCONFUSIONMATRIX ); 
