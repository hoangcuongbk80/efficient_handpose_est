### Install
* Install **[PyTorch](https://pytorch.org)** and Python >= 3.7.4 and run `sh requirements.sh`.

### Dataset  
You need to follow directory structure of the `data` as below.  
```  
${ROOT}  
|-- data  
|   |-- HO3D
|   |   |-- data
|   |   |   |-- train
|   |   |   |   |-- ABF10
|   |   |   |   |-- ......
|   |   |   |-- evaluation
|   |   |   |-- annotations
|   |   |   |   |-- HO3D_train_data.json
|   |   |   |   |-- HO3D_evaluation_data.json
|   |-- DEX_YCB
|   |   |-- data
|   |   |   |-- 20200709-subject-01
|   |   |   |-- ......
|   |   |   |-- annotations
|   |   |   |   |--DEX_YCB_s0_train_data.json
|   |   |   |   |--DEX_YCB_s0_test_data.json
``` 
* Download HO3D(version 2) data and annotation files [[data](https://www.tugraz.at/institute/icg/research/team-lepetit/research-projects/hand-object-3d-pose-annotation/)][[annotation files](https://drive.google.com/drive/folders/1pmRpgv38PXvlLOODtoxpTYnIpYTkNV6b?usp=sharing)]
* Download DexYCB data and annotation files [[data](https://dex-ycb.github.io/)][[annotation files](https://drive.google.com/drive/folders/1pmRpgv38PXvlLOODtoxpTYnIpYTkNV6b?usp=sharing)] 

### Pytorch MANO layer
* For the MANO layer, we used [manopth](https://github.com/hassony2/manopth). The repo is already included in `common/utils/manopth`.
* Download `MANO_RIGHT.pkl` from [here](https://mano.is.tue.mpg.de/) and place at `common/utils/manopth/mano/models`.

### Train    
```bash  
python train.py --gpu
```  

### Test  
```bash  
python test.py --gpu --test_epoch {test epoch}  
```  