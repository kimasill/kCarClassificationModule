
## kCarClassificationModule

> YOLOv5 🚀 is a family of compound-scaled object detection models trained on the COCO dataset, and includes simple functionality for Test Time Augmentation (TTA), model ensembling, hyperparameter evolution, and export to ONNX, CoreML and TFLite.

> -- YoloV5 official documents <br>
> &nbsp;&nbsp;&nbsp; [Pytorch_YoloV5](https://pytorch.org/hub/ultralytics_yolov5/)
<br/> 
<br/>


## Overview
차종인식 분류기는 방범, 교통 분석, 자율 주행 등 다양한 분야에 활용될 수 있다.
이를 위해서 AI-HUB 에서 제공하는 KCars 데이터셋을 사용하고, 이미지 데이터 학습에
적합한 물체인식 네트워크 중 R-CNN(Region Convolution Neural Network) 방식의
훈련을 통한 국산 차량 분류기를 생성했다. 부족한 데이터셋을 보완하기 위해 표준
라이브러리 selenium을 사용하여 크롤링 한 이미지 데이터셋을 구성하여 사용하였다.
적합한 네트워크를 찾기 위해 물체인식 네트워크를 연구하였고, 이 중 빠른 처리속도 및
높은 정확도를 나타내는 YOLO 모델을 선정하였다. 최근의 YOLO 모델은 여러 버전이
있는데, 가장 적합한 버전을 찾기 위해 버전 별로 성능 테스트를 하였고, 이를 통해
학습하는 전체 과정을 살펴보고, 다양한 형식으로 구성한 이미지 데이터에 따른 정확도를
평가함으로써 최적의 학습 모델을 제시한다.
모델을 학습시키기 위해 Imglabel 프로그램을 사용하여 네트워크에 맞는 라벨링 방식인
YOLO 방식의 BBox 라벨링을 하였다. 여러 데이터셋 버전과, 모델에 따라 다른 정확도와
성능을 평가하고, 국산 차량 인식 분류기를 위한 적합한 학습데이터를 제공하고, 효율적인
학습 방안을 제시한다.
