# orca-ir
A Python 3 script for (hassle-free) plotting of IR spectra from [ORCA](https://orcaforum.kofo.mpg.de) output files with 
peak dectection and annotation.
It combines the stick spectrum with the convoluted spectrum (gaussian line shape). 
The full spectrum or parts of the spectrum (via matplotlib window) can be plotted.

## External modules
 `re` 
 `numpy` 
 `matplotlib`
 `scipy`  
 
## Quick start
 Start the script with:
```console
python3 orca-ir.py filename
```
it will save the plot as PNG bitmap:
`filename-ir.png`

## Command-line options
- `filename` , required: filename
- `-w`  `N` , optional: line width of the gaussian (default is  `N = 15`)
- `-s` , optional: shows the `matplotlib` window
- `-n` , optional: do not save the spectrum

## Script options
There are numerous ways to configure the spectrum in the script:
Check `# plot config section - configure here` in the script. 
Here, you can configure an absorption or transmittance plot for example.
You can even configure the script to plot of the single gaussian functions.

## Code options
Colors, line thickness, line styles, level of peak detection and 
more can be changed in the code directly.

## Special options and limitations
The spectrum always starts at zero and ends at the maximum wave number. 
If you need only a part of the spectrum, you can start the script with:
```console
python3 orca-ir.py filename -s
```
and use the matplotlib window to zoom to an area of interest and save it.
The PNG file will be replaced everytime you start the script with the same output file. 
If you want to keep the file, you have to rename it. 

## Examples:
![show](/examples/show-use2.gif)
![Example 1](/examples/example1.png)
![Example 2](/examples/example2.png)
![Example 3](/examples/example3.png)
