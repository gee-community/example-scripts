# ee.Algorithms.Landsat.pathRowLimit.md
- creates a new image collection by replicating a specified Landsat image collection after limiting it to only the best of a specified number of scenes. 

## Syntax

#### Javascript
```
newImageCollection = ee.Algorithms.Landsat.pathRowLimit( oldImageCollection, pathLimit, totalLimit )
```

- *newImageCollection* is the new image collection.
- *ee.Algorithms.Landsat.pathRowLimit* is the specified Landsat image collection. 
- *oldImageCollection* is the specified classifier. 
- *pathLimit* is the maximum number of scenes scenes per path. Default: 25.
- *totalLimit* is the maximum number of scenes scenes in total. Default: 100
 
Argument names used in documentation:
```
newImage = oldImage.classify( classifier, outputName )
```

## Example

#### Javascript
```

```
