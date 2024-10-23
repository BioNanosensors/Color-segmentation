Image Segmentation and HSV Color Thresholding Readme

This code processes images of pigment dilutions using HSV color segmentation. The primary goal is to detect and segment specific regions of interest in images based on color thresholds. It is particularly tailored for analyzing natural pigment solutions like hibiscus, curcumin, chlorophyll, and red cabbage.

Photos of pigment dilutions are included in a zip file that can be downloaded in: https://drive.google.com/file/d/1Eu9-1dhsRF8gHDDjC0sYnLknRCvntnIM/view?usp=drive_link

1) In the folder of each pigment, there is a subfolder named as References_Threshold. This images must be initially loaded to the first section of code to compute segmentation thresholds. Modify the file paths to the reference images:

image_low_conc = cv2.imread('path_to_lowest_concentration_image.jpg')
image_high_conc = cv2.imread('path_to_highest_concentration_image.jpg')
image_background = cv2.imread('path_to_background_image.jpg')
image_to_segment = cv2.imread('path_to_test_image.jpg')

2) In the next section code select the background area to compute color difference Delta_E 

3) After that, a set of dilution images having concentrations between the lowest and highest concentration used in the computation of threshold can be automatically segmented. This images must be stored in folders and loaded in the las section of code:

img_folder = 'path_to_folder_with_images'
write_folder = 'path_to_folder_where_segmented_images_will_be_saved'

