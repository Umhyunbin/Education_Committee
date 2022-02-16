# 주제 : 서울특별시의회 교육행정감사 회의록 분석       

## 1. 분석 목표    
### 1) 회의록 현황 파악     
### 2) 감사 준비 참고 자료 생성    
### 3) 교육 정책 수립을 위한 새로운 인사이트 제공         

## 2. 분석 프로세스 

### 1) 회의록 홈페이지 스크레이핑을 통한 데이터 수집
### 2) 불용어 사전 구축
### 3 - 1) 단어 빈도 분석
### 3 - 2) 위원별 단어 빈도, 발언 수 분석
### 3 - 3) 주요 키워드 분석
### 3 - 4) 감성 분석           

## 3. 분석 과정
### 1) 회의록 스크레이핑
#### - 원하는 회의록 접속. 해당 페이지에서 데이터 셋에 필요한 항목 추출.
#### - 회의록 접속 후 발언 내용을 포함한 필요 항목들 추출.
#### - 같은 회수의 모든 회의를 날짜별로 반복.
#### - 수집이 끝나면 하나의 데이터프레임으로 취합하여 csv 파일 생성.
#### 코드 : [회의록 스크레이핑](https://github.com/Umhyunbin/Education_Committee/blob/abdad102eb788933da740d9bd3cd9b3db9c7b91c/%ED%9A%8C%EC%9D%98%EB%A1%9D_%EC%8A%A4%ED%81%AC%EB%A0%88%EC%9D%B4%ED%95%91.ipynb)       

### 2) 단어 빈도 분석
#### 문장 -> 분석기 -> 명사 추출 -> 불용어 처리 -> 최종 단어 추출
#### 위와 같은 순서로 진행함.
#### 코드 : [단어 빈도 분석](https://github.com/Umhyunbin/Education_Committee/blob/5c6f7d2f48b601db2d1391f6fd707f287d58f807/%EB%8B%A8%EC%96%B4%20%EB%B9%88%EB%8F%84%20%EB%B6%84%EC%84%9D.ipynb)        

### 3) 주요 키워드 분석
#### 키워드 설정 -> 키워드 탐색 -> 문맥 추출 -> 키워드 정제
#### 위와 같은 순서로 진행함.
#### 코드 : [주요 키워드 분석](https://github.com/Umhyunbin/Education_Committee/blob/7b0fb3e182d255db067c406b2f7223c9db3d7bf8/%EB%8B%A8%EC%96%B4%20%ED%8F%AC%ED%95%A8%20%EB%AC%B8%EB%A7%A5%20%ED%8C%8C%EC%95%85.ipynb)     

### 4) 감성 분석
#### - KoBERT 모델을 이용하여 발언자의 발언을 부정, 중립, 긍정으로 분류.
#### - 학습 데이터 셋 구축을 위해 voting 방식을 통해 레이블 생성.
#### 코드 : [감성 분석](https://github.com/Umhyunbin/Education_Committee/blob/35c15035ff271cded36978d5ce2c4fe249ad0654/sentiment_classification_kobert.ipynb)      
 
#### KoBERT Github 주소 : [KoBERT](https://github.com/SKTBrain/KoBERT.git)
