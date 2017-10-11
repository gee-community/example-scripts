# image.cast
- Creates a new image of specified band-by-band types by replicating a specified image of any type.

## Syntax

#### Javascript
```
newImage = oldImage.cast( bandTypes, bandOrder )
```

- *newImage* is the new image.
- *oldImage* is the specified image.
- *bandTypes* are the specified types, given as a dictionary of band names and corresponding types.  Types can be specified as PixelType objects or as any of the following strings:  'int8', 'int16', 'int32', 'int64', 'uint8', 'uint16', 'uint32', 'byte', 'short', 'int', 'long', 'float', or 'double.'
- Optional: *bandOrder* is a list of (all) band names indicating the order in which they are to be stored.  Default: alphabetical order.

Argument names used in documentation:
```
newImage = oldImage.cast( bandTypes, bandOrder )
```

## Example

#### Javascript
```javascript
Example needed.
```
