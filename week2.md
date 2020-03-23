# 파이썬 머신러닝 완벽가이드 스터디 2회
20.03.23 스터디 2회   
19시부터 진행함 
저녁은 짜장면과 탕수육을 먹음, 탕수육 맛이 기대 이하였다. 

## 스터디 중 나온 질문 답변
1. 질문 : isna()와 isnull()의 차이?  
   답변 : python 한정, 둘의 값은 같음. pandas에서는 같은 기능을 하는 것 같다.  
  [관련 답변](https://datascience.stackexchange.com/questions/37878/difference-between-isna-and-isnull-in-pandas)

2. 질문 : 여러개의 column을 보고싶을때는?  
	답변 : df[['col1','col2']]
   
3. 질문 : 내림 차순으로 정렬하고 싶다면?  
	답변 : ascending=False 옵션을 주면 됨


## 책을 보면서 인상적인 부분
**인상적인 부분** 
- df.values.to_dict()에서  str {'dict', 'list', 'series', 'split', 'records', 'index'} 로 다양하게 사용할 수 있는 점
- groupby 후 agg 사용할 때, agg_format = {'Age':'max','SibSp':'sum','Fare':'mean'} 묶어서 사용할 수 있는 점
- apply쓰는 게 열 가져와서 처리할 때 사용한다. 사실 열 가져와서 처리하는 방법은 다양하다. for문, iterrows도 존재함. list comprehension, 병렬연산의 속도 차이 결과. for문이 가장 느림, 병렬처리가 가장 빠름. numpy 병렬처리가 pandas 병렬처리보다 빠름. .values만 붙여서 돌려도(numpy ndarray) 훨씬 빠름  
[굼뜬 pandas를 위한 다이어트 방법!](https://www.pycon.kr/program/talk-detail?id=73)
- **p.51에서 dict 객체 할당하는 흉악한 코드 발견! 이건 책에서 수정해야 할듯**
- index에 문자열 넣는 것도 가능하다는 점
- column drop할 때 Inplace=False는 반영안되는데, 이걸 같은 변수에 할당하면 메모리에서 제거되는 게 아니라, 메모리에서 추후 제거되는 점이 신기함. 
- index는 변경 불가 하다는 것
- dataframe slicing할 때, slicing으로 데이터 추출하지 않는 게 중요함
- sort_values에 inplace=True 옵션이 있는 줄 몰랐음
- lambda 쓸 때 if else만 지원하고 else if 지원 안하는 점, 이렇게 사용하고 싶으면. if else문을 여러개 사용하면 됨


 
