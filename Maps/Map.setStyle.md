# Map.setStyle
- sets the current map’s background to user-specified settings

## Syntax

#### Javascript
```
Map.setStyle (  styleName, dictionaryOfStyles  )
```

- *styleName* is one of the keys in dictionaryOfStyles 
- *dictionaryOfStyles* is the name of a user-created dictionary of styles as described [here](https://developers.google.com/maps/documentation/javascript/reference#MapTypeStyle)

## Examples

#### Javascript
```javascript
Map.setCenter( -77.00919270515442, 38.88981361419182, 15 );
Map.setStyle( 'NewTYPE', 
             {'NewTYPE':[ { featureType:'all',           stylers:[{saturation:-100}]                  },
                          { featureType:'road.arterial', stylers:[{saturation: 100}, {hue:'#ff0000'}] },  ]  }  );
```
