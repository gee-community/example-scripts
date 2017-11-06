# confusionMatrix.producersAccuracy
- creates a new array indicating the consumer's accuracy(reliability) of a specified confusion matrix.
- computed as the number of correct classifications divided by the the total number of classifications for each column.
       
## Syntax

#### Javascript

```
newArray = oldConfusionMatrix.producersAccuracy()
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
var NewARRAY           = TheCONFUSIONMATRIX.producersAccuracy(); 
print (TheCONFUSIONMATRIX);
print( NewARRAY ); 
```
