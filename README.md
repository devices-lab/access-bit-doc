# Documentation for the Access:Bit

Must be built with `npm` rather than `yarn` as yarn doesn't play nicely with the package dependencies, unfortunately.

## Image autocropping

Consider using the `mogrify` tool in ImageMagick to autocrop images to a consistent border:

`magick mogrify -trim -bordercolor white -strip -border 20 *.png` 

```
magick mogrify \
    -trim \
    -bordercolor white \
    -strip \
    -depth 8 \
    -alpha on \
    -define png:compression-level=9 \
    -define png:compression-strategy=1 \
    -define png:compression-filter=5 \
    -border 20 \
    -resize 1200x\> \
    *.png
```