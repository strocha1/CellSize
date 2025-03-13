# BioSize
A Python Script to read, filter, label, and measure bacterial cells utilizing microscopy images from a phase contrast microscope

## CITATION 
**If you use BioSize, please cite the following paper:**



## LOCAL INSTALLATION
### System requirements
The code has been written in Jupyter Notebook on a Windows system. Please open an issue if you have problems with installation. 
### Dependencies
HOMDscrape relies on the following packages (which can be installed using pip if needed):
- [numpy](https://numpy.org/)
- [pandas](https://pandas.pydata.org/)
- [matplotlib](https://matplotlib.org/)
- [skimage](https://scikit-image.org/)
- [scipy](https://scipy.org/)

### Instructions for use
1. Capture an microscope image of bacteria using a phase contrast microscope.
2. Read the image by changing the image path to the image that needs to be analyzed.
3. Run each code cell one by one and determine which threshold would work the best to filter out noise in the image.
4. The images and filter will overlay and each individual cell will be labeled.
5. Display and save the Dataframe that contains the original label, area, centroid, length, width and adjusted labels of each bacterial cell.
6. Filter out remaining noise before use. 
