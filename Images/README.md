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
- With *logical* operations:
  - [image.eq](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.gt](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.lt](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.and](image.and_image.or_BooleanForNon-zeroImageValues.md)  
  - [image.neq](RelationshipsBetweenValuesOfTwoImages.md)
  - [image.gte](RelationshipsBetweenValuesOfTwoImages.md)  
  - [image.lte](RelationshipsBetweenValuesOfTwoImages.md)  
  - [image.or](image.and_image.or_BooleanForNon-zeroImageValues.md)  
  - [image.not](image.not.md) 
- With *mathematical* operations:
  - [image.abs](TransformingImagesWithMathematicalOperations1.md)  <-- Incomplete from here onwards
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
- With *trigonometric* operations:
  - [image.sin](TransformingImagesWithTrigonometricOperations.md)
  - [image.cos](TransformingImagesWithTrigonometricOperations.md)
  - [image.tan](TransformingImagesWithTrigonometricOperations.md)
  - [image.sinh](TransformingImagesWithTrigonometricOperations.md)
  - [image.cosh](TransformingImagesWithTrigonometricOperations.md)
  - [image.tanh](TransformingImagesWithTrigonometricOperations.md)
  - [image.acos](TransformingImagesWithTrigonometricOperations.md)
  - [image.asin](TransformingImagesWithTrigonometricOperations.md)
  - [image.atan](TransformingImagesWithTrigonometricOperations.md)
  - [image.atan2](TransformingImagesWithTrigonometricOperations.md)
- With *bitwise* operations: 
  - [image.bitwiseAnd](TransformingImagesWithArrayOperations.md)
  - [image.bitwiseOr](TransformingImagesWithBitwiseOperations.md)
  - [image.bitwise_xor](TransformingImagesWithBitwiseOperations.md)
  - [image.bitwiseNot](TransformingImagesWithBitwiseOperations.md)
  - [image.bitwise_and](TransformingImagesWithBitwiseOperations.md)
  - [image.bitwise_or](TransformingImagesWithBitwiseOperations.md)
  - [image.bitwise_Xor](TransformingImagesWithBitwiseOperations.md)
  - [image.bitwise_not](TransformingImagesWithBitwiseOperations.md)  
- With pixel *reducers*:
  - [image.reduce](TransformingImagesWithMathematicalOperations1.md)
- With *array* operations:
  - [image.arrayAccum](TransformingImagesWithArrayOperations.md)
  - [image.arrayFlatten](TransformingImagesWithArrayOperations.md)
  - [image.arrayGet](TransformingImagesWithArrayOperations.md)
  - [image.arrayLengths](TransformingImagesWithArrayOperations.md)
  - [image.arrayMask](TransformingImagesWithArrayOperations.md)
  - [image.arrayProject](TransformingImagesWithArrayOperations.md)
  - [image.arrayReduce](TransformingImagesWithArrayOperations.md)
  - [image.arrayRepeat](TransformingImagesWithArrayOperations.md)
  - [image.arraySlice](TransformingImagesWithArrayOperations.md)
  - [image.arraySort](TransformingImagesWithArrayOperations.md)
  - [image.arrayTranspose](TransformingImagesWithArrayOperations.md)
- With *insularity* operations:
  - [image.connectedComponents](image.connectedComponents.md)
  - [image.connectedPixelCount](image.connectedPixelCount.md)
- With *terrain* operations:
  - [image.derivative](image.derivative.md)
  - [ee.Terrain.products](ee.Terrain.products.md)
  - [ee.Algorithm.Terrain](ee.Terrain.products.md)
  - [ee.Terrain.slope](ee.Terrain.slope.md)
  - [ee.Terrain.aspect](ee.Terrain.aspect.md)
  - [ee.Terrain.fillMinima](ee.Terrain.fillMinima.md)
  - [ee.Terrain.hillshade](ee.Terrain.hillshade.md)
  - [ee.Terrain.hillshadow](ee.Terrain.hillshadow.md)
  - [ee.Algorithm.Hillshadow](ee.Terrain.hillshadow.md)
- With *texture* operations:
  - [image.entropy](image.entropy.md)
  - [image.glcmTexture](image.glcmTexture.md)
- With *edge* operations:
  - [image.zeroCrossing](image.zeroCrossing.md)
  - [ee.Algorithms.CannyEdgeDetector](ee.Algorithms.CannyEdgeDetector.md)
  - [ee.Algorithms.HoughTransform](ee.Algorithms.HoughTransform.md)
- With *distance* operations:
  - [image.distance](image.distance.md)
  - [featureCollection.distance](featureCollection.distance.md)
- With *neighborhood* operations:
  - [image.focal_max](focalOperations.md)
  - [image.focal_min](focalOperations.md)
  - [image.focal_median](focalOperations.md)
  - [image.focal_mode](focalOperations.md)
  - [image.convolve](image.convolve.md)
  - [image.reduceNeighborhood](image.reduceNeighborhood.md)
- With *alignment* operations:
  - [ee.Algorithms.CrossCorrelation](ee.Algorithms.CrossCorrelation.md)

#### Reproducing Images
- As *FeatureCollections*:
  - [reduceToVectors](reduceToVectors.md)
- As *ImageCollections*:
  - [ee.ImageCollection](ee.ImageCollection.md)
  - [ee.ImageCollection.fromImages](ee.ImageCollection.fromImages.md)
- As GoogleMap *Overlays*:
  - [image.getMap](image.getMap.md)
- As *images of bands for neighbors*:
  - [image.neighborhoodToBands](image.neighborhoodToBands.md)
- As *images of arrays for bands*:
  - [image.toArray](image.toArray.md)
- As *images of bands for arrays*:
  - [image.arrayFlatten](image.arrayFlatten.md)

#### Summarizing Images
- By *region*:
  - [image.reduceRegion](image.reduceRegion.md)
  - [image.sampleRegion](image.sampleRegion.md)

#### Comparing Images
- [ee.Algorithms.IsEqual(image)](ee.Algorithms.IsEqual(image).md)

#### Documenting Images
- [image.getInfo](image.getInfo.md)
- [ee.Algorithms.Describe(image)](ee.Algorithms.Describe(imageCollection).md)
- [image.toString](image.toString.md)
- [image.serialize](image.serialize.md)

#### Presenting Images
- In print:
  - [print(image)](print(image).md)
  - [alert(image)](alert(image).md)
  - [console.log(image)](console.log(image).md)
  - [confirm(image)](confirm(image).md)
- In maps:
  - [Map.addLayer(image)](Map.addLayer(image).md)
- In charts:
  - [Chart.image.histogram](Chart.image.histogram.md)
  - [Chart.image.byRegion](Chart.image.byRegion.md)
  - [Chart.image.regions](Chart.image.regions.md)

#### Exporting Images
- [Export.image](Export.image.md)
- [image.getDownloadURL](image.getDownloadURL.md)
- [ee.data.getDownloadID](ee.data.getDownloadID.md)
- [ee.data.getDownloadURL](ee.data.getDownloadURL.md)
