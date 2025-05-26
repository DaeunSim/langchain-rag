# langchain-rag

### Data
* 60 페이지 분량의 PDF 파일 (목차 제거)

### Tool
* OpenAI Key 와 ElasticSearch Key는 env 파일로 관리

### Flow
1. PDF의 각 페이지를 이미지 파일로 변환
2. ChatGPT 4-o 모델을 사용해 각 이미지에서 텍스트 추출
3. 추출한 텍스트를 ElasticSearch 데이터베이스에 저장
4. 질문 시 ElasticSearch에서 관련 텍스트를 검색하여 답변 생성

### Future Work
* 현재는 페이지 단위로 나누어져 있으나, 더 작은 단위(청크)로 쪼개서 테스트 필요
* 테이블이나 코드 등 특수 형식 텍스트에 대해 후처리 작업 필요
* score_threshold 값에 따른 답변 결과 비교 필요
