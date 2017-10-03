#ee.Image

##Syntax
'''
newImage = ee.Image('assetID')
'''

assetID is the specified asset ID, given as a string.

##Example
'''javascript
var NewIMAGE = ee.Image( 'CGIAR/SRTM90_V4' );
Map.setCenter( -98, 39, 4 );
Map.addLayer( NewIMAGE, {min:0, max: 2500} );
'''
