# Task definition
[Kits19](https://kits19.grand-challenge.org/home/)

There are more than 400,000 new cases of kidney cancer each year, and surgery is its most common treatment. Due to the wide variety in kidney and kidney tumor morphology, there is currently great interest in how tumor morphology relates to surgical outcomes, as well as in developing advanced surgical planning techniques . Automatic semantic segmentation is a promising tool for these efforts, but morphological heterogeneity makes it a difficult problem.

The goal of this challenge is to accelerate the development of reliable kidney and kidney tumor semantic segmentation methodologies. We have produced ground truth semantic segmentations for arterial phase abdominal CT scans of 300 unique kidney cancer patients who underwent partial or radical nephrectomy at our institution. 210 of these have been released for model training and validation, and the remaining 90 will be held out for objective model evaluation.

# Dataset and model weights
Whole dataset can be downloaded from [data](https://github.com/neheller/kits19)

One patient from testing set (patient 202) as well as weights of 2 models (Unet2D, Unet3D) can be downloaded [here](https://drive.google.com/drive/folders/1Fjxo_CURRjnBcz21FVkdOwjJ_rejfRyX?usp=sharing).

Replace case_00202 in this git directory (kits/kits_cases_subset/case_00202) with downloaded case_00202 directory from google drive.

Replace Unet3D in this git directory (kits/kits19_tumor/output_final_models/Unet3D_2020_05_25-18_53_28) with downloaded Unet3D_2020_05_25-18_53_28 directory from google drive.

Replace Unet2D in this git directory (kits/kits19_tumor/output_final_models/Unet2D_small_2020_05_11-17_07_37) with downloaded Unet2D_small_2020_05_11-17_07_37 directory from google drive. 



# How to run notebook
Experiments can be done on whole code. Process of loading model weights, data and initialization of all libraries can be found in *testing_model_weights.ipynb* file.


```python
base_path = '/content/drive/My Drive/kits'
#here are all scripts and model weights
all_scripts = os.path.join(base_path,'kits19_tumor')
#this is folder with data
data_path = os.path.join(base_path,'kits_cases_subset')
```

Above is the structure of whole project in google drive. 
There is no need to manipulate with any folder in git repo. You just need to make sure that in *testing_model_weights.ipynb* file are variables *base_path*, *all_scripts*, *data_path* correct for your specific case.