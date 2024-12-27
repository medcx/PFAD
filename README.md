<div align="center">
  
<h1> Motion Artifact Removal in Pixel-Frequency Domain via Alternate Masks and Diffusion Model </h1>

<div>
    <a href='https://scholar.google.com.hk/citations?user=NC_8AWkAAAAJ'target='_blank'>Jiahua Xu</a><sup>1</sup>&emsp;
    <a href='https://scholar.google.com.hk/citations?user=7H-LIigAAAAJ'target='_blank'>Dawei Zhou</a><sup>1</sup>&emsp;
    <a href='https://scholar.google.com.hk/citations?user=AyboWyoAAAAJ'target='_blank'>Lei Hu</a><sup>2</sup>&emsp;
    Jianfeng Guo<sup>3</sup>&emsp;
    Feng Yang<sup>3</sup>&emsp;
    </br>
    Zaiyi Liu<sup>2</sup>&emsp;
    <a href='https://scholar.google.com.hk/citations?user=SRBn7oUAAAAJ'target='_blank'>Nannan Wang</a><sup>1</sup>&emsp;
    <a href='https://scholar.google.com.hk/citations?user=VZVTOOIAAAAJ'target='_blank'>Xinbo Gao</a><sup>4</sup>&emsp;
</div>
<div>
    <sup>1</sup>State Key Laboratory of Integrated Services Networks, Xidian University;<br>
    <sup>2</sup>Department of Radiology, Guangdong Provincial People’s Hospital, Southern Medical University;<br>
    <sup>3</sup>Department of Radiology, Xiangyang No. 1 People’s Hospital, Hubei University of Medicine;<br>
    <sup>4</sup>Chongqing Key Laboratory of Image Cognition, Chongqing University of Posts and Telecommunications;
</div>
</br>
<div>
    <strong>AAAI 2025</strong>
</div>
<div>
    <h4 align="center">
        <a href="https://github.com/medcx/PFAD/" target='_blank'>
        <img src="https://img.shields.io/badge/🤗%20Github-PFAD-yellow">
        </a>
        <a href="https://arxiv.org/abs/2412.07590" target='_blank'>
        <img src="https://img.shields.io/badge/arXiv%20paper-2412.07590-b31b1b.svg">
        </a>
    </h4>
</div>


</div>


---
## 🔥Caption

This is the codebase for the article [Motion Artifact Removal in Pixel-Frequency Domain via Alternate Masks and Diffusion Model](https://arxiv.org/pdf/2412.07590) (AAAI 2025).

This repository is based on [guided-diffusion](https://github.com/openai/guided-diffusion).

## 🔍Overview

PFAD is a method for medical image motion artifact removal using pixel-frequency domain information combined with alternate masks.

![overall_framework](./assets/method.png)

## 🔧Quick Start

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

## ⚡Results

We show the visualization results on HCP (Brain dataset).

![visualization results](./assets/brain.png)

## 📧Contact

If you have any questions, please contact jhxu.xidian@gmail.com.

## 📖 Citation
If you find our work useful for your research, please consider citing our paper:
```
@article{xu2024motion,
  title={Motion Artifact Removal in Pixel-Frequency Domain via Alternate Masks and Diffusion Model},
  author={Xu, Jiahua and Zhou, Dawei and Hu, Lei and Guo, Jianfeng and Yang, Feng and Liu, Zaiyi and Wang, Nannan and Gao, Xinbo},
  journal={arXiv preprint arXiv:2412.07590},
  year={2024}
}
```
