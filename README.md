# Flow4D: Leveraging 4D Voxel Network for LiDAR Scene Flow Estimation

Flow4D is a novel LiDAR-based scene flow framework that utilizes a 4D voxel network.

## Requirements

This code is based on DeFlow. <br>
Please follow the installation instructions from the [DeFlow repository](https://github.com/KTH-RPL/DeFlow).

Additionally, you need to install `spconv 2.3.6`.<br>
You can find the installation instructions here: [spconv 2.3.6](https://github.com/traveller59/spconv).


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


# Flow4D
# Flow4D
