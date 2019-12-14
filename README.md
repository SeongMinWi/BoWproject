# BoWproject
2019-2 패턴인식 프로젝트

### Topic
Image classification using Pattern Recognition

### Base paper
* [Beyond bags of features spatial pyramid matching for recognizing natural scene categories, CVPR 2006](https://inc.ucsd.edu/~marni/Igert/Lazebnik_06.pdf)

### Dataset
* Link:(http://www.vision.caltech.edu/Image_Datasets/Caltech101/)
![alt text](https://www.google.com/url?sa=i&rct=j&q=&esrc=s&source=images&cd=&ved=2ahUKEwiS-_DOgrXmAhVQMd4KHVa7AfEQjRx6BAgBEAQ&url=https%3A%2F%2Fwww.researchgate.net%2Ffigure%2FAn-Illustrative-example-for-Caltech101-Data-Sample-from-16_fig2_320250462&psig=AOvVaw25UJaUCcmMGij4DhR8LPNz&ust=1576408815873050)

### Histogram



### Result
| Type | Level | features | Image size | SIFT step_size | Scaler | SVM Kernel | Accuracy|
|:----:|:-----:|:--------:|:----------:|:--------------:|:------:|:----------:|:-------:|
Single-level | 0 | 200 | 256x256 | 8 | standard | RBF | 0.40070 |
Pyramid | 2 | 200 | 256x256 | 8 | standard | RBF | 0.48877 |
Pyramid | 2 | 200 | 256x256 | 8 | standard | Precomputed | 0.54669 |
Pyramid | 2 | 400 | 256x256 | 8 | standard | Precomputed | 0.56737 |
Pyramid | 2 | 600 | 256x256 | 8 | standard | Precomputed | 0.58333 |
Pyramid | 2 | 1200 | 256x256 | 8 | robust+standard | Precomputed | 0.61406 |

### Reference
* https://github.com/TrungTVo/spatial-pyramid-matching-scene-recognition.git
* https://github.com/wihoho/Image-Recognition.git
