## Contrastive Memory Feature Transfer for Non-shared-and-Imbalanced Unsupervised Domain Adaption(TII2022)

This repository contains PyTorch evaluation code, training code and pretrained models for CMFT.

For details see [CMFT](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9976256) by Guangyi Xiao, Shun Peng, Weiwei Xiang, Hao Chen, Jinzhi Guo and Zhiguo Gong

### Following the 5 steps below to train CMFT

#### 1. experiment environment
   &emsp;&emsp;`python=3.7`
   
   &emsp;&emsp;run command below to install other packages
   
   &emsp;&emsp;`pip install -r requirements.txt`
   
#### 2. download datasets
   &emsp;&emsp;Office-Home: `https://drive.google.com/u/0/uc?id=0B81rNlvomiwed0V1YUxQdC1uOTg&export=download`
   
   &emsp;&emsp;DomainNet: `http://ai.bu.edu/M3SDA`

   
#### 3. replace the path in txt file which located in `./data/`

#### 4. run '**CMFT**' on UDA
   &emsp;&emsp;Enter the following command or modify the parameter settings in `train.py` to run `train.py` directly
   
   &emsp;&emsp;`cd trainer/`
   
   &emsp;&emsp;`python train.py --config ../config/officehome_UDA.yml --src_address ../data/officehome/Art_65.txt --tgt_address ../data/officehome/Clipart_65.txt --gpu_id 0`
   
#### 5. run '**CMFT**' on NI-UDA
   &emsp;&emsp;`cd trainer/`
   
   &emsp;&emsp;`python train.py --config ../config/officehome_NIUDA.yml --src_address ../data/officehome/Art_small_25.txt --tgt_address ../data/officehome/Clipart_small_25.txt --src_ns_address ../data/officehome/Art_noshare_40.txt --gpu_id 0`

   &emsp;&emsp;more run command in `train.sh` 
   
## Citation
If you find that CMFT interesting and help your research, please consider citing it:
```
@article{2022cmft,
  author={Xiao, Guangyi and Peng, Shun and Xiang, Weiwei and Chen, Hao and Guo, Jingzhi and Gong, Zhiguo},
  journal={IEEE Transactions on Industrial Informatics}, 
  title={CMFT: Contrastive Memory Feature Transfer for Non-shared-and-Imbalanced Unsupervised Domain Adaption}, 
  year={2022},
  volume={},
  number={},
  pages={1-12},
  doi={10.1109/TII.2022.3227637}
}

```
