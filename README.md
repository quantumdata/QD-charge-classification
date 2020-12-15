# Charge transition line detection for autotuning of quantum dots
## Motivation
We provide the datasets on which small feed-forward neural networks are trained and tested for the detection of charge transition lines in stability diagrams of solid-state quantum dot experiments in [[1]](#1). Synthetic training and experimental test data are provided for different sizes of patches for which the neural network classifier decides if a transition line is present or not.

## Data structure
The synthetic training data and the experimental test data are stored in separate folders. Each folder contains subolders with data for various patch sizes of <img src="https://render.githubusercontent.com/render/math?math=L\times L"> pixels, named ```patch_{L}_{L}```.
The training dataset consists of 80,000 files, the test dataset consists of 2700 files. The data is provided in the ```Data``` folder, together with the ground truth in ```Truth```.
The files are numbered and the data files contain NumPy arrays of size <img src="https://render.githubusercontent.com/render/math?math=L\times L"> corresponding to the binary values of each pixel in the patch. The truth files contain a single number which is 0 if no transition line is present in the patch and 1 otherwise.
All files can be loaded in Python via ```numpy.load('{N}.txt')```, with file number N.

## References
<a id="1">[1]</a>
Czischek et al. (2020)
arXiv.....
