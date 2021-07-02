### 독립변수와 종속변수

 * 독립변수(independent variable) : 회귀분석에서 원인이 되는 변수 

   * 설명변수(explanatory variable), 예측변수(predictor variable), 회귀변수(regressor)
   * 독립적(다른 변수에 영향을 받지 않음) - 종속변수에 영향을 주는 변수
   * 연구자가 의도적으로 조작시키는 변수 

   

 * 종속변수(dependent variable) : 회귀분석에서 결과에 해당하는 변수

   * 설명된 변수(explained variable), 반응변수(response variable), 피회귀변수(regressand)
   * 독립변수의 변화에 따라 달라지는 변수
   * 연구자 입장에서는 독립변수의 변화를 통해 달라지는 결과가 무엇인지 알고 싶은 변수

   

 * 회귀분석(regression) : 인과관계가 있을 것으로 예상되는 여러 변수의 관계를 예측하는 분석 기법

   * 인과관계는 상관관계에 포함
     - 상관관계가 있다고 인과관계인 것은 아님(상관관계와 인과관계를 혼동하지 않도록 주의)
   * 독립변수와 종속변수는 인과관계에 있음
   * (종속변수) = f(독립변수)
     * 독립변수가 하나일 경우 단순회귀분석, 복수일 경우 다중회귀분석



#### 예시 ) 타이타닉 호 생존 여부 예측

* 타이타닉 모델 데이터 구조

  | 변수        | 의미                                              |                                                         |
  | ----------- | ------------------------------------------------- | ------------------------------------------------------- |
  | PassengerId | 승객 고유 번호                                    |                                                         |
  | Survived    | 생존 여부                                         | 0: 사망 <br />1: 생존                                   |
  | Pclass      | 티켓 클래스                                       | 1: 1등석 <br />2: 2등석 <br />3: 3등석                  |
  | Name        | 성명                                              |                                                         |
  | Sex         | 성별                                              | Female, Male                                            |
  | Age         | 나이                                              |                                                         |
  | SibSp       | 동반한 형제자매(Sibling) 또는 배우자(Spouse)의 수 |                                                         |
  | Parch       | 동반한 부모(Parent) 또는 자녀(Child)의 수         |                                                         |
  | Ticket      | 티켓 고유 번호                                    |                                                         |
  | Fare        | 티켓 요금                                         |                                                         |
  | Cabin       | 객실 번호                                         |                                                         |
  | Embarked    | 탑승한 항구명                                     | S: Southampton, <br />C: Cherbourg, <br />Q: Queenstown |

  

* train data와 test data로 구분되어 있는데 test data에는 Survived가 빠져 있음

  * test data에서 분석을 통해 생존 여부를 추정해야 하는 Survived가 종속변수에 해당

  * (Survived) = f(Pclass, Sex, Age, SibSp, Parch, Fare, Cabin, Embarked, ...)

    * 독립변수가 많다고 해서 무조건 설명력이 높은 회귀모델은 아님

    

------

Reference:

* 타니아이 히로키 저, 츠지 신고 감수, 권기태 옮김, 「누구나 파이썬 통계분석」, 한빛아카데미, 2020

* 정보통신기술용어해설 http://www.ktword.co.kr/abbr_view.php?m_temp1=1916&id=1421&nav=2
* 제1부 통계학의 기초와 자료 분석 http://www.kmooc.kr/assets/courseware/e17442a0ad9c55202e4bd

* 이호준, 김진환, 김진, 김혜원, 김유진, 차경림, 김영희, 「캐글 데이터로 살펴보는 데이터분석 With Python & SAS」 , 위니브 https://www.notion.so/With-Python-and-SAS-f2b8927d9b054fa5bd12b24e2da7ffb7
