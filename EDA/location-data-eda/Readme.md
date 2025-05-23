# 서울시 자치구별 범죄 위험도 분석 및 정책 제언

## 📊 분석 개요

### 목적
- 서울시 자치구별 범죄 발생 위험도 분석
- 데이터 기반 범죄 예방 정책 수립을 위한 근거 제시
- CCTV 등 범죄 예방 시설물의 효율적 배치 방안 도출

### 데이터
- 112 신고 출동 현황 (2023년 상반기)
- CCTV 설치 현황
- 인구 통계 데이터 (성별, 연령별, 외국인 등)

## 🔍 분석 방법론

### 1. 위험도 기반 분석
- RandomForest 기반 위험도 예측
  - Optuna를 통한 하이퍼파라미터 최적화
  - 교차 검증(5-fold)을 통한 모델 평가
- 주요 성능 지표
  - Accuracy: [실제 accuracy 값]
  - Precision: [실제 precision 값]
  - Recall: [실제 recall 값]
  - F1 Score: [실제 f1 값]
- 복합 위험도 산출
  - 인구당 범죄 발생률 (가중치: 0.35)
  - CCTV 설치 밀도 (가중치: 0.40)
  - 예측 위험 확률 (가중치: 0.25)

### 2. 클러스터링 기반 분석
- DBSCAN 알고리즘 활용 범죄 다발지역 군집화
- 클러스터별 CCTV 커버리지 분석
- 사각지대 탐지 및 우선순위 선정

## 💡 주요 분석 결과

### 1. CCTV 설치 우선순위 지역
1. 종로구 (복합 위험도: 0.72)
   - 높은 범죄율 (271.7건/인구)
   - 3개 고위험 클러스터 발견
   - CCTV 커버리지 부족 지역 존재

2. 중구 (복합 위험도: 0.69)
   - 최고 범죄율 (294.1건/인구)
   - 2개 고위험 클러스터
   - 을지로 일대 CCTV 사각지대 존재

3. 마포구 (복합 위험도: 0.61)
   - CCTV 인프라 심각 부족
   - 유동인구 대비 낮은 CCTV 밀도

### 2. 클러스터 분석 결과
- 고위험 클러스터 특성
  - 도심 상업지구 중심 군집 형성
  - 야간 시간대 범죄 집중
  - CCTV 커버리지 불균형

## 📈 정책 제언

### 1. 단기 개선방안
- CCTV 추가 설치
  - 종로구 종로3가 일대 우선 설치
  - 중구 을지로 사각지대 보완
  - 마포구 전역 CCTV 인프라 확충

- 기존 CCTV 최적화
  - 방향 및 커버각 조정
  - 야간 촬영 성능 개선

### 2. 중장기 개선방안
- 스마트 관제 시스템 도입
  - 클러스터 기반 모니터링
  - 실시간 위험도 분석
  - AI 기반 이상 행동 감지

- 통합 범죄 예방 전략
  - 여성 안심 귀갓길 확대
  - 고령자 밀집 지역 순찰 강화
  - 지역 특성 기반 맞춤형 대책

## 📋 기대효과
1. 과학적 의사결정
   - 데이터 기반 정책 수립
   - 예산 효율성 증대

2. 선제적 범죄 예방
   - 고위험 구역 중심 예방
   - 취약계층 보호 강화

3. 시민 안전 향상
   - 범죄 발생 위험 감소
   - 체감 안전도 개선