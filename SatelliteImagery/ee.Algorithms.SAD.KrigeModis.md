# ee.Algorithms.SAD.KrigeModis.md
- creates a new image by replicating a specified MODIS image at a finer resolution (from 500 to 250 meters) by using covaiance parameters drawn from a specified feature collection.

## Syntax

#### Javascript
```
newImage = ee.Algorithms.SAD.KrigeModis( oldImage, parameters ) 
```

- *newImage* is the new image.
- *oldImage* is the specified MODIS image. 
- *parameters* is The specified feature collection, given as a geometry with the following columns:
  - Band 	(number, 3/4/6/7), 
  - Model 	(string, gaussian/spherical/exponential), 
  - Sill 	(number), 
  - Range 	(number). 
For each tile, the first row with an intersecting geometry will be used for each band. 
 

Argument names used in documentation:
```

```

## Example

#### Javascript


```
