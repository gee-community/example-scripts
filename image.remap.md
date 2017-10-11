# image.remap
- Creates a new image on which each pixel’s value is explicitly assigned according to its value on a specified band on a specified image.

## Syntax

#### Javascript
```
newImage = oldImage.remap( listOfOldValues, listOfNewValues, defaultNewValue, bandName )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *listOfOldValues* a list of values from the specified image for which new values are to be assigned.
- *defaultNewValue* a list of new values to be assigned according to those at corresponding ordinal positions in listOfOldValues.
- *bandName* is the name of the specified band, given as a string.

## Example

#### Javascript
```javascript
var OldIMAGE        = ee.Image('MCD12Q1/MCD12Q1_005_2001_01_01').select('Land_Cover_Type_1');
var NewIMAGE        = OldIMAGE.remap( [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17],
                                      [0,1,1,1,1,1,2,2,2,3, 3, 4, 5, 6, 5, 7, 8, 9], 0, 'Land_Cover_Type_1' );
print( 'Original Image', OldIMAGE );
print( 'Remapped Image', NewIMAGE );
var ColorsForMODIS  = ['aec3d4', // 00 = Water                        */ 'd9903d', // 09 = Savanna
                       '152106', // 01 = Evergreen Needleleaf Forest  */ '91af40', // 10 = Grassland
                       '225129', // 02 = Evergreen Broadleaf Forest   */ '111149', // 11 = Permanent Wetland
                       '369b47', // 03 = Deciduous Needleleaf Forest  */ 'cdb33b', // 12 = Cropland
                       '30eb5b', // 04 = Deciduous Broadleaf Forest   */ 'cc0013', // 13 = Urban
                       '387242', // 05 = Mixed Deciduous Forest       */ '33280d', // 14 = Crops & Natural Vegetation
                       '6a2325', // 06 = Closed Shrubland             */ 'd7cdcc', // 15 = Permanent Snow & Ice
                       'c3aa69', // 07 = Open Shrubland               */ 'f7e084', // 16 = Barren / Desert
                       'b76031', // 08 = Woody Savanna                */ '6f6f6f'  // 17 = Unclassified
                      ].join(',');     
var DisplaySETTINGS = { min:0, max:17, opacity:0.7, palette:ColorsForMODIS };
Map.setCenter(17.3172, 59.5275, 9 );
Map.addLayer( OldIMAGE, DisplaySETTINGS, 'Land Cover Classes' );
Map.addLayer( NewIMAGE, { min:0, max:9, palette:['000066', // 00 = Water     */ '00ff00',  // 05 = Cropland
                                                 '008800', // 01 = Forest    */ 'ff0000', // 06 = Urban


                                                 '444400', // 02 = Shrubland */ 'ffffff', // 07 = Snow & Ice
                                                 'aaaa00', // 03 = Savanna   */ 'ffff00', // 08 = Desert
                                                 '00dddd', // 04 = Wetland   */ '000000'  // 09 = Unclassified
                                                 ] },'Land Cover Groups' );
```
