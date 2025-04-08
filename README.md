# CellSize
A Python Script to read, filter, label, and measure bacterial cells utilizing microscopy images from a phase contrast microscope


## LOCAL INSTALLATION
### System requirements
The code has been written in Jupyter Notebook on a Windows system. Please open an issue if you have problems with installation. 
### Dependencies
CellSize relies on the following packages (which can be installed using pip if needed):
- [numpy](https://numpy.org/)
- [pandas](https://pandas.pydata.org/)
- [matplotlib](https://matplotlib.org/)
- [skimage](https://scikit-image.org/)
- [scipy](https://scipy.org/)
- [seaborn](https://seaborn.pydata.org/index.html)
- [glob](https://docs.python.org/3/library/glob.html#module-glob)
- [os](https://docs.python.org/3/library/os.html)
- [re](https://docs.python.org/3/library/re.html)

### Instructions for use
#### 1. Packages
-	Import the packages that are required for the code to run. 
#### 2. Specifying the Input and Output directories
-	Specify where the input files are located. This can be the folder that contains all of the .tiff images that need to be analyzed.
#### 3. Describing functions
-	The defined function “extract_condition” works to extract condition naming schemes based on the file naming scheme. This may need to be adjusted to match your personalized naming scheme. Use [re](https://docs.python.org/3/library/re.html) to adjust this. 
-	The defined function “process_image” is based off the [CellSize_main.ipynb](https://github.com/strocha1/CellSize/blob/main/Comparing%20Datasets%20Barplots/CellSize_main.ipynb) that follows the following structure: 1. Converting image into a binary_mask. 2. Selection and application of filter to identify object in the field. 3. Inversion and labeling of components in the field. 4. Storing of properties such as label, area, centroid, length, and width. 5. Filtering based on area. 6. Creation of a new binary mask with updated labels. 
-	“process_image” may need to be adjusted to fit individual needs. This can be done by selecting a different filter, or adjusting the area filter to fit that of a particular cell. 
#### 4. Labeled object CSV generation
-	CSV files of each individual .tiff image is generated and saved to the marked output directory.
#### 5. Merging files and conversion to microns
-	Pixels_per_micron may need to be adjusted depending on individual needs. The x40 lens in our lab is a Nikon plan 40x/0.65 lens which uses a 6 pixels per micron conversion. 
-	The defined function “Process_and_visualize” works to convert the pixel information from the previous .csv files to microns using the pixel to micron conversion. After this, it will plot individual histograms of area, length, and widths as well as an aspect ratio of the cells. 
#### 6. Process and visualize data
-	Using the previously described .csv files, you can combine them and visualize using the “process_and_visualize” command. 
-	If needed, a combined .csv file can be generated with information from all of the .csv files generated with this code. 

