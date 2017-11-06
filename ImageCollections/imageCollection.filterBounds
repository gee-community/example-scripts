# imageCollection.filterBounds
- creates new image collection that contains only those images from a specified image collection.

## Syntax

#### Javascript
```
newImageCollection = oldImageCollection.filterBounds(geometry )
```

- *newImageCollection* is the new image collection.
- *oldImageCollection* is the specified image collection.
- *geometry* is the specified geometry.

## Example

#### Javascript
```javascript

var OldIMAGES        = ee.ImageCollection('LANDSAT/LE7').filterDate('2000-04-01','2000-04-15');
var AllStateFEATURES = ee.FeatureCollection( 'ft:1fRY18cjsHzDgGiJiS2nnpUU3v9JPDc2HNaR7Xk8' );
var OneStateFEATURE  = AllStateFEATURES.filter( ee.Filter.eq('Name','Florida') );
var FilteredIMAGES   = OldIMAGES.filterBounds( OneStateFEATURE );
Map.centerObject( OneStateFEATURE, 6);
Map.addLayer( OneStateFEATURE, {color: '000000'},                         'Bounding Feature' );
Map.addLayer( FilteredIMAGES,  {bands: ['B3','B2','B1'], min:0, max:255 }, 'Bounded Images '  );

```
