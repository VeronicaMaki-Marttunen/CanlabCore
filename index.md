The CANlab Core Tools package is a set of Matlab functions that are designed to serve miscellaneous purposes. Many of them have stand-alone command line function, but the toolbox also contains functions that are used in other CANlab toolboxes, and so this package should be downloaded and put on the Matlab path when using any of the toolboxes.

Some functions are experimental/in development, and the toolbox is provided on an as-is basis, with no claims about quality or correctness expressed or implied.

Our vision is that the package will be developed into an extensible package that will allow developers and statisticians to create new tools and make them available to the community without rew-writing basic image manipulation and visualization code. We call this framework "statistical plug-in for neuroimaging analysis" (SPINN).

There are several general ways to use these tools stand-alone:

1) A new set of object-oriented tools offers a command-line interface for working with fMRI data and other data types interactively. 

2) Many of the functions work by turning a brain image (.img or .nii) into a "clusters" structure, a vector of structures that stores information about a continuous activation 'blob'. You can turn a thresholded image (some values are zero or NaN) into a clusters structure using mask2clusters.m.  Once you have done this, you can visualize, extract data, perform analyses, etc. on the clusters.

3) You can run any analysis that you can run on a single voxel over the whole brain with image_eval_function and image_eval_function_multisubj.

4) Another set of functions, with names beginning with iimg_*, works by turning one or more 3-D image files (.img or .nii) into a single-column vector per image file. This makes the images easier to work with. They can be converted to/from clusters structures or 3-D/4-D volumes. Functions exist for defining masks, extracting data, and other things.

5) The toolbox also contains a number of miscellaneous statistical functions used in other toolboxes, and some stand-alone tools for cross-validation (xval_***).