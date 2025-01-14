<img src="https://i.imgur.com/gb6B4ig.png" width="400" alt="Weights & Biases" />

# Learn Effective MLOps: Model Development

This repository contains materials for our [MLOps Course](https://www.wandb.courses/courses/effective-mlops-model-development)

Bringing machine learning models to production is challenging, with a continuous iterative lifecycle that consists of many complex components. 

Having a disciplined, flexible and collaborative process - an effective MLOps system - is crucial to enabling velocity and rigor, and building an end-to-end machine learning pipeline that continually delivers production-ready ML models and services.

## 🚀 [Enroll for free](https://www.wandb.courses/courses/effective-mlops-model-development)

## What you'll learn

- Best practice machine learning workflows
- Exploratory data analysis with Tables and Reports in W&B
- Versioning datasets and models with Artifacts and Model Registry in W&B
- Tracking and analyzing experiments
- Automating hyperparameter optimization with Sweeps
- Model evaluation techniques that ensure reproducibility and enterprise-level governance

# My Notes

**My notebooks**  
Lesson 1: [01_EDA.ipynb](https://nbviewer.org/github/Nov05/wandb-edu/blob/main/mlops-001/lesson1/01_EDA.ipynb), [02_Split.ipynb](https://nbviewer.org/github/Nov05/wandb-edu/blob/main/mlops-001/lesson1/02_Split.ipynb), [03_Baseline.ipynb](https://nbviewer.org/github/Nov05/wandb-edu/blob/main/mlops-001/lesson1/03_Baseline.ipynb)  
Lesson 2: [04_refactor_baseline_02.ipynb](https://nbviewer.org/github/Nov05/wandb-edu/blob/main/mlops-001/lesson2/04_refactor_baseline_02.ipynb), [04_refactor_baseline_03_ubuntu-wsl.ipynb](https://nbviewer.org/github/Nov05/wandb-edu/blob/6c232b0cd4c46863e056425d3d7c8bd20c342189/mlops-001/lesson2/04_refactor_baseline_03_ubuntu-wsl.ipynb)  

**Baseline run overview**  
<img src="https://raw.githubusercontent.com/Nov05/pictures/master/repos/wandb-edu/2023-03-07%2004_35_52-royal-sky-5%20_%20mlops-course-001%20%E2%80%93%20Weights%20%26%20Biases.jpg">  

**[My baseline report](https://api.wandb.ai/links/novemberfifth/dlmvt4ss)**  
<img src="https://raw.githubusercontent.com/Nov05/pictures/master/repos/wandb-edu/2023-03-08%2011_45_24-20230224_mlops_lesson-1_03-baseline%20report%20_%20mlops-course-001%20%E2%80%93%20Weights%20%26%20Biases.jpg" width=600>  

【**Caution**】  
1. For lesson 2, if you use a local machine, file `conda-environment.yaml` in Lesson 2 won't work for Windows, cause pytorch/vision just does **NOT** support Windows well. You can install Ubuntu WSL and [set up the enviroment with miniconda](https://www.how2shout.com/linux/install-miniconda-on-ubuntu-22-04-lts-jammy-linux/) there. 
2. If you use Google Colab, there is no need to install conda then create the env from yaml, which would cause a few problems that are hard to solve. You can just pip install `wandb` and run the notebooks.    
3. Remeber to change the configurations in `params.py` and `sweep.yaml`.  
<img src="https://raw.githubusercontent.com/Nov05/pictures/master/repos/wandb-edu/2023-03-08%2004_39_06-root%40guido_%20_mnt_d_github_wandb-edu_mlops-001_lesson2.jpg">  

4. If you run into **error** `Could not load library libcudnn_cnn_infer.so.8. Error: libcuda.so: cannot open shared object file: No such file or directory
Please make sure libcudnn_cnn_infer.so.8 is in your library path`, which is probably related to Ubuntu 22.04.2 LTS, cause some users reported that they downgraded to Ubuntu 20.04 and then had no problems, [add the following config](https://discuss.pytorch.org/t/libcudnn-cnn-infer-so-8-library-can-not-found/164661).   

> As discussed in this issue 155 it is just a matter to add this in the `.bashrc`:  
> `export LD_LIBRARY_PATH=/usr/lib/wsl/lib:$LD_LIBRARY_PATH`  
> Be sure that your library is in /usr/lib/wsl/lib, to see it you can run  
> `ldconfig -p | grep cuda`   

You can check the config with command `$cat ~/.bashrc`.  
[Install text editor](https://help.ubuntu.com/community/gedit) with command `$sudo apt-get install gedit`.  

