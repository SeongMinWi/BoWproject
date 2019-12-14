# BoWproject
2019-2 패턴인식 프로젝트

### Topic
Image classification using Pattern Recognition


### Base paper
* [Beyond bags of features spatial pyramid matching for recognizing natural scene categories, CVPR 2006](https://inc.ucsd.edu/~marni/Igert/Lazebnik_06.pdf)


### Dataset - Caltech 101
101종류의 class, class당 영상 30장
* Link: http://www.vision.caltech.edu/Image_Datasets/Caltech101/


### Environment
1. Python 3.x
2. numpy
3. opencv-contrib-python 3.4.2.16 (SIFT 알고리즘이 특허로 등록되어있어 opencv 특정 버전만 사용가능)
4. sklearn
5. scipy
6. kmc2


### Bag of Words
1. Extract SIFT descriptor
```
sift = cv2.xfeatures2d.SIFT_create()
kp = [cv2.KeyPoint(x,y,Step_size) for y in range(0, image_gray.shape[0], Step_size) for x in range(0, image_gray.shape[1],   Step_size)]
keypoint, des = sift.compute(image_gray, kp)
```

2. Generate Codebook (K-means clustering)
3. Generate Histogram of codeword
4. Train classifier (Support Vector Machine)

![Alt text](https://t1.daumcdn.net/cfile/tistory/2171564C5302BF5F27)

### Spatial Pyramind Matching
+ Pyramid Match Kernel
+ Spatial Matching Scheme 

![Alt text](https://t1.daumcdn.net/cfile/tistory/2407DA485302FE6009)


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
* https://github.com/obachem/kmc2
