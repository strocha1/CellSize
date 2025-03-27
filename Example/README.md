## Folder contains all required files to run the tutorial. 
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
1. Ensure that the image file 'WTA_exp_2025-01-15T13-08-43.213.tif' and the example notebook 'CellSize_example.ipynb' are in the same folder. This is an image of _Escherichia coli_.
2. Read the image and ensure the file size is (1080, 1440, 3).
3. Run each code cell one by one and determine which threshold would work the best to filter out noise in the image.
4. In the 'threshold =' line, the filter can be changed to the one that works best for your use. In this case, threshold_minimum was used. 
5. Section 4 of the code utilizes Regionprops to collect the properties of each object in the frame.  Information such as the original labe, area, centroid, length, and width should be added to a dataframe.
6. In section 4, 'df3 = Outprops[Outprops['Area'] > 60 ]' the number (in this case, 60) can be adjusted to filter out any unwanted particles.
7. The output of section 4 should display a binary mask image overlayed with object labels.
8. Section 5 will display the Dataframe that contains the original label, area, centroid, length, width and adjusted labels of each bacterial cell.
9. Filter using the line described in step 6 as needed.
   
