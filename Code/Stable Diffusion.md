'''
source /opt/share/etc/miniconda3-py39.sh
conda activate ldm
'''

Then use the following prompt:

```
python scripts/txt2img.py --prompt "An oil painting of a cozy village in a snowy mountain, it is in the evening, warm light emitting from well-crafted cabins" --plms --ckpt sd-v1-4.ckpt --skip_grid --n_samples 2
```
