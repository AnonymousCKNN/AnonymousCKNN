# Cleansed k-nearest neighbor (CKNN)

Anonymous Submission #4835 to ICCV 2023.

# Installation

#### Step 1. Install libraries
- We used python=3.7
- Install libraries in [requirements.txt](requirements.txt)
- If the code doesn't work, try this: [requirements_all.txt](requirements_all.txt).   

#### Step 2. Download files

- [Download features](https://drive.google.com/file/d/14Gqj2X1OmL64hSgTUMLnCDxdZCk7-mue/view?usp=share_link)
- [Download meta data](https://drive.google.com/file/d/1IdVelWK9cGuaaLczotPxCx1V2elAdWBd/view?usp=share_link)
- [Download all 6 files of patches in this folder](https://drive.google.com/drive/folders/1iNGFY7fuOG4bCrbQAF1-VE9aI7BdC1zi?usp=sharing)

#### Step 3. Untar all *.tar.xz files and place properly
- File structure should be like below.
```
AnonymousCKNN
├── features
│   ├── avenue
│   │   ├── test
│   │   └── train
│   ├── ped2
│   │   ├── test
│   │   └── train
│   └── shanghaitech
│       ├── test
│       └── train
├── meta
│   ├── frame_labels_avenue.npy
│   ├── frame_labels_ped2.npy
│   ├── frame_labels_shanghaitech.npy
│   ├── test_bboxes_avenue.npy
│   ├── test_bboxes_ped2.npy
│   ├── test_bboxes_shanghaitech.npy
│   ├── test_lengths_avenue.npy
│   ├── test_lengths_ped2.npy
│   ├── test_lengths_shanghaitech.npy
│   ├── train_bboxes_avenue.npy
│   ├── train_bboxes_ped2.npy
│   └── train_bboxes_shanghaitech.npy
├── patches
│   ├── avenue
│   │   ├── test
│   │   └── train
│   ├── ped2
│   │   ├── test
│   │   └── train
│   └── shanghaitech
│       ├── test
│       └── train
...
``` 

#### Step 4. Generate pseudo anomaly scores

```
./run1_pseudo_anomaly_scores.sh avenue
```

#### Step 5. Evaluate on each dataset

```
./run2_evaluate.sh avenue
```
