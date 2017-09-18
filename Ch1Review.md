# 讀書心得
## Video codec design Ch2
### 2.2
* Video image is 3D scene projection onto 2D one.
* Spatial and temporal sampling
    * spatial => video resolution
    * temporal => frame rates
* scene => camera => capture => processing/storage/transmission => display
* sampled image is defined at a series of regularly spaced sampling points. most common is a rectangle.
* temporal sampling can be improved by interlacing.
    * PAL video improved from 25Hz to 50Hz by interlacing.

### 2.3
* A monochrome('grey scale') uses just one number per spatio-temporal sample.
* Human Visual System(HVS) is less sensitive to colour than to luminance.
* YCrCb is more efficient.
    * Y: luminance
    * Cr: red chrominance
    * Cb: blue chrominance
    * Cr+Cb+Cg = 1
    * ITU BT.601: Y = 0.299 R + 0.587 G + 0.114 B

* YCrCb sampling 4:4:4 vs 4:2:2 vs 4:2:0
* 720x576px image:
    * 4:4:4 720x576 samples, 8bits = 720x576x8x3 = 9953280 bits
    * 4:2:0 360x288 samples, 8bits = (720 x 576 x 8) + (360 x 288 x 8 x 2) = 4976640 bits

### 2.4
* some components of HVS

### 2.5
* DSCQS testing system => expensive and time-consuming.
* Peak signal to noise ratio(PSNR) = 10log(2^n - 1)^2 / MSE
* ITU-T Video Quality Experts Groups(VQEG) are developing a starndard for objective video quality evaluation.

## Video processing and communications Ch1
### 1.1
* illuminating source vs reflecting source
* illuminating: additive rule
* reflecting: subtractive rule
* eye cones => colour tone
* eye rods => luminance
* RGB primary set vs CMY primary set

### 1.2
* video camera and video display
* composite video(S-video) vs component video
* gamma correction => exponential scale

### 1.3
* Progressive and interlaced raster scan
* very complex spectrum functions

### 1.4
* NTSC vs PAL
* NTSC frame rate: 59.94 Hz, line number: 525 lines/frame
* PAL frame rate: 50 Hz, line number: 625 lines/frame
* YIQ vs YUV vs YDbDr
* Signal bandwidth physics

### 1.5
* some notation introduction
* spatial and temporal resolution
* Linear transform: RGB => YCbCr
* ITU-R BT.601: 4:4:4 vs 4:2:2 vs 4:2:0
* ISO-MPEG introduction
* MEPG-2 is the cornerstone of the next gerneration of TV system
* Video Quality Measurement: MSE, PSNR, MAD
