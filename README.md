# Charge transition line detection for autotuning of quantum dots
## Motivation
We provide the dataset on which small feed-forward neural networks are trained for the detection of charge transition lines in stability diagrams of solid-state quantum dot experiments in [[1]](#1). Synthetic training data is provided for different sizes of patches for which the neural network classifier decides if a transition line is present or not.

## Data structure
The folder ```Training_data``` contains subfolders with data for various patch sizes of <img src="https://render.githubusercontent.com/render/math?math=L\times L"> pixels, named ```patch_{L}_{L}```.
The training dataset consists of 80,000 patches, all come together with ground truth data. The data is provided in ```data.txt```, and the ground truth in ```truth.txt```.
The data files contain NumPy arrays of size <img src="https://render.githubusercontent.com/render/math?math=80000\times L\times L">. The first dimension counts the individual patches in the dataset, while the second and third dimension index the pixels in the patch, providing a binary value for each pixel. The corresponding truth files are one-dimensional arrays of size <img src="https://render.githubusercontent.com/render/math?math=80000"> and contain a single number per patch which is 0 if no transition line is present and 1 otherwise.
All files can be loaded in Python via ```nump.load('data.txt')``` and analogously for the truth files.

## References
<a id="1">[1]</a>
Czischek et al. (2020)
arXiv.....
