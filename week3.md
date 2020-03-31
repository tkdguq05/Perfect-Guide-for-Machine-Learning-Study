# 파이썬 머신러닝 완벽가이드 스터디 3회
20.03.30 스터디 3회   
19시부터 진행하려고 했는데 족발이 옴  
지난 주 먹은 중국집보다 훨 나았음, 20시부터 시작 


## 스터디 중 나온 질문 답변
1. 질문 : 벡터 정규화에서 밑 부분에 루트 왜 씌움?
   답변 : 노름 개념을 이용한 듯, 유클리드 놈으로 나눠주었음
  

2. 질문 : 왜 StandarScaler를 사용하나, 왜 선형 회귀에 정규분포를 가정해야 하나
	답변 : $y=ax+\epsilon$, $\epsilon$에 대한 가정이 정규분포를 따름
   
3. 질문 : MinMaxScaler와 StandardScaling 언제 사용해야하는가?
	답변 : 보통 사용하려는 모델이 선형인 경우 StandardScale, 데이터 분포가 가우시안 분포가 아니면 minmax

4. 질문 : 그럼 왜 전처리 할때 로그 취하고 역수취하고 그런거지?  
	답변 : 정규화 하려고 하는 것
	
	
```math
SE = \frac{\sigma}{\sqrt{n}}
```
	
	
	


## 책을 보면서 인상적인 부분
**인상적인 부분** 
- StratifiedKfold
- cross_validate보다 cross_val_score가 낫다
- 절대 까먹지 말아야 할 것, 스케일링 할 때. fit은 한번만 해야한다. test 데이터 넣을 때는 transform, 
- 가능하다면 전체 데이터의 스케일링 변환을 적용하고 학습과 테스트 데이터 분리
- 여의치 않다면 fit() 또는 fit_transform()을 적용하지 않고 학습데이터로 이미 fit된 scaler객체를 이용해 transform() 변환
- tree계열은 수치에 영향을 받지 않으므로, label encoding을 써도 된다.


 
