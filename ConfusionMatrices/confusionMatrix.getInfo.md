# ConfusionMatrix.getInfo
- creates a JSON-compatible text object representing a specified confusion matrix.
       
## Syntax

#### Javascript

```
newObject = oldConfusionMatrix.getInfo()
```
- *newObject* is the new text object.
- *oldConfusionMatrix* is the specified confusion matrix.
- alternatively, you could also use ee.Algorithms.Describe(oldConfusionMatrix) to achieve the same results

## Example

#### Javascript
```javascript
var TheARRAY           = ee.Array( [ [0,2,0,0],  
                                     [0,1,0,0],  
                                     [0,1,3,1], 
                                     [0,1,3,4]   ] ); 
var TheCONFUSIONMATRIX = ee.ConfusionMatrix( TheARRAY ); 
print( TheCONFUSIONMATRIX.getInfo( ) ); 

//alternatively
print( ee.Algorithms.Describe( TheCONFUSIONMATRIX ) ); 

```
