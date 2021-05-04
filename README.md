# cassava_disease_classification
Solution for Cassava Competition 2020 at Kaggle. Korean explanation included.

## Overview
이 competition은 열대에 서식하는 카사바 나무에 발병하는 질병 4개와 건강한 상태, 즉 5가지의 class들을 분류하는 classification 문제입니다. 주어지는 이미지는 모두 600x800 사이즈이고, test set은 공개되지 않습니다. 각 파일은 훈련 코드, kaggle submission 코드, baseline 코드로 주피터 노트북 파일로 제공합니다.

데이터는 아래의 링크에서 다운받아 직접 실행하여 볼 수 있습니다. 또한 Kaggle API를 통해서 더 쉽게 다운로드 가능합니다.
```
kaggle competitions download -c cassava-leaf-disease-classification
```

구글의 EfficientnetB4로 transfer learning을 사용해 훈련하였습니다. 대회 데이터 뿐 아니라 2019년 대회의 데이터까지 merge하여 한 번에 훈련에 이용하였습니다. Image augmentation을 사용하여 더 다양한 사진에도 잘 학습하도록 하였으며, voting ensemble과 TTA를 사용하여 정확도를 높였습니다. 

결과적으로 test data 기준으로 89.5% 정도의 정확도를 보여주는 코드입니다. 

## Notebooks
* [베이스라인 코드](./for-korean-cassava.ipynb)
* [훈련 코드](./for-korean-lb-0-895-effnetb4-train.ipynb)
* [TTA 및 submission 코드](./for-korean-lb-0-895-submission.ipynb)

## Resource

* [Kaggle Competition Site](https://www.kaggle.com/c/cassava-leaf-disease-classification)
* [Cassava dataset](https://www.kaggle.com/c/cassava-leaf-disease-classification/data)
* [Leaderboard](https://www.kaggle.com/c/cassava-leaf-disease-classification/data)
