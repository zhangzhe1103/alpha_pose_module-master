# alpha_pose_module-master
# pose_module
- python3
## Dependencies
- https://github.com/MVIG-SJTU/AlphaPose/tree/pytorch
- torchsampe pip install -e git+https://github.com/ncullen93/torchsample.git#egg=torchsample
- pandas
- numpy
- nibabel
- tqdm
- matplotlib
- visdom


# Debug
- pytorch == 1.0
- ModuleNotFoundError: No module named 'torchsample'
```
Traceback (most recent call last):
  File "pose_module.py", line 13, in <module>
    from SPPE.src.main_fast_inference import *
  File "/home/m/workspace/method_modules/pose_module/SPPE/src/main_fast_inference.py", line 7, in <module>
    from SPPE.src.utils.img import flip_v, shuffleLR
  File "/home/m/workspace/method_modules/pose_module/SPPE/src/utils/img.py", line 4, in <module>
    from torchsample.transforms import SpecialCrop, Pad
ModuleNotFoundError: No module named 'torchsample'
```
- Solution
```
pip install -e git+https://github.com/ncullen93/torchsample.git#egg=torchsample
pip install visdom
pip install nibabel
pip install h5py  # this will be removed in the formal version
```
[Ref](https://github.com/MVIG-SJTU/AlphaPose/issues/71) https://github.com/MVIG-SJTU/AlphaPose/issues/71
