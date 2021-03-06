# CV-Course-CellDetection

This respository presents Computer Vision (COMP9517) Group Project, created by Group 1. Review presentation pdf for quick summary, report pdf for detailed analysis. Sample Video is also provided

Overview is presented as following do points:
- Detecting 3 different Cell types [PhC-C2DL-PSC, Fluo-N2DL-HeLa, DIC-C2DH-HeLa]
- Tracking 3 different Cell types [PhC-C2DL-PSC, Fluo-N2DL-HeLa, DIC-C2DH-HeLa]
- Presenting motion analysis for 3 different Cell types [PhC-C2DL-PSC, Fluo-N2DL-HeLa, DIC-C2DH-HeLa]
- Limitation of proposed method

To run the overall file:
1) Copy and paste raw images into RawData, do not change the names
2) Run generate_model.py with the given requirements in requirements.txt. Output directories of predicted outcome will be generated
3) Run Split_Raw_img.py in order to split the output image from UNET to segmented and distance transformed
4) Run respective dataset's post-processing.py in order to perform post processing
5) Run Box_Drawing_script.py to perform detection and tracking:
    - Note, requested output for Task 1,2,3 are printed on output image (3D graph), pop up of image window is deleted as
    it largely stops the overall process, hence focusing on post-processing video for visualizaiton of output
    - Terminal is mainly for tracking process  and providing command in executing
    - Motion analysis for a single cell can be performed at the end of each sequence run by inputting the cell-id
    desired for tracking, cell-id can be retrieved from annotation html file under Results-Annotation
6) Respective Static results are shown:
    - Results-Annotation Directory: Per frame motion analysis of cells
    - Results-BoundaryBox: Drawing of cell boundary box with trajectory (note id is not labelled as it caused clustering
    making un-visible image in Dataset 3 - PhC-C2DL-PSC)
    - Results-PathImage: Drawing of trajectory per frame with requested Task 1 and 2, total cell count and division count
7) Run Video_creator.py for putting all output together into a simple avi output video
    - output video will be placed under respective folder for each Dataset, Results-Video
