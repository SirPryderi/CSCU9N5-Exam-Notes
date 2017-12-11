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
    * [Images Compression Algorithms](#images-compression-algorithms)
      * [Pixel Packing](#pixel-packing)
      * [RLE](#rle)
      * [Dictionary Based Methods](#dictionary-based-methods)
      * [JPEG compression](#jpeg-compression)
      * [Video Compression Algorithms](#video-compression-algorithms)
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

### Images Compression Algorithms
#### Pixel Packing
  Not an actual compression algorithm, but can reduce the space by colours,
  fitting more than one colour in the same byte.
#### RLE
  Run Length Encoding is a lossless algorithm that tries to encode consecutive values.
  Example of RLE encoding:

    OOOOOOOOOOHJEEEEEEEEEEEEZ

Wound encode to

    1O-1H-1J-12E-1Z

This algorithm is hardly useful for photographic pictures,
but might be still useful for diagrams and computer images
with wide areas with the same exact colour.

#### Dictionary Based Methods
Dictionary compression algorithms are can store entire pattern that are used
more than once to save space.

**Huffmann & CCITT Compression** was developed for fax machines and documents scanner.
Uses a predefined dictionary of b&w documents, and it is not stored in the compressed file.

**Lempel-Ziv-Welch Algorithm** is another example of dictionary-based compression.
The dictionary is constructed s the the encoding progresses. The compressed file
becomes also the dictionary, saving space. Still not good for photographic images.

#### JPEG compression
Joint Photographic Expert Group is designed to compress
photographic pictures with a lossy algorithm, especially
exploiting the inability of the human eye to see full a
range of colours. Not adequate for diagrams and similar.

Steps:
1. Convert image to HSV to create a γ map
2. Downsample the colour map by 2x
3. Divide both γ and colour map in 8x8 pixel blocks
4. For each block, perform a _discrete cosine transformation_ on the data
5. Use quantisation of the previous values
6. Store these numbers in an efficient way


#### Video Compression Algorithms
Since videos have also a time dimension, they not only be compressed _spatially_
but also _temporally_, meaning that adjacent frames can be compressed detecting
changes between them. Certain frames are designated ask _key frames_, that get
compressed only spatially. Each frame between key frames is replaced by a _difference
frame_, that get compressed even further with linear compressions.

**CODECs** are compression/decompression algorithm, often proprietary and
hardware-implemented.

Video data-rate is extremely high, even for our modern network speeds and
storage capabilities, thus compression algorithm on videos are absolutely vital.

## File Formats
Nothing here just yet, move along!

## Animation
To produce an animation still images are displayed in rapid sequence,
the it's left to the human eye to perceive motion. At least 10 frames
per second are required to produce a flicker-free motion, but much
more a required to produce a very smooth motion.

### Creation
- **Model Design** ─ Uses a modelling tool to produce the objects to be animated.
- **Animation Design** ─ Motion sequences, lighting, action and interaction are planned to a script.
- **Rendering** ─ The script is run and a raster version is produced.
- **Post-Production** ─ The final raster version is edited to match the creator's idea.

## Sound
In a multimedia application, sound can be used as an input device, as an output device or both.

![Sound Wave][SoundWave]

Sound is a pressure wave which travels in air at about 331 m/s,
with a frequency between 20 and 20,000 Hz.

The sound wave has two physical characteristics:

- **Amplitude** ─ The height of the wave, also measure the strength of the sound.
- **Frequency** ─ The number of compressions per second.

From the perspective of a human observer, the sound has three main characteristics:

- **Loudness** ─ how intense the sound is perceived.
- **Pitch** ─ The sense of the sound having a tone.
- **Timbre** ─ The nature of the sound.

Loudness is perceived logarithmically by the human hear, and
decibels (dB), a logarithmic scale, is the official unit for
sound loudness.

### Dynamic range
The dynamic range is the loudest measurable signal compared to quietest signal.
It is measured using decibels (dB), a logarithmic scale.
The range is defined as follows: `range = 10 × log(max ÷ min)`.

The dynamic range of a 16-bit linear track (like in CD quality) is around 96 dB.

### Sound Transduction
Sound transduction is the process of converting a sound wave,
into a different form of energy, i.e. electrical current.
This is the internal process that powers the microphone.

Microphones have a limited frequency response, they are more sensitive to sounds
with certain frequencies.
They also have limited dynamic range, they cannot deal well from sounds from the
quietest to the loudest.

Sounds are digitised using an analogue-to-digital converter (ADC).
Sounds is reproduced using a digital-to-analogue converter (DAC).
Both process introduces imperfections, reason why it is impossible to perfectly
reproduce a recorded sound.

Analogue-to-digital conversion has two parameters:
- **Sampling Rate** ─ How many measure per second are performed.
Measured in samples/second or Hz.
- **Sample Size** ─ It's the size in bits (usually 8, 16, 32)
and measure the precision of each sampling (the higher the better).
Can be either linear (more precision) or logarithmic
(wider range, lower resolution at higher values).

![Sample Rate][SamplingRate]

According to the **Nyquist sampling theorem**,
the **sampling rate** must be twice the highest frequency of interest,
otherwise **aliasing** may occur.

The **bit-rate** is defined as `sample-rate × sample-size`.

The size of a track is defined by the following relationship:

`size = bit-rate × 8 × length × channels_no`.

### Sound compression
Due to the high difference between samples and the need to have an extremely
high range of amplitudes, make particularly hard to compress sound.

A simple **lossless** way to compress audio could to be to apply a threshold of
silence, and compress the silence with run-length encoding.

#### Differential Pulse Code Modulation (DPCM)
This method is based on storing the difference between samples,
but there is no reason to assume that the difference between the frames might be
small at all.

#### Adaptive Differential Pulse Code Modulation (ADPCM)
Similar to DPCM, but uses an adaptive sample size to make a more efficient of
bits, taking account of the change of signal.

#### Linear Predictive Coding
Linear Predictive Coding uses a mathematical model of the vocal tract.
Instead of transmitting the original sound, it is converted into a model of the
vocal tract, and it is sent over, achieving great compression, but very low
voice fidelity.

As a comparison, image that a picture is
approximated into a vector format, and then sent over the network and
reconstructed. Yeah, it is as bad as you are imagining.

#### Perceptually Based Compression
This wide area of compression tries to reduce the size, by deleting signals our
ear is not capable of perceiving. For instance:

- Too quiet
- Obscured by another sound
- Outside the hearing range

These algorithms are extremely hard to implement, and thanks Codd, we won't
dwell any further in the details. Just know that **MP3** and **AAC** make use of
these techniques to achieve good lossy compression, with very little perceivable
difference.

### Known Sound Formats
- **WAV** ─ Windows Waveform. Can be both lossy and lossless using (A)DPCM.
- **SND** ─ NeXT/SUN file format.
- **MPEG** ─ Both in MP3 and the new AAC variant.
- **FLAC** ─ Free Lossless Audio Codec, part of the OGG family.

### Midi
Musical Instruments Digital Interface is a set of commands used to
reproduce notes with different instruments digitally. It is left
to the target machine to reproduce the sound. There is no guarantee
on support or final quality due to the MIDI implementation often being
hardware-implemented. Additionally, it has no support for voice.
Like SVG for music. Just way less useful.

-------------------------------------------------

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
[SoundWave]: https://scienceaid.net/images/b/b6/crest.png
[SamplingRate]: https://i.stack.imgur.com/tWdb0.gif
