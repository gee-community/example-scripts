# ConfusionMatrix.consumersAccuracy
- creates a new array indicating the consumer's accuracy(reliability) of a specified confusion matrix.
- computed as the number of correct classifications divided by the the total number of classifications for each row.
       
## Syntax

#### Javascript

```
newArray = oldConfusionMatrix.consumersAccuracy()
```
- *newNumber* is the new number.
- *oldConfusionMatrix* is the specified confusion matrix.

## Example

#### Javascript
```javascript
var TheARRAY           = ee.Array( [ [0,2,0,0],  
                                     [0,1,0,0],  
                                     [0,1,3,1], 
                                     [0,1,3,4]   ] ); 
var TheCONFUSIONMATRIX = ee.ConfusionMatrix( TheARRAY ); 
var NewARRAY           = TheCONFUSIONMATRIX.consumersAccuracy(); 
print (TheCONFUSIONMATRIX);
print( NewARRAY ); 
```
