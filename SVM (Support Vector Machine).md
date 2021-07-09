## SVM (Support Vector Machine)

기계학습에서 패턴 인식, 자료 분석을 위한 지도 학습 모델로 결정 경계(Decision Boundary)를 정의하기 위한 모델

<img src="C:\Users\myhkj\Downloads\Svm_max_sep_hyperplane_with_margin.png" alt="Svm_max_sep_hyperplane_with_margin" style="zoom: 33%;" />

- 결정 경계(Decision Boundary) : 데이터가 가지고 있는 두 종류 이상의 다른 속성을 분류하는 기준
  - 2차원(line), 3차원(plane), 3차원 초과 다차원(hyperplane)
  - 서로 다른 속성(feature)에 속하는 데이터로부터 가장 멀리 떨어져 있는 경계이자 데이터를 가장 잘 설명하는 경계(best hyperplane)

- 마진(margin) : 결정 경계와 서포트 벡터(support vector) 사이의 거리
  - 서포트 벡터(support vector) : 결정 경계와 가장 가까운 데이터이자 마진에 걸쳐 있는 데이터
  - 마진의 간격이 좁을수록 허용하는 이상치(outlier)의 범위가 적다는 의미
    - 하드 마진(hard margin) : 이상치를 허용하는 기준을 까다롭게 설정하여(마진에 포함된 이상치가 적음) 간격이 좁은 마진
      - 학습 데이터의 이상치에 대한 기준이 깐깐한 경우 자칫하면 오버피팅(overfitting) 문제 발생
    - 소프트 마진(soft margin) : 이상치에 대한 기준이 상대적으로 너그러워(마진 내에 이상치가 상대적으로 포함되는 것을 허용하여) 간격이 넓어진 마진
      - 이상치를 허용하는 범위가 너무 넓어지면 데이터에 대한 학습이 부족하여 언더피팅(underfitting) 문제가 발생하여 분석 모델의 정확도 감소
    - SVM 모델이 오류를 어느 정도 허용하는지는 파라미터(C)를 통해 지정(scikit-learn)
      - C값이 클수록 하드 마진에 근접
- 오버피팅(overfitting)과 언더피팅(underfitting)
  - 오버피팅(overfitting) : 과적합이라고도 하며 학습 데이터에 지나치게 의존하여 분석 모델이 새로운 데이터를 포함한 분석에서는 설명력이 떨어지는 문제가 발생할 수 있음
    - 이를 해결하기 위한 방법 중 하나가 교차 검증(cross validation)으로 데이터의 일부는 훈련용(train)으로 나머지는 테스트용(test)으로 사용
  - 언더피팅(underfitting) : 결정 경계를 정할 만큼 충분히 데이터에 대한 학습이 이루어지지 않은 경우로 
- 새로운 데이터가 분석에 포함되면 주어진 데이터를 바탕으로 해당 데이터가 이 모델에서 어느 카테고리에 속할지 결정하여 분류



SVM 파이썬 라이브러리

- scikit-learn (Window, Mac OS X, Linux)
- PyML (Mac OS X, Linux)
- LIBSVM (Window, Mac OS X, Linux)



활용 예시
- 이미지 분류
- 손글씨의 특징 인지 



------

Reference:

위키피디아, 서포트 벡터 머신 설명 [link]( https://ko.wikipedia.org/wiki/%EC%84%9C%ED%8F%AC%ED%8A%B8_%EB%B2%A1%ED%84%B0_%EB%A8%B8%EC%8B%A0)

아무튼 워라밸, '서포트 벡터 머신(Support Vector Machine) 쉽게 이해하기' [link](http://hleecaster.com/ml-svm-concept/)

아무튼 워라밸, '머신러닝 오버피팅의 개념과 해결 방법' [link](http://hleecaster.com/ml-overfitting/)

Apensia의 상상 작업소, '오버피팅(Overfitting)과 언더피팅(Underfitting) 및 해결방법' [link](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=dhstar914&logNo=221272078843)

BioinformaticsAndMe, 'Support Vector Machine(SVM)' [link](https://bioinformaticsandme.tistory.com/304)

Thales Sehn Körting, How SVM (Support Vector Machine) algorithm works [link](https://www.youtube.com/watch?v=1NxnPkZM9bc)

