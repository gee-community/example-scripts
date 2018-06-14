# image.bitwiseAnd,  image.bitwiseOr,  image.bitwiseXor,  image.bitwiseNot,  image.bitwise_and,  image.bitwise_or,  image.bitwise_xor,  *and*  image.bitwise_not
- Create a new image by applying a specified bitwise function the values of corresponding pixels on corresponding bands* of two specified images.
  - If either of two specified images has only one band, then that band is used against all the bands in the other image.  
  - If the images have the same number of bands, but not the same names, they are used in pairwise order. 
  - The output bands are named for the longer of the two specified images, or the first image if they're equal in length.


## Syntax

#### Javascript
```
newImage = 1stImage.bitwiseAnd(2ndImage)
newImage = 1stImage.bitwiseOr(2ndImage)
newImage = 1stImage.bitwiseXor(2ndImage)
newImage = 1stImage.bitwiseNot(2ndImage)
newImage = 1stImage.bitwise_and(2ndImage)
newImage = 1stImage.bitwise_or(2ndImage)
newImage = 1stImage.bitwise_xor(2ndImage)
newImage = 1stImage.bitwise_not(2ndImage)
```

- *newImage* is the new image.
- *1stImage* is the specified first image.
- *2ndImage* is the specified second image.
- *.bitwiseAnd .bitwiseOr .bitwiseXor .bitwiseNot .bitwise_and .bitwise_or .bitwise_xor .bitwise_not* are the specified bitwise functions.


## Example

#### Javascript
```javascript
var FirstIMAGE     = ee.Image( 1 ); 
var SecondIMAGE    = ee.Image( 2 );
var BothBitIMAGE   = FirstIMAGE.bitwiseAnd( SecondIMAGE ); 
var EitherBitIMAGE = FirstIMAGE.bitwise_or( SecondIMAGE ); 
print ( 'Image of bitwise 1s and 2s =', BothBitIMAGE   );
print ( 'Image of bitwise 1s or 2s =',  EitherBitIMAGE );
Map.addLayer( FirstIMAGE,     null, 'Image of 1s' );
Map.addLayer( SecondIMAGE,    null, 'Image of 2s' );
Map.addLayer( BothBitIMAGE,   null, 'Image of Bits from Both' );
Map.addLayer( EitherBitIMAGE, null, 'Image of Bits from Either' );	
```
