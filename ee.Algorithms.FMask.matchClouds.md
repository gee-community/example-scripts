# ee.Algorithms.FMask.matchClouds
- Creates a new image with a single band called 'csm' that depicts cloud and shadow masks as computed by applying the *Fmask* algorithm to a specified image using other specified images that depict potential clouds, potential shadows, and brightness temperature; as well as coefficients indicating the upper and lower extents of brightness temperature. 

## Syntax

#### Javascript
```
newImage = ee.Algorithms.Fmask.matchClouds ( oldImage, cloudImage, shadowImage, brightnessImage, howDark, howBright, tilePadding )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *cloudImage* is the specified image of potential clouds, on which cloudy pixels are set to 1 and non-cloudy pixels are masked.
- *shadowImage* is the specified image of potential shadows, on which cloudy pixels are set to 1 and non-cloudy pixels are masked.  
- *brightnessImage* is the specified image of brightness temperatures, given in degrees Celsius. 
- *howDark* is the specified lower limit (17.5 percentile) on brightness temperature. 
- *howBright* is the specified upper limit (82.5 percentile) on brightness temperature. 
- Optional: *tilePadding* is the amount by which tiles should be padded, given in pixel widths. Default: 50. 

Argument names used in documentation:
```
newImage = ee.Algorithms.FMask.matchClouds(input, cloud, shadow, btemp, sceneLow, sceneHigh, neighborhood)
```

## Example

#### Javascript
```javascript
Example needed.
```
