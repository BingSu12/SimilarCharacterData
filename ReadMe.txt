Please cite the following papers if you use the data:

1. B. Su, X. Ding, C. Liu, H. Wang, and Y. Wu, "Discriminative transformation for multi-dimensional temporal sequences," IEEE Trans. Image Processing, vol. 26, pp. 3579-3593, 2017.

2. B. Su, X. Ding, H.Wang, and Y.Wu, "Discriminative dimensionality reduction for multi-dimensional sequences," IEEE Trans. Pattern Anal. Mach. Intell., 2017.



-----------------------------------------------------------------------


"similarCharacterSet.mat" contains two .mat files: "samplenum", and "characterset".


-----------------------------------------------------------------------
"samplenum": the number of similar characters w.r.t. the seven classes, whose GBK codes correspond to:

'd7c9';
'c8d4';
'b4b9';
'f6b5';
'f9be';
'fbbe';
'b5b9';

respectively.


-----------------------------------------------------------------------

"characterset": the cell array of sample set w.r.t. the seven simialr characters.

characterset{i} is a cell array which contains samplenum(i) online character trajectories. e.g. characterset{i}{j} is the j-th online character sample of class i.

Each character sample (characterset{i}{j}) is a vector containing the trajectories of a online character sample. 

The first six elements correspond to the number of the corresponding GBK code (GBK2NUM);

The remaining elements are the [x,y] positions of each trajectory point. The format of as follows:
[x1, y1, x2, y2, ... , -1, 0, x_n, y_n, ..., -1, 0, -1, -1]

The trajectories of the strokes are stored stroke-by-stroke. Flags are added between strokes.

-1 is the ending flag of the x-coordinate of a stroke;

0 is the ending flag of the y-coordinate of a stroke;

an additional (-1 -1) is added at the end of the whole character.