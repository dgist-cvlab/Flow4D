# Flow4D: Leveraging 4D Voxel Network for LiDAR Scene Flow Estimation (RA-L 2025)

This repository contains the code for the [Flow4D paper (RA-L 2025)](https://ieeexplore.ieee.org/document/10887254)


## Notice

**Flow4D has been integrated into [OpenSceneFlow](https://github.com/KTH-RPL/OpenSceneFlow).**
Please visit the [OpenSceneFlow](https://github.com/KTH-RPL/OpenSceneFlow) repository for the latest updates and developments.

This repo saved README, and quick core file in Flow4D for a quick reference.
The old source code branch is also [available here](https://github.com/dgist-cvlab/Flow4D/tree/source).

## Requirements

This code is based on DeFlow. <br>
Please follow the installation instructions from the [DeFlow repository](https://github.com/KTH-RPL/DeFlow).

Additionally, you need to install `spconv 2.3.6`.<br>
You can find the installation instructions here: [spconv](https://github.com/traveller59/spconv).


## Training

To train the model, use the following command:

```bash
python train.py model=flow4d lr=1e-3 epochs=15 batch_size=8 num_frames=5 loss_fn=deflowLoss "voxel_size=[0.2, 0.2, 0.2]" "point_cloud_range=[-51.2, -51.2, -3.2, 51.2, 51.2, 3.2]"
```


## Inference

To perform inference, use the following command:

```bash
python eval.py checkpoint=path_to_checkpoint av2_mode=(val, test)
```

Replace `path_to_checkpoint` with the actual path to your checkpoint file and choose either `val` or `test`.


## Gratitude
This code is based on the [DeFlow code](https://github.com/KTH-RPL/DeFlow) by Qingwen Zhang.
We extend our deepest gratitude to her.<br>
Additionally, we would like to express our sincere thanks to Kyle Vedder et al. for hosting and providing extensive support for [Argoverse2 2024 Scene Flow Challenge](https://www.argoverse.org/sceneflow.html)

