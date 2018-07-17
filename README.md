# landsat7-errors
Demonstrates errors in radiance values of Landsat 7, probably due to oversaturation, or maybe due to some data processing. When converted to reflectance, these errors pollute dataset and can't be removed anymore.

Run script as the following to generate figures:

```
python landsat7_overflow_errors.py --scene-dir=data --offset=1000000 --count=2000000
```

Original:
![no fix](https://github.com/gena/landsat7-errors/blob/master/fig_nofix.png?raw=true)

After a simple fix, masking out values equal 255, but also very low values:
![fix](https://github.com/gena/landsat7-errors/blob/master/fig_fix.png?raw=true)
