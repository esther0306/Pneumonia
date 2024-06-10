# Pneumonia X-ray Binary Classification

## 프로젝트 개요
폐렴 엑스레이 이미지 분류 프로젝트입니다. 이 프로젝트에서는 의료 영상 데이터를 사용하여 폐렴 여부를 이진 분류하는 모델을 개발하였습니다.

---

## 프로젝트 설명
이 프로젝트는 다음과 같은 작업을 포함합니다:
- 데이터 전처리: X-ray 이미지 데이터셋을 불러와 전처리 작업을 수행하였습니다.
- 모델 구축: 여러 딥러닝 모델을 사용하여 분류 모델을 구축하였습니다.
- 모델 학습: 학습 데이터를 사용하여 모델을 학습시켰습니다.
- 성능 평가: 테스트 데이터를 사용하여 모델의 성능을 평가하였습니다.

---

## 현재 개선 사항
1. 모델 변경 및 하이퍼파라미터 수정 후 성능 비교
2. 모델 테스트 부분 코드 작성
3. 의료 영상 전용 데이터 증강 기법 탐색 후 적용

---

## 추후 개선 사항
1. GAN으로 데이터 증강
2. 오버피팅 줄이기 위해 Batch Normalization, Dropout 사용

---

## 사용 라이브러리 및 기술
```python
import datetime
import os
import matplotlib.pyplot as plt
import random
import numpy as np
import pandas as pd
import torch
import torch.nn as nn
import torchvision
from torchsummary import summary
from torchvision import transforms
from torchvision import datasets
from torch.utils.data import DataLoader
import torch.optim as optim
from torchvision import models
from torch.optim.lr_scheduler import ReduceLROnPlateau
from tqdm import tqdm
import seaborn as sns
from sklearn.metrics import confusion_matrix, f1_score, precision_score, recall_score
