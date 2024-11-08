# PFAD for motion artifact removal
This is the codebase for the article "Motion Artifact Removal in Pixel-Frequency Domain via Alternate Masks and Diffusion Model". 

This repository is based on [guided-diffusion](https://github.com/openai/guided-diffusion).

**Download the pre-trained model**

We provide the pre-trained model for HCP dataset, please save it to ```results/model/brain```. 

Here are the download link: 
[Google Drive](https://drive.google.com/file/d/1Hh0wabKmW5CUXpUAS4GcEHZIoYeZq_v-/view?usp=sharing)

**Artifact removal via the pre-trained model**

At the beginning, we need to build an environment called ```artifact_removal```.
```
conda env create -f environment.yml
```
To get the inference results of PFAD, please run:
```
cd scripts
python image_sample.py --conf_path ../conf/brain_sample_config.yml --img_dir brain --save_path motion_remove
```
Then, you can obtain the results of the example images after removing motion artefacts in ```results/motion_remove```

We currently only provide the code for the inference process, you can refer to [guided-diffusion](https://github.com/openai/guided-diffusion) for training process.
