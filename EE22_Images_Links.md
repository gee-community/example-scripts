An image is is an EE variable object that represents a cartographic depiction of geographic space in a format much like that of a digital photograph.  Images can be processed by using operations of the types listed below, which vary according to the nature of that processing.  Each operation name is linked to a separate page describing that operation.	

|Category         |Method         |
|-----------------|-------------------|
|UPLOADING IMAGES |		`Asset Manager` |
|ACCESSING IMAGES	|	[ee.Image](ee.Image.md) [ee.Image.load](ee.Image.load.md)|
|CREATING IMAGES	|		`ee.Image(value)`		`ee.Image.constant` 	`ee.Image.pixelLonLat`	`ee.Image.pixelArea` |		

|EDITING IMAGES|  |
|--------------|--|
|BY MASKING REGIONS		|	[image.mask](image.mask.md) |
|BY CLIPPING REGIONS	|	[image.clip](image.clip.md|
|BY SELECTING BANDS		|	`image.select` 			`image.slice`|
|BY COMBINING BANDS		|	`image.addBands`|
|BY REPROJECTING			|	`image.reproject`|
|BY RECODING COLORS	|		`image.rgbtohsv`		`image.hsvtorgb`|
|BY RECASTING DATA TYPES		|	`image.uint8`		`image.Uint8`			`image.uint16`			`image.Uint16` `image.uint32`			`image.Uint32`		`image.int8`		`image.toInt8`			`image.byte`			`image.toByte`	`image.int16`			`image.toInt16`	`image.short`			`image.toShort` `image.int32`			`image.toInt32`		`image.int`			`image.toInt`	`image.int64`			`image.toInt64`		`image.long`			`image.toLong`	`image.float`			`image.toFloat` 		`image.double`		`image.toDouble`	`image.cast`|
|BY RESETTING VALUES		|	`image.set`			`image.setMulti`		`image.remap`			`image.where` `image.metadata`		`image.clamp`			`image.unitScale`		`image.interpolate`|
	  			            

|TRANSFORMING IMAGES| |
|WITH LOGICAL OPERATIONS	|	image.eq			image.gt			image.lt			image.and			image.neq			image.gte			array.lte			image.or 		image.not		|
|WITH MATHEMATICAL OPERATIONS	|	image.abs			image.ceil			image.log			image.floor		image.round			image.exp 		image.sqrt			image.log10	image.add			image.subtract		image.multiply		image.divide		image.max			image.min			image.mod			image.pow			image.hypot			image.first			image.first_nonzero		image.polynomial		image.expression
|WITH TRIGONOMETRIC OPERATIONS |	image.sin			image.cos			image.tan			
image.sinh			image.cosh			image.tanh	
image.acos			image.asin			image.atan			image.atan2
WITH BITWISE OPERATIONS			image.bitwiseAnd		image.bitwiseOr		image.bitwise_xor		image.bitwiseNot	
image.bitwise_and		image.bitwise_or		image.bitwiseXor		image.bitwise_not 
image.leftShift		image.left_shift		image.rightShift		image.right_shift
WITH PIXEL REDUCERS			image.reduce      
WITH ARRAY OPERATIONS			image.arrayAccum    	image.arrayFlatten    	image.arrayGet        		image.arrayLengths 	
image.arrayMask 		image.arrayProject 		image.arrayReduce. 	image.arrayRepeat 		
image.arraySlice     		image.arraySort 		image.arrayTranspose
WITH INSULARITY OPERATIONS		image.connectedCom…	image.connectedPixelCount
WITH TERRAIN OPERATIONS			image.derivative		ee.Terrain.products		ee.Algorithm.Terrain	
ee.Terrain.slope		ee.Terrain.aspect		ee.Terrain.fillMinima	
ee.Terrain.hillshade		ee.Terrain.hillshadow	ee.Algorithm.Hillshadow
WITH TEXTURE OPERATIONS			image.entropy		image.glcmTexture
WITH EDGE OPERATIONS			image.zeroCrossing		ee.Algorithms.Canny…	ee.Algorithms.HoughTransform
WITH DISTANCE OPERATIONS		image.distance		featureCollection.distance
WITH NEIGHBORHOOD OPERATIONS		image.focal_max		image.focal_min		image.focal_median	image.focal_mode		image.convolve		image.reduceNeighborhood
WITH ALIGNMENT OPERATIONS		ee.Algorithms.CrossCorr…

PROCESSING IMAGE VARIABLES				  			            



REPRODUCING IMAGES
AS FEATURE COLLECTIONS			reduceToVectors 		
AS IMAGE COLLECTIONS			ee.ImageCollection		ee.ImageCollection.fromImages
AS GOOGLEMAP OVERLAYS			image.getMap
AS IMAGES OF BANDS FOR NEIGHBORS	image.neighborhoodToBands
AS IMAGES OF ARRAYS FOR BANDS		image.toArray	
AS IMAGES OF BANDS FOR ARRAYS		image.arrayFlatten

SUMMARIZING IMAGES
BY REGION				image.reduceRegion	image.sampleRegion	THIS MUST BE ADDED FOR IMAGE CLASSIFICATION

COMPARING IMAGES		ee.Algorithms.IsEqual(image)

DOCUMENTING IMAGES		ee.Algorithms.Describe 	image.getInfo	
	image.toString		image.serialize		

PRESENTING IMAGES														 
IN PRINT					print(image)			console.log(image)	
	alert(image)			confirm(image)
IN MAPS					Map.addLayer(image)	image.Visualize		image.sldStyle
IN CHARTS				Chart.image.histogram	Chart.image.byRegion	Chart.image.regions

EXPORTING IMAGES			Export.image 		image.getDownloadURL	
ee.data.getDownloadId	ee.data.getDownloadURL	

