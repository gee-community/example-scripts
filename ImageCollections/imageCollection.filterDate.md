# ee.imageCollection.filterDate 
- Creates a new image collection that contains only those images from the specified collection 
that are associated with the time period between specified starting and stopping dates

## Syntax

#### Javascript
```
newImageCollection = oldImageCollection.filterDate ( startingDate, stoppingDate )

```

- *newImage* is the new image.
- *old image* is the specified image collection.
- *startingDate* is the specified starting date, given either as a string in 'month#/day#/year#' 
  (or 'month#-day#-year#') format or the number of milliseconds since January 1, 1970
- *stoppindDate* is the specified stopping date, given either as a string in 'month#/day#/year#' 
  (or 'month#-day#-year#') format or the number of milliseconds since January 30, 1970




## Example

#### Javascript
```javascript
var FilteredIMAGES = ee.ImageCollection( 'LC8_L1T_TOA' ).filterDate( '2014-10-03','2014-10-5' );	 
Map.setCenter( -96.15, 44.15, 4);                                                         
Map.addLayer( FilteredIMAGES, {bands:'B4,B3,B2', min:0, max:0.2}, 'Filtered Images' ); 

```
