# Table of Contents
* [Multimedia](#multimedia)
  * [What is multimedia?](#what-is-multimedia)
  * [Multimedia Application](#multimedia-application)
    * [Communication information](#communication-information)
    * [Pros and Cons of multimedia](#pros-and-cons-of-multimedia)
    * [Multimedia Presentation](#multimedia-presentation)
  * [Colour](#colour)
    * [Additive Colour Matching](#additive-colour-matching)
    * [Colours Models](#colours-models)
    * [Flat Screen Monitors](#flat-screen-monitors)
    * [Screen Corrections](#screen-corrections)
  * [Graphics](#graphics)
    * [Logical vs Physical Representation](#logical-vs-physical-representation)
      * [Scaling bitmaps](#scaling-bitmaps)
      * [Rendering](#rendering)
      * [Fonts](#fonts)
        * [Font Anatomy](#font-anatomy)
      * [Type of Fonts](#type-of-fonts)
      * [Bitmap Image Manipulation](#bitmap-image-manipulation)
  * [Data Compression](#data-compression)
    * [Why use Data Compression?](#why-use-data-compression)
    * [Types of Compression](#types-of-compression)
      * [Compression Algorithms](#compression-algorithms)
        * [Pixel Packing](#pixel-packing)
        * [RLE](#rle)
        * [Dictionary Based Methods](#dictionary-based-methods)
        * [JPEG compression](#jpeg-compression)
  * [File Formats](#file-formats)
  * [Animation](#animation)
  * [Sound](#sound)
* [Human Computer Interaction](#human-computer-interaction)
  * [Design](#design)
  * [Web Design](#web-design)
  * [Multimedia Design](#multimedia-design)
  * [Usability Testing](#usability-testing)
  * [Interaction Styles](#interaction-styles)
  * [Human Factors](#human-factors)
  * [Interaction Devices](#interaction-devices)
  * [Software Development](#software-development)

# Multimedia
## What is multimedia?
Multimedia is useful for **education**, **information** and **entertainment**.

> “Multimedia is the seamless integration of
> text, sound, images of all kinds and control
> software within a single digital information
> environment.”
>
> ─ Tony Feldman

## Multimedia Application
### Communication information
- **Modalities** ─ Related human sense.
- **Channels of communication** ─ Single-modality type of communication, e.g. speech.
- **Medium** ─ Object that uses one or more channels, e.g. audio clip, picture, animation.

### Pros and Cons of multimedia
**Pros**
- Grabs attention
- Multiple channels for the same message
- Combined media can enhance message
- Interactivity


**Cons**
- Poor design
- Accessibility problems
- Lack of suitable device

### Multimedia Presentation
- **Card Based** ─ Based on 2D pages, similar to books or magazines. E.g. PDF, HTML, PPT.
- **Event Based** ─ System driven by the user events. E.g. GUIs.
- **Time Based** ─ Things are arranged on a timeline. E.g. Flash.

More often that not, an application use **all three forms** of presentations combined.

## Colour

### Additive Colour Matching
Mixing different amounts and wavelengths of light together to produce all colours.

### Colours Models
- Additive
  - **RGB** ─ Red Green Blue
  - **HSV** ─ Hue Saturation Value
- Subtractive
  - **CMY** ─ Cyan Magenta Yellow
  - **CMYK** ─ Cyan Magenta Yellow Black
- XYZ
  - **CIE** ─ Commission Internationale d'Eclarange ─ Device independent

### Flat Screen Monitors
- LCD
  - Liquid Crystals Display
  - Low Power
- OLED
  - Organic light-emitting diodes
  - No backlight required
  - Higher contrast

### Screen Corrections
- **Gamut** ─
- **Gamma** ─

## Graphics
### Logical vs Physical Representation
- **Physical Representation** of graphical data is how it is actually displayed on the screen.
- **Virtual Representation** of a graphical data is how it stored in a file or in a program.

Displays are only capable of displaying **bitmaps**, matrices of bits or colours.

#### Scaling bitmaps
Scaling bitmaps requires some sort of resampling to create or remove pixels.

- Upsampling ─ increase size.
- Downsampling ─ decrease size.

Possible resampling algorithms:
- Nearest neighbour
- Bilinear Interpolation
- Bicubic Interpolation

#### Rendering
Vector-based pictures have to be rendered to be converted to display-compatible bitmaps.

This raises the problem of sub-pixel values, particularly for lines and fonts.

**Antialiasing** uses an algorithm to fill pixel with a range of colours, more or less full to smooth the image.

#### Fonts
> In the beginning Men created the computers without fonts, now the screen was formless and without text styles, raster
> monospace fonts were over the surface of the deep, and the Spirit of Men was hovering over the pixels.
>
> ─ Computer Genesis 1-3

**Fonts** are ways of representing characters on the screen with different styles.

Some combination of letters might be represented by a single glyph, to look better.
Similarly, some characters may consist of one or more glyphs.


##### Font Anatomy
![Fonts Anatomy][FontAnatomy]

A font has various properties, as described in the infographic above.
The most common one, the font size, is determined by distance of the _ascender_ from the _descender_.

Kerning adjusts the space between letters, sometimes even to the point of overlapping,
to reduce the space between glyphs, to make the text more compact, contributing to a more natural look.

#### Type of Fonts
There are three main categories of fonts:

- **Raster**/**BitMap**
  ─ These were the first fonts to be created and consists in various bitmaps for each character.
    This kind of fonts did not allow clear resizing.
- **Vector**
  ─ Vector-based fonts solve the issue with resizing, because they use vector images to render the fonts,
    but antialiasing might reduce legibility due to its inability of smoothing straight lines effectively.
- **TrueType**/**OpenType**
  ─ These two types of fonts, still use vector-based images to display the shapes of the font,
    but also make use of **hints***, that explains the rendered how to properly display straight lines,
    and widely improve legibility.

#### Bitmap Image Manipulation
  - **Pixel Selection**
    - Basic Marquee Tools
      - Rectangle
      - Ellipse
      - Hand-drawn Curves
    - Photoshop's _magic wand_
      - Clicking on a pixel causes all similar colour to be selected
    - Photoshop's _magic lasso_
      - Draw around the area with the mouse
      - Boundary of selection snaps to the edges within a specified distance
  - **Pixel Point Processing**
    - Redefining individual pixel colours independently from the neighbouring pixels
    - Makes use of a transformation function
    - Used for recolouring a photo, like those stupid Instagram filters.
  - **Pixel Group Processing**
    - More complex processing
    - Redefining colour groups based on neighbouring colours
    - Applying spatial filters
      - Antialiasing
      - Blurring
      - Sharpening
    - Applying arbitrary image filters
      - Warping
      - Morphing

## Data Compression
### Why use Data Compression?
- Uncompressed bitmap images can be quite memory-expensive
- Reduce space on storage
- Reduce transfer time over the network

### Types of Compression
- **Lossy** ─ The original uncompressed can NOT be retrieved from the compressed version.
Only acceptable for pictures  and sounds. Not good for bit-to-bit encoding.
- **Lossless** ─ The original uncompressed can be restored from the compressed version.

#### Compression Algorithms
##### Pixel Packing
  Not an actual compression algorithm, but can reduce the space by colours,
  fitting more than one colour in the same byte.
##### RLE
  Run Length Encoding is a lossless algorithm that tries to encode consecutive values.
  Example of RLE encoding:

    OOOOOOOOOOHJEEEEEEEEEEEEZ

Wound encode to

    1O-1H-1J-12E-1Z

This algorithm is hardly useful for photographic pictures,
but might be still useful for diagrams and computer images
with wide areas with the same exact colour.
##### Dictionary Based Methods

##### JPEG compression

## File Formats
## Animation
## Sound

# Human Computer Interaction
## Design
## Web Design
## Multimedia Design
## Usability Testing
## Interaction Styles
## Human Factors
## Interaction Devices
## Software Development


[FontAnatomy]: http://www.designersinsights.com/wp-content/uploads/2012/03/Anatomy-of-Typography.png
