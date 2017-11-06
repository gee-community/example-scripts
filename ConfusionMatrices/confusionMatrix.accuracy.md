# confusionMatrix.accuracy
- Creates a new floating-point number indicating the accuracy of a specified confusion matrix.
- Computed as the number of correct classifications divided by the total number of classifications.
       
## Syntax

#### Javascript

```
newNumber = oldConfusionMatrix.accuracy()
```
- *newNumber* is the new number.
- *oldConfusionMatrix* is the specified confusion matrix.

## Example

#### Javascript
```javascript
var TheARRAY           =  ee.Array( [ [0,2,0,0],  
                                     [0,1,0,0],  
                                     [0,1,3,1], 
                                     [0,1,3,4]   ] ); 
var TheCONFUSIONMATRIX =  ee.ConfusionMatrix( TheARRAY ); 
var NewNumber           = TheCONFUSIONMATRIX.accuracy(); 
print(TheCONFUSIONMATRIX);
print( NewNumber ); 
```
