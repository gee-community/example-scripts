# Converting image pixel types
- Each of these operations replicates a specified image (of any pixel type) to create a new one whose pixel type is as indicated accordingly.

| Pixel Type | Operations |
| --- | --- | 
| unsigned 8-bit integers | ```.uint8()     .toUint8()    .byte()   .toByte()``` |
| unsigned 16-bit integers | ``` .uint16()    .toUint16()``` |
| unsigned 32-bit integers | ``` .uint32()    .toUint32()``` |
| signed 8-bit integers | ``` .int8()     .toInt8()``` |
| signed 16-bit integers | ``` .int16()    .toInt16()   .short()    .toShort()``` |
| signed 32-bit integers | ``` .int32()    .toInt32()   .int()    .toInt()``` |
| signed 64-bit integers | ``` .int64()    .toInt64()   .long()   .toLong()``` |
| 32-bit floating point numbers | ``` .float()    .toFloat()``` |
| 64-bit floating point numbers| ``` .double()    .toDouble()``` |


## Syntax

#### Javascript
```
newImage = oldImage.uint8() etc.
```

- *newImage* is the new image.
- *oldImage* is the specified image.


## Example

#### Javascript
```javascript
var oldImage = ee.Image(1);
var newImage = oldImage.uint8();
print(oldImage, newImage);
```
