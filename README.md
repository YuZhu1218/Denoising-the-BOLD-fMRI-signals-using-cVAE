# Denoising-the-BOLD-fMRI-signals-using-cVAE
This is the final project of class CSCI3397 Biomedical Image Analysis by Yu Zhu and Jiayi Li

## Package dependencies

    numpy
    nibabel
    sklearn
    matplotlib
    torch

    
## Dataset
In total 5 input files are need, which are 

    anat.nii.gz
    func.nii,gz
    gm.nii.gz
    wm.nii.gz
    csf.nii.gz
    
  The 'nat.nii.gz' is the anatomical  3d images of human whole brain. The 'func.nii,gz' is the functional MRI 3D images of human whole brain over time, which is 4D. 'gm.nii.gz', 'wm.nii.gz', and 'csf.nii.gz' are the probability maps of gray matter tissues, white matter tissues, and cerebrospinal fluid tissues of human whole brain with the same size of the anatomical images. 
  
## Commands
To call the cVAE model, use following code in the shell:

    python finalproject_cvae_arg.py -a ./anat.nii.gz -gm ./gm.nii.gz -wm ./wm.nii.gz -csf ./csf.nii.gz -f ./func.nii.gz -e epoch_num -b batch_size
    
where epoch_num is the number of epoch used to train the model and batch_size is the batch size used when loads datasets.
    
    

