# ImageCollections

An ImageCollection is is an EE variable object that represents a set of images that usually all depict spatial variation the same geographical characteristic but do so: 
  - for the same place at different times,
  - for different places at the same time; or
  - for different places at different times.
ImageCollections can be processed by using operations of the types listed below, which vary according to the nature of that processing.  Each operation name is linked to a separate page describing that operation.

#### Creating ImageCollections
- [ee.ImageCollection.fromImages](ee.ImageCollection.fromImages.md) <-- Incomplete

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

#### Transforming ImageCollections
- By *mosaicking*:
  - [imageCollection.mosaic](imageCollection.mosaic.md)
- with *logical* operations
  - [imageCollection.and](image.and_image.or_BooleanForNon-zeroImageValues.md)  
  - [imageCollection.or](image.and_image.or_BooleanForNon-zeroImageValues.md)  
- With *mathematical* operations:
  - [imageCollection.sum](imageCollection.sum.md)   
  - [imageCollection.product](imageCollection.product.md)
  - [imageCollection.max](imageCollection.max.md) 
  - [imageCollection.min](imageCollection.min.md) 
  - [imageCollection.mean](imageCollection.mean.md)
  - [imageCollection.mode](imageCollection.mode.md) 
  - [imageCollection.median](imageCollection.median.md)
  - [imageCollection.count](imageCollection.count.md) 
  - [imageCollection.formaTrend](imageCollection.formaTrend.md)
- With *reducers*:
  - [imageCollection.reduce](imageCollection.reduce.md)
  
#### Reproducing ImageCollections
- As lists of *pixel data*:
  - [imageCollection.getRegion](imageCollection.getRegion.md)
- As lists of *images*:
  - [imageCollection.first](imageCollection.first.md)  
  - [imageCollection.toList](imageCollection.toList.md)  
- As GoogleMap *overlays*:
  - [imageCollection.getMap](imageCollection.getMap.md)
- As images of *arrays*:
  - [imageCollection.toArray](imageCollection.toArray.md)   
  - [imageCollection.toArrayPerBand](imageCollection.toArrayPerBand.md) 
  
#### Comparing ImageCollections
- [ee.Algorithms.IsEqual(imageCollection)](ee.Algorithms.IsEqual(imageCollection).md)

#### Parallel Processing ImageCollections
- [imageCollection.Map](imageCollection.Map.md)

#### Documenting ImageCollections
- [imageCollection.getInfo](imageCollection.getInfo.md)
- [ee.Algorithms.Describe(imageCollection)](ee.Algorithms.Describe(imageCollection).md)
- [imageCollection.toString](imageCollection.toString.md)
- [imageCollection.serialize](imageCollection.serialize.md)
- [ee.data.getList](ee.data.getList.md)

#### Presenting ImageCollections
- In print:
  - [print(imageCollection)](print(imageCollection).md)
  - [alert(imageCollection)](alert(imageCollection).md)
  - [console.log(imageCollection)](console.log(imageCollection).md)
  - [confirm(imageCollection)](confirm(imageCollection).md)
- In maps:
  - [Map.addLayer(imageCollection)](Map.addLayer(imageCollection).md)
- In charts:
  - [Chart.image.series](Chart.image.series.md)
  - [Chart.image.seriesByRegion](Chart.image.seriesByRegion.md)
  - [Chart.image.doySeries](Chart.image.doySeries.md)
  - [Chart.image.doySeriesByRegion](Chart.image.doySeriesByRegion.md)
  - [Chart.image.doySeriesByYear](Chart.image.doySeriesByYear.md)
