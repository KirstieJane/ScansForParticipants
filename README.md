# ScansForParticipants
This repository contains code required to create fun "thank you" packs for participants in MRI studies. It takes the structural scans and makes pictures and movies of the brain. The appropriate programs are also included.


### Step 1. Select your scan for distribution
Pick your T1-weighted scan for participant gift distribution. This is usually an MPRAGE, SPGR, or any other T1-weighted scan.

### Step 2. If necessary, convert your dicom file to nifti (nii)
 Download the program mricron [here](http://www.mccauslandcenter.sc.edu/mricro/mricron/install.html).
 Follow the download instructions on the website.
 With mricron you will have downloaded the program [dcm2nii](http://www.mccauslandcenter.sc.edu/mricro/mricron/dcm2nii.html),
 which converts dicom (.dcm) files to nifti (.nii) files.
 Go into the downloaded and installed mricron folder, double click on dcm2niigui. This will open the dcm2nii graphical user interface of the dcm2nii program. Click on "File -> DICOM to NIFTI" and select your folder with your dicom files. It will automatically create a nifti file from your dicom files in the same location as your dicom files, while keeping your original dicom files.
 
### Step 3. Create your participant gift folder.
 Copy the high resolution .nii.gz file to your participant gift folder and rename it to ```high_res.nii.gz```.
 
 
## Outcome 1.
 Give your participant a flashdrive or dvd with the .zip file for the mricron program and their ```high_res.nii.gz``` brain scan file in a folder with additional instructions. 


### Step 4. Creating a video of your ```high_res.nii.gz``` file
Dependencies: Anaconda (or miniconda), nibabel, ImageJ
If you already have a version of Conda installed, please check your version using: ```conda info```

The code used in the following steps has been tested using python version 2.7. If you are using python 3.x, you may encounter some problems. If you do contact [KirstieJane](https://github.com/KirstieJane/).

If you do not have anaconda or miniconda installed, please install this using these instructions.
Download [Anaconda](https://www.continuum.io/downloads) with python version 2.7 and follow the download instructions.
Check your version by typing ```conda info```.

After installing anaconda, install nibabel by typing in your terminal ```pip install nibabel```

Download and install [ImageJ](http://rsb.info.nih.gov/ij/download.html) using instructions provided on the download page.

After you have downloaded all your programs you are ready to create your PNG files from which your awesome videos will be created.

1. Download all the python scripts (or the entire folder) using the Download ZIP button.
2. Open terminal and change to your working directory, e.g.

   ```
   cd ~/User/Documents/ScansForParticipants
   ```
3. We will be using the MakePngs_HighRes.py script for creating the PNG files. This will create PNG files in the axial, coronal and sagittal directions. You can check the help file by typing

  ```
  python MakePngs_HighRes.py --help
  ```
  You positional arguments are:
  
   - bg_fname              File name for background .nii.gz image
   - overlay_fname         File name for overlay .nii.gz image
   - output_dirname        Output directory for .png images
  
  In addition, if you would like to change the overlay of the brain to another colourmap (e.g. gray) you can do this with the -cm2 command. For example, I would like to use colourmap "gray", my bg_fname is Example_Participant/high_res.nii.gz,  my overlay_fname is Example_Participant/high_res.nii.gz and my output_dirname is Example_Participant/PNGs
  ```
  python MakePngs_HighRes.py -cm2 gray Example_Participant/high_res.nii.gz Example_Participant/high_res.nii.gz Example_Participant/PNGs
  ```
  
4. Open ImageJ to create a video of your PNGs files: 

File -> Import -> Image Sequence
  
Then you nagivate to the folder that holds all your PNGs and choose that folder. In the sequence options box type your preferred direction in the "File name contains" box, e.g. axial, and click OK. This will create your video in a new window. 

While having that window selected, click File -> Save As -> AVI.. In the diaglog box that appears, keep the compression option to JPEG and choose your frame rate. The default frame rate of 7 should be fine. Click ok and name file as appropriate in your folder of choice, e.g. axial_movie.avi in the Example_Participant folder.

## Outcome 2.
 Give your participant a flashdrive or dvd with the .zip file for the mricron program and their ```high_res.nii.gz``` brain scan file in a folder with additional instructions. And include you new axial, sagittal and coronal .avi video files for more excitement.



 
