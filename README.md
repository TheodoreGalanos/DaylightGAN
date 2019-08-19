# DaylightGAN
Daylight prediction pipeline, using Rhinoceros 3D, Grasshopper 3D, Ladybug Tools and pyTorch

# Downloading the Daylight Autonomy (DA) dataset

If you wish to train your own model on the DA dataset, you can download the files from this location (https://drive.google.com/open?id=1Nvw_5GrjdpDhlbf6ME32RBIAkjuAyfc4). Extract the files in cycleGAN/datasets folder.

# Pretrained model

You can download the Daylight Autonomy (DA) pretrained model from this location: https://drive.google.com/open?id=16i-ZdF8BeFZ0D-BFfinrNjeiCmtRRSSO. Extract the files into cycleGAN/checkpoints folder.

# Training your own model on the DA dataset

After extracting the dataset you can train your own model by running:

```python
python train.py --dataroot ./datasets/da --name p2p_512 --checkpoints_dir ./checkpoints/da --model pix2pix --batch_size 4 --norm instance --init_type kaiming --dataset aligned --direction AtoB --load_size 512 --crop_size 512 --no_flip --display_winsize 512 --gan_mode lsgan --lr_policy linear --netG unet_512 --netD n_layers --n_layers_D 4
```
