## 1) RFM 분석
### 개요
천재교육 온라인 쇼핑몰의 판매 현황 데이터를 분석하여 RFM 분석을 수행했습니다. 이 분석을 통해 고객의 구매 패턴을 파악하고, 특정 고객의 행동에 따른 판매 전략을 세울 수 있습니다.

### 가설
세 가지 주요 가설을 설정하고 분석을 진행했습니다:

1. RFM 등급이 판매금액과 연관성이 있다.
- 판매금액에 따른 분류를 통해, RFM 지표와 판매금액 간의 상관관계를 파악.
- 카이제곱 검정을 이용해 RFM 등급과 판매금액의 관계를 분석.

2. 월, 연도별 판매금액의 차이가 있다.
- 월별 및 연도별 판매금액 추이를 확인하여 시즌성 및 특정 기간에 따른 판매 변화를 분석.
- 할부 및 처리상태를 고려한 순수익 계산으로 실제 수익 변동을 파악.

3. 결제 방법과 판매금액이 연관성이 있다.
- 결제 방법을 기준으로, 결제 방법과 판매금액 간의 연관성을 분석.
- Boxplot을 통해 결제 방식에 따른 판매금액 분포를 시각화했으며, 카이제곱 검정을 활용해 두 변수 간의 관계를 검토.


## 2) 텍스트 분석

### 개요
- 웹크롤링 기법을 이용하여 두 회사의 리뷰를 분석
- 웹크롤링 기법을 이용해 수집한 리뷰를 텍스트 분석을 통해 교육 회사인 아이스크림에듀와 천재교육의 리뷰를 비교했습니다. 이 분석은 Okt 형태소 분석기를 사용하여 리뷰 데이터를 전처리하고, 별점에 따른 이진 분류를 통해 감정 분석을 수행.
- 워드클라우드로 시각화

### 데이터 개요
- Tselpha 연수원: 9개의 feature와 155개의 샘플로 이루어져 있음.
- Is-cream: 9개의 feature와 2675개의 샘플로 이루어져 있음.

### 분석 절차
- 형태소 분석기인 Okt와 불용어 처리를 통해 리뷰 내용을 전처리하고, 이를 바탕으로 교육 회사들의 리뷰를 비교.
- 별점 기준 이진화 후, 감정 분석을 통해 긍정적/부정적 감정을 구분하였으며, 각 리뷰의 개선 사항을 도출.

### 참고
자세한 분석 과정과 코드, 보고서는 첨부된 파일을 통해 확인.

## 3) 프롬프트 엔지니어링

### 개요
- 프롬프트 엔지니어링을 사용하여 독후감 첨삭 프로그램을 개발. 
- 이 프로그램은 사용자가 작성한 독후감에서 느낀점을 식별하고, 각 문장에 포함된 감정 키워드를 추출하며, 각 문장에 대한 개선 사항을 제시하는 작업을 수행.

### 목적
주어진 독후감 텍스트에서 글쓴이의 느낀점을 포함한 문장을 식별하고, 감정 키워드를 추출.
각 문장의 개선 사항을 제시하여, 독후감의 품질을 향상시키는 것이 목표입니다.

### 프로그램 설계
- 모델 : ChatGPT OpenAI모델 사용
- 입력 데이터: 독후감 3개를 texts 변수에 저장 (제목과 함께 저장)
- 결과 저장: 각 독후감에 대한 결과를 results 리스트에 저장
- 반복 처리: texts 내용을 user_prompt로 설정하여 OpenAI API를 통해 시스템 프롬프트와 유저 프롬프트를 사용하여 채팅 컴플리션 생성
- 결과 출력: 3개의 독후감 첨삭 결과를 출력합니다.
