#geometry.union  ,  .intersection , .symmetricDifference ,   and  Difference
- create a new polygonal geomety encompassing locations that are determined by two specified polygonal geometries such that
-	union calls for locations included in either or both 	of the specified geometries;
-	intersection calls for locations included	both 	of the specified geometries;
-	symmetricDifference calls for locations included in either but not both of the specified geometries; and
-	Difference calls for locations included in	the 1st but not the 2nd	of the specified geometries;


## Syntax

#### Javascript
```
newGeometry = 1stOldGeometry.union ( 2ndOldGeometry, errorMargin, coordinateSystem )
              or  .intersection
              or  .symmetricDifference
              or  .Difference

```
- *newGeometry* is the new geometry.
- *1stOldGeometry* is the first specified geometry.
- *2ndOldGeometry* is the second specified geometry.
- *errorMargin* = an ErrorMargin indicating the maximum allowable placement error in meters.  
- *coordinateSystem* = aspecified coordinate system, given as an EPSG code ( as described [here](http://spatialreference.org/) ) or as a WKT string ( as described [here](http://en.wikibooks.org/wiki/Geospatial_Data_in_SQL_Server/WKT) ).  Default:  'EPSG4326' (WGS84) 

## Example

#### Javascript
```javascript

var AllStateCOLLECTION          = ee.FeatureCollection('ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8');
var OneStateCOLLECTION          = AllStateCOLLECTION.filter( ee.Filter.eq('Name', 'Arkansas') );
var OneStateELEMENT             = OneStateCOLLECTION.first( );   var OneStateFEATURE  = ee.Feature( OneStateELEMENT );
var OneStateGEOMETRY            = OneStateFEATURE.geometry(); 
var AllRegionCOLLECTION         = ee.FeatureCollection('ft:1Ec8IWsP8asxN-ywSqgXWMuBaxI6pPaeh6hC64lA');
var OneRegionCOLLECTION         = AllRegionCOLLECTION.filter(ee.Filter().eq('ECO_NAME', 'Ozark Mountain forests'));
var OneRegionELEMENT            = OneRegionCOLLECTION.first( );  var OneRegionFEATURE = ee.Feature( OneRegionELEMENT );
var OneRegionGEOMETRY           = OneRegionFEATURE.geometry( );
var UnionGEOMETRY               = OneStateGEOMETRY.union( OneRegionGEOMETRY );
var IntersectionGEOMETRY        = OneStateGEOMETRY.intersection( OneRegionGEOMETRY );
var SymmetricDifferenceGEOMETRY = OneStateGEOMETRY.symmetricDifference( OneRegionGEOMETRY );
var DifferenceGEOMETRY          = OneStateGEOMETRY.difference( OneRegionGEOMETRY );
Map.centerObject( OneStateGEOMETRY, 6 );	
Map.addLayer( OneStateGEOMETRY,            {color:'ffff00'}, 'State'                );  
Map.addLayer( OneRegionGEOMETRY,           {color:'00ffff'}, 'Region'               );
Map.addLayer( UnionGEOMETRY,               {color:'ff0000'}, 'Union'                );  
Map.addLayer( IntersectionGEOMETRY,        {color:'00ff00'}, 'Intersection'         );
Map.addLayer( SymmetricDifferenceGEOMETRY, {color:'0000ff'}, 'Symmetric Difference' );
Map.addLayer( DifferenceGEOMETRY,          {color:'000000'}, 'Difference'           );

```
