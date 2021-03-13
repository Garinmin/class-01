# Images, Color, Text

## Images

To add an image into the page you need to use **img** element:
```
   <img src="images/bear.jmg" alt="Bear" width=400px heihgt=600px />
```
Where an image is placed in the code will affect how it is displayed. 

### Aligning images horizontally
```
   <p><img src=URL alt="name" align="left"/> (maybe "right")
```
### Aligning images vertically
``` 
   <p><img ... align="top" /> (middle, bottom)
```
Image formaqts:

- jpeg
- gif - animated
- png
- svg - vector

### HTML5: figure and figure caption
```
<figure>
   <img src ... />
   <br />
   <figcaption>TEXT</figcaption>
</figure>
```

### Color

- color
- background-color

### Opacity

- opacity: 0.5;
- or background-color: rgba (0,0,0,0.5); - where 0.5 - opocity

## Text

- specifying typefaces: font-family
- sixe of type: font-size
- bold:font-weight
- italic: font-style
- underline and strike: text-decoration
- leading: line-height
- alignment: text-align
- vertical alignment: vertical-align
- identing text: text-indent
- drop shadow: text-shadow

## JPEG vs PNG vs GIF — which image format to use and when? [blog.imagekit](https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d)

Use JPEG format for all images that contain a natural scene or photograph where variation in colour and intensity is smooth. Use PNG format for any image that needs transparency or for images with text & objects with sharp contrast edges like logos. Use GIF format for images that contain animations.

### Colours

- JPEG images can support around 16 million colours. This is what makes them suitable for storing images of natural scenes.
- PNG images mainly have two modes — PNG8 and PNG24. PNG8 can support upto 256 colours whereas PNG24 can handle upto 16 million colours like a JPEG image.
- GIF images are limited to 256 colours.

### Animation

Of these 3 formats, only GIF supports animation.

