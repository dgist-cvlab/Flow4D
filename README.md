# Flow4D: Leveraging 4D Voxel Network for LiDAR Scene Flow Estimation

This repository contains the code for the [Flow4D paper (RA-L 2025)](https://arxiv.org/pdf/2407.07995)

## Requirements

This code is based on DeFlow. <br>
Please follow the installation instructions from the [DeFlow repository](https://github.com/KTH-RPL/DeFlow).

Additionally, you need to install `spconv 2.3.6`.<br>
You can find the installation instructions here: [spconv](https://github.com/traveller59/spconv).


## Training

To train the model, use the following command:

```bash
python 1_train_flow4D.py
```


## Inference

To perform inference, use the following command:

```bash
python 2_eval_flow4D.py checkpoint=path_to_checkpoint av2_mode=(val, test)
```

Replace `path_to_checkpoint` with the actual path to your checkpoint file and choose either `val` or `test`.


## Gratitude
This code is based on the [DeFlow code](https://github.com/KTH-RPL/DeFlow) by Qingwen Zhang.
We extend our deepest gratitude to her.<br>
Additionally, we would like to express our sincere thanks to Kyle Vedder et al. for hosting and providing extensive support for [Argoverse2 2024 Scene Flow Challenge](https://www.argoverse.org/sceneflow.html)

