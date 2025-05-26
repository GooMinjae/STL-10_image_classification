# STL-10_image_classification

stl-10 이미지를 사용하여 분류모델을 만드는 Kaggle Competition 프로젝트입니다.

최종 제출 Score: 86.1 %

마감 이후 성능 개선 모델 Score: 90.4 %

---

### 🔍 사용한 모델 및 기법

* Base Model: **ResNet-50**

* Regularization: **EarlyStopping, EMA (Exponential Moving Average)**

* Augmentation: **CutMix, MixUp**

* Learning Rate Scheduler: **OneCycleLR**

* Inference Trick: **TTA (Test-Time Augmentation)**

---

### ⚙️ 학습 과정 중 겪은 이슈 및 해결 경험

* 적은 학습 데이터

    STL-10은 학습 데이터 수가 비교적 적기 때문에, 다양한 Data Augmentation 기법을 적극적으로 활용하였습니다.

    특히 CutMix와 MixUp을 통해 데이터 다양성을 확보하고 과적합을 방지할 수 있었습니다.

* 일반화 성능 향상

    모델의 일반화 성능을 높이기 위해 EMA 기법을 적용했고,

    테스트 시에는 TTA(Test-Time Augmentation)를 활용하여 예측 정확도를 개선했습니다.