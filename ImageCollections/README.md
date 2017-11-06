# ImageCollections

An ImageCollection is is an EE variable object that represents a set of images that usually all depict spatial variation the same geographical characteristic but do so: 
	- for the same place at different times,
  - for different places at the same time; or
  - for different places at different times.
ImageCollections can be processed by using operations of the types listed below, which vary according to the nature of that processing.  Each operation name is linked to a separate page describing that operation.

#### Accessing ImageCollections
- [ee.ImageCollection](ee.ImageCollection.md)
- [ee.ImageCollection.load](ee.ImageCollection.load.md)

#### Editing ImageCollections
- By *limiting* images:
  - [imageCollection.limit](imageCollection.limit.md) 
- By *filtering* images: 
  - [imageCollection.filterMetadata](imageCollection.filterMetadata.md)  <-- Incomplete
  - [imageCollection.filterBounds](imageCollection.filterBounds.md) 
  - [imageCollection.filterDate](imageCollection.filterDate.md) 
  - [imageCollection.filter](imageCollection.filter.md)  <-- Incomplete from here onwards
- By *selecting* bands: 
  - [imageCollection.select](imageCollection.select.md),  
  - [imageCollection.distinct](imageCollection.distinct.md) 
- By *combining* bands: 
  - [imageCollection.combine](imageCollection.combine.md)
- By *recasting* data types:
  - [imageCollection.uint8](ConvertingImageCollectionPixelType.md)
  - [imageCollection.uint16](ConvertingImageCollectionPixelType.md)
  - [imageCollection.uint32](ConvertingImageCollectionPixelType.md)
  - [imageCollection.int8](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.int16](ConvertingImageCollectionPixelType.md)
  - [imageCollection.int32](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.int64](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.float](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.double](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.Uint8](ConvertingImageCollectionPixelType.md)
  - [imageCollection.Uint16](ConvertingImageCollectionPixelType.md)
  - [imageCollection.Uint32](ConvertingImageCollectionPixelType.md)
  - [imageCollection.toInt8](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.toInt16](ConvertingImageCollectionPixelType.md)
  - [imageCollection.toInt32](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.toInt64](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.toFloat](ConvertingImageCollectionPixelType.md)  
  - [imageCollection.toDouble](ConvertingImageCollectionPixelType.md)
  - [imageCollection.byte](ConvertingImagePixelType.md)
  - [imageCollection.short](ConvertingImagePixelType.md)
  - [imageCollection.int](ConvertingImagePixelType.md)
  - [imageCollection.toLong](ConvertingImagePixelType.md)   
  - [imageCollection.toByte](ConvertingImagePixelType.md)
  - [imageCollection.toShort](ConvertingImagePixelType.md)
  - [imageCollection.toInt](ConvertingImagePixelType.md)
  - [imageCollection.toLong](ConvertingImagePixelType.md) 
  - [imageCollection.cast](imageCollection.cast.md) 
- By resetting values:
  - [imageCollection.set](imageCollection.set.md)
  - [imageCollection.setMulti](imageCollection.setMulti.md)

#### Transforming Images
- By *mosaicking*:
  - [imageCollection.mosaic](imageCollection.mosaic.md)
- with logical operations
  - [image.and](image.and_image.or_BooleanForNon-zeroImageValues.md)  
  - [image.or](image.and_image.or_BooleanForNon-zeroImageValues.md)  
<!--- 
- With mathematical operations <--- stopped here 
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
---!>
