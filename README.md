# collembola-counter
Counting objects on image.
The project aims to solve the problem of a friend working in a biology lab. They have soil samples with collembola larvae and adults (tiny white worms). They colour the soil to purple for better contrast and spread it out in a petri disk. They need to count the larvae and adults in the petri disk. Since there are many very tiny larvae (couple of hundreds), the manual counting is cumbersome, time consuming, and tiring.
![Alt text](IMG_0048.JPG?raw=true "Title")
The proposed program first segments the region of interest (ROI), the central area of the petri disk. Then it uses intensity thresholding to keep the highest intesity shapes only which includes the larvae and adults. As a last step it contours the high intensity shapes and classifies them to larvae (children), adult, and noise categories based on pre-defined contour length thresholds.

The model parameters are fitted using a smaller patch of the high resolution input image. Then it is evaluated on the whole image.

### Note:
The code and comments are currently in a jupyter notebook. Since GitHub sometimes fails to load notebooks, you can open it using [nbviewer](https://nbviewer.jupyter.org/).

When I receive some more images I'll update the project with the results on them.
