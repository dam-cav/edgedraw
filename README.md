# edgedraw
[linedraw](https://github.com/LingDong-/linedraw) fork with changes to get compatibility with python 3.

Differences from the original repository:

- Doesn't work with *.tif* files;
- Added compatibility with *.png* images with transparent background;
- Only the silhouettes of the figures are sketched;

In particular, this is no longer designed specifically for plotters but actually serves to achieve a nice effect in redesigning icon silhouettes.



Convert images to vectorized line drawings.
![Alt text](/screenshots/screen.png?raw=true "")

## Usage
Convert an image to line drawing and export .SVG format:
```shell
$ python linedraw.py -i input.jpg -o output.svg -t 235 -s 4
```
Command specs:
```
usage: linedraw.py [-h] [-i [INPUT_PATH]] [-o [OUTPUT_PATH]] [-b] [-t [INT_VALUE]] [-s [INT_VALUE]] [-nc] [-nh]
                   [--no_cv] [--hatch_size [HATCH_SIZE]]
                   [--contour_simplify [CONTOUR_SIMPLIFY]]

Convert image to vectorized line drawing for plotters.

optional arguments:
  -h, --help            show this help message and exit
  -i [INPUT_PATH], --input [INPUT_PATH]
                        Input path
  -o [OUTPUT_PATH], --output [OUTPUT_PATH]
                        Output path.
  -b, --show_bitmap     Display bitmap preview.
  -t [INT_VALUE], --threshold [INT_VALUE]
                        Defines the brightness to which the lightest shapes are ignored.
                        (Use value between 200 and 250 to get good result!)
  -s [INT_VALUE], --sigma [INT_VALUE]
                        Defines how tolerant the detection of the edges is.
                        (Use value between 1 and 10 to get good result!)
  -nc, --no_contour     Don't draw contours.
  -nh, --no_hatch       Disable hatching.
  --no_cv               Don't use openCV.
  --hatch_size [HATCH_SIZE]
                        Patch size of hatches. eg. 8, 16, 32
  --contour_simplify [CONTOUR_SIMPLIFY]
                        Level of contour simplification. eg. 1, 2, 3
```