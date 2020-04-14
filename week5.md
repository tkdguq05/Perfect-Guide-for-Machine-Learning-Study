# 파이썬 머신러닝 완벽가이드 스터디 5회
20.04.13 스터디 5회   
도꼬 돈카츠 먹음, 기획팀 재홍 주임님 참여   
19시 30분 부터 시작. 


## 스터디 중 나온 질문 답변
1.	질문 : tree 알고리즘의 depth가 깊어지면 정확도가 떨어진다고 적혀 있는데, 실제 코드를 돌린 결과를 보면 무조건 score가 떨어지는 건 아니던데, 이부분은 어떻게 설명해야 할까?
   
	답변 : overfitting과 연관된 것으로 생각하면 될듯, training data에 대해서만 잘 맞추고 test data에 대해서는 잘 못 맞추니깐 정확도가 떨어진다는 표현으로 이해하였음
   
2.	질문: adaboost의 각 stump별 가중치는 어떻게 정해질까?
	
	답변: 여러 자료를 참조해보면 amount of say(최종 분류에서 해당 stump가 얼마만큼의 영향을 주는지 결정)를 활용하여 계산하는 듯함. 하지만 정확한 것은 아니므로 추후 보강 필요.
	
	참고: amount of say = $\frac{1}{2} log\frac{1-total error}{total error}$
   
## 책을 보면서 인상적인 부분
**인상적인 부분** 

- 모든 모델에는 bias-variance trade off가 존재함. 만약 variance를 통제하고 싶으면 샘플 집합의 크기 'N'을 키우면 됨.
- 한편 bagging(bootstrap + aggregating = 반복적인 복원 추출 + 결과를 모두 종합)은 그 특성상 bias는 낮고, variance는 높은 모델에 적합함. bagging은 aggregating 시 '평균'을 사용하므로 평균을 통해서 weak leaner의 variance를 통제할 수 있음
- 한편 부트스트랩(bootstrap)은 복원 추출된 표본 집합을 의미하며, 복원 추출로 인해 한번도 뽑히지 못하는 OOV 데이터가 존재할 수 있음(sklearn에서는 oov 데이터를 모델 성능 테스트에 활용함)
- 그러나 bagging의 경우 학습에 사용되는 변수들끼리의 상관관계가 높아지면, average로 인한 이점을 잃게 되는 단점이 있음.

	참고: 변수들끼리의 상관관계가 존재하면,
	
	$var[\frac{1}{n}\sum_{i=1}^{n}x_{i}]=p\sigma^2 + \frac{1-p}{n}\sigma^2$
		
	변수들끼리 상관관계가 존재하지 않으면,
	
	$var[\frac{1}{n}\sum_{i=1}^{n}x_{i}]=\frac{\sigma^2}{n}$	
	
- Bias Variance Trade off
![trade off](https://lh5.googleusercontent.com/lAbzDl1HYiYHAEuGnaUw2GdCyQzkZvjWisgNY-ZRYqvRG-X-U7f7cL_UunIF7v5q0BbUSw4CZ-1-xMXs8mvE8fbGa7ghFeEGzuwJ6wiIs64nUgJxkDNEC2JrSTUHEjViRZLdA23NLqI)
	
		
