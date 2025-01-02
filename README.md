# 마트 쇼핑 도우미 챗봇 (SmartShopper)

![alt text](<DALL·E 2025-01-02 14.51.51 - A minimalistic and modern depiction of a shopping assistant chatbot service called 'SmartShopper' for smartphones. The image features a smartphone wit.webp>)

## 서비스 개요
### 1. 서비스가 해결하려는 문제점(Problem Statement)
마트에서 물건을 구입할 때, 다른 마트의 가격정보를 비교하여 의사결정을 내리기 어렵다.

### 2. 제공하고자 하는 주요 기능 및 가치  
- 실시간 가격 비교 및 가성비 평가
- 할인 정보 제공

### 3. 타겟 사용자와 예상 사용 시나리오  
타겟 사용자 : 가격 민감도가 높은 일반 소비자 및 주부  
예상 시나리오 : 사용자가 특정 상품의 가격을 입력하거나 검색하면, 최적의 가격과 가성비 분석 결과를 제공  

<br>

## 목표 및 기대효과
### 서비스 목표
- 사용자에게 실시간 가격 정보와 가성비 분석을 제공하여 현명한 소비를 지원  
- 마트별 할인 정보를 제공하여 사용자 선택의 폭을 넓힘  

### 기대효과
- 가성비 높은 구매 경험 제공  
- 합리적인 소비 문화 정착과 마트의 경쟁력 강화 지원  

<br>

## 타겟 사용자

|구분|내용|
|-|-|
|예상 사용자 유형|일반 소비자, 쇼핑 애호가, 주부, 대학생 등|
|주요 요구사항|실시간 가격 비교, 가성비 분석|

<br>

## 데이터 소스 및 형식
### 원천데이터 소스
- 공공데이터 [한국소비자원_생필품 가격 정보_20241220] 활용  
https://www.data.go.kr/data/15083256/fileData.do

### 원천데이터 형식
- 정형 데이터 : JSON    

<br>

## RAG 파이프라인 설계
|구분|내용|
|-|-|
|데이터 최적화|chunk size : 100, Overlap : 100|
|벡터 DB|Pinecone|
|임베딩 모델|OpenAI Embeddings|
|하이퍼 파라미터|top-k = 4, 유사도 임계값 = 0.7|
