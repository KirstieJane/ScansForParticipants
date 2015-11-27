# ScansForParticipants
This repository contains code required to create fun "thank you" packs for participants in MRI studies. It takes the structural scans and makes pictures and movies of the brain. The appropriate programs are also included.


### Step 1. Select your scan for distribution
Pick your T1-weighted scan for participant gift distribution. This is usually an MPRAGE, SPGR, or any other T1-weighted scan.


### Step 2. If necessary, convert your dicom file to nifti (nii)
 Download the program mricron [here](http://www.mccauslandcenter.sc.edu/mricro/mricron/install.html)
 Follow the download instructions on the website.
 With mricron you will have downloaded the program [dcm2nii](http://www.mccauslandcenter.sc.edu/mricro/mricron/dcm2nii.html),
 which converts dicom (.dcm) files to nifti (.nii) files.
 Go into the downloaded and installed mricron folder, double click on dcm2niigui. This will open the dcm2nii graphical user interface of the dcm2nii program. Click on "File -> DICOM to NIFTI" and select your folder with your dicom files. It will automatically create a nifti file from your dicom files in the same location as your dicom files, while keeping your original dicom files.
 
### Step 3. Create your participant gift folder.
 Copy the high resolution .nii.gz file to your participant gift folder and rename it to ```high_res.nii.gz```
 
## Outcome 1.
 Give your participant a flashdrive or dvd with the .zip file for the mricron program and their ```high_res.nii.gz``` brain scan file in a folder with additional instructions. 

 
