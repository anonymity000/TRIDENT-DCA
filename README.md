# TRIDENT-CrosA
This is an implementation of CrosA on the TRIDENT(baseline network)

# Data
1. Create a directory: dataset. 
2. miniImagenet: extract dataset in ./dataset/mini_imagenet  [Link](https://drive.google.com/file/d/16V_ZlkW4SsnNDtnGmaBRq2OoPmUOc5mY/view?pli=1)
3. tieredImagenet: extract dataset in ./dataset/tiered/tiered-imagenet  [Link](https://drive.google.com/file/d/1Y54Nwimfilhf245BaTnyZ7x16hnNc0B5/view)
4. CUB200-2011: extract dataset in ./dataset/cubirds200  [Link](https://drive.google.com/file/d/1hbzc_P1FuxMkcabkgn9ZKinBwW683j45/view)

# Usage
1. Create a directory: ./save. The training/testing results are saved in this directory.
2. Create a directory: ./models/mini-5,1  The trained models are copied in this directory. We have offerred the trained models.
## Train
```
python -m src.trident_train --cnfg PATH_TO_CONFIG.JSON
```
example:
```
python -m src.trident_train --cnfg ./configs/mini-5,1/train_conf.json
```

## Test

```
python -m src.trident_test --cnfg PATH_TO_CONFIG.JSON
```
Example:
```
python -m src.trident_test --cnfg ./configs/mini-5,1/test_conf.json
```
An example for cross-domain testing:
```
python -m src.trident_test --cnfg ./configs/mini-5,1/cub_test.json
```
