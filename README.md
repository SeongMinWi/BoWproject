# BoWproject
2019-2 패턴인식 프로젝트

Topic: Image classification using Pattern Recognition

Base paper: 
[Beyond bags of features spatial pyramid matching for recognizing natural scene categories, CVPR 2006](https://inc.ucsd.edu/~marni/Igert/Lazebnik_06.pdf)

| Type | Level | features | Image size | SIFT step_size | Scaler | SVM Kernel | Accuracy|
|:----:|:-----:|:--------:|:----------:|:--------------:|:------:|:----------:|:-------:|
Single-level | 0 | 200 | 256x256 | 8 | standard | RBF | 0.40307 |
Pyramid | 2 | 200 | 256x256 | 8 | standard | RBF | 0.48877 |
Pyramid | 2 | 200 | 256x256 | 8 | standard | Precomputed | 0.54669 |
Pyramid | 2 | 400 | 256x256 | 8 | standard | Precomputed | 0.56737 |
Pyramid | 2 | 600 | 256x256 | 8 | standard | Precomputed | 0.58333 |
Pyramid | 2 | 1200 | 256x256 | 8 | standard | Precomputed | 0.61406 |
Pyramid | 2 | 1200 | 256x256 | 8 | robust+standard | Precomputed | 0.61465 |

### Reference
https://github.com/TrungTVo/spatial-pyramid-matching-scene-recognition.git
https://github.com/wihoho/Image-Recognition.git
