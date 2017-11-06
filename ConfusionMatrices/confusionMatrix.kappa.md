# confusionMatrix.kappa
- Creates a new floating-point number indicating the Kappa statistic for a specified confusion matrix.
- This measures the agreement between two datasets on a scale that genereally ranges from 0 to 1.
       
## Syntax

#### Javascript

```
newNumber = oldConfusionMatrix.kappa()
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
var NewNumber           = TheCONFUSIONMATRIX.kappa(); 
print( TheCONFUSIONMATRIX ); 
print( NewNumber ); 
```
