# Images

An image is an EE variable object that represents a cartographic depiction of geographic space in a format much like that of a digital photograph.  Images can be processed by using operations of the types listed below, which vary according to the nature of that processing.  Each operation name is linked to a separate page describing that operation.	

#### Uploading Images
- Asset Manager

#### Accessing Images
- [ee.Image](ee.Image.md)
- [ee.Image.load](ee.Image.constant.md)

#### Creating Images
- [ee.Image(value)](ee.Image(value).md)
- [ee.Image.constant](ee.Image.constant.md)
- [ee.Image.pixelLonLat](ee.Image.pixelLonLat.md)
- [ee.Image.pixelArea](ee.Image.pixelArea.md)

#### Editing Images
- By *masking* regions: 
  - [image.mask](image.mask.md) 
- By *clipping* regions: 
  - [image.clip](image.clip.md) 
- By *selecting* bands: 
  - [image.select](image.select.md),  
  - [image.slice](image.slice.md) 
- By *combining* bands: 
  - [image.addBands](image.addBands.md)
- By *reprojecting*:
  - [image.reproject](image.reproject.md) 
- By *recoding colors*:
  - [image.rgbtohsv](image.rgbtohsv.md)
  - [image.hsvtorgb](image.hsvtorgb.md)
- By *recasting* data types:
  - [image.uint8](ConvertingImagePixelType.md)
  - [image.uint16](ConvertingImagePixelType.md)
  - [image.uint32](ConvertingImagePixelType.md)
  - [image.int8](ConvertingImagePixelType.md)  
  - [image.int16](ConvertingImagePixelType.md)
  - [image.int32](ConvertingImagePixelType.md)  
  - [image.int64](ConvertingImagePixelType.md)  
  - [image.float](ConvertingImagePixelType.md)  
  - [image.double](ConvertingImagePixelType.md)  
  - [image.Uint8](ConvertingImagePixelType.md)
  - [image.Uint16](ConvertingImagePixelType.md)
  - [image.Uint32](ConvertingImagePixelType.md)
  - [image.toInt8](ConvertingImagePixelType.md)  
  - [image.toInt16](ConvertingImagePixelType.md)
  - [image.toInt32](ConvertingImagePixelType.md)  
  - [image.toInt64](ConvertingImagePixelType.md)  
  - [image.toFloat](ConvertingImagePixelType.md)  
  - [image.toDouble](ConvertingImagePixelType.md)
  - [image.byte](ConvertingImagePixelType.md)
  - [image.short](ConvertingImagePixelType.md)
  - [image.int](ConvertingImagePixelType.md)
  - [image.toLong](ConvertingImagePixelType.md)   
  - [image.toByte](ConvertingImagePixelType.md)
  - [image.toShort](ConvertingImagePixelType.md)
  - [image.toInt](ConvertingImagePixelType.md)
  - [image.toLong](ConvertingImagePixelType.md) 
  - [image.cast](image.cast.md) 
- By *resetting* values:
  - [image.set](image.set.md)
  - [image.setMulti](image.setMulti.md)
  - [image.remap](image.remap.md)
  - [image.where](image.where.md)
  - [image.metadata](image.metadata.md)
  - [image.clamp](image.clamp.md)
  - [image.unitScale](image.unitScale.md)
  - [image.interpolate](image.interpolate.md)

#### Transforming Images
- With *logical* operations
  - [image.eq](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.gt](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.lt](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.and](image.and_image.or_BooleanForNon-zeroImageValues.md)  
  - [image.neq](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.gte](RelationshipsBetweenValuesOfTwoImages.md)  
  - [image.lte](RelationshipsBetweenValuesOfTwoImages.md)  
  - [image.or](image.and_image.or_BooleanForNon-zeroImageValues.md)  
  - [image.not](image.not.md) 
- With *mathematical* operations 
  - [image.abs](TransformingImagesWithMathematicalOperations1.md)
  - [image.ceil](TransformingImagesWithMathematicalOperations1.md)
  - [image.log](TransformingImagesWithMathematicalOperations1.md)
  - [image.floor](TransformingImagesWithMathematicalOperations1.md)  
  - [image.round](TransformingImagesWithMathematicalOperations1.md)
  - [image.exp](TransformingImagesWithMathematicalOperations1.md)  
  - [image.sqrt](TransformingImagesWithMathematicalOperations1.md)  
  - [image.log10](TransformingImagesWithMathematicalOperations1.md)  
  - [image.add](TransformingImagesWithMathematicalOperation2s.md)
  - [image.subtract](TransformingImagesWithMathematicalOperations2.md)
  - [image.multiply](TransformingImagesWithMathematicalOperations2.md)
  - [image.divide](TransformingImagesWithMathematicalOperations2.md)
  - [image.max](TransformingImagesWithMathematicalOperations2.md)   
  - [image.min](TransformingImagesWithMathematicalOperations2.md)
  - [image.mod](TransformingImagesWithMathematicalOperations2.md)
  - [image.pow](TransformingImagesWithMathematicalOperations2.md)
  - [image.hypot](TransformingImagesWithMathematicalOperations2.md) 
  - [image.first](TransformingImagesWithMathematicalOperations2.md) 
  - [image.first_nonzero](TransformingImagesWithMathematicalOperations2.md) 

