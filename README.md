# Monocular depth map generation using CNN | FastDepth
This repo contains Pytorch implementation of depth estimation deep learning network based on the published paper: [FastDepth: Fast Monocular Depth Estimation on Embedded Systems](https://arxiv.org/pdf/1903.03273.pdf)

### Step-by-Step Procedure
Use the following commands to install all dependencies

**GPU based enviroment on colab**:
```
!git clone https://github.com/tau-adl/FastDepth
%cd FastDepth/
!pip install -r pip_requirements.txt
!pip3 install 'prompt-toolkit<2.0.0,>=1.0.15' --force-reinstall

```

# NYU database
Download the preprocessed NYU Depth V2 dataset in HDF5 format and place it under a data folder outside the repo directory. The NYU dataset requires 32G of storage space.
 ```
!/content/FastDepth/DataCollect.sh
```
# Train
```
python3 main.py -train -p 100 --epochs 20
```
# Evaluate
```
python3 main.py --evaluate /home/usr/results/trained_model.pth.tar
```
