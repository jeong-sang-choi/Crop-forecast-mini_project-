# Crop-forecast-mini_project-

🧄 마늘 수확량 예측 모델 개발
📅 프로젝트 기간
2024.02 (개인 프로젝트)
🔍 프로젝트 개요
지역별 마늘 생산 데이터를 활용하여 수확량을 예측하는 머신러닝 모델을 개발
다양한 데이터 전처리 기법과 랜덤 포레스트, XGBoost, LGBM 등의 모델을 비교 평가

🛠 문제 정의
✅ 기존 마늘 생산량 예측은 단순 평균 또는 경험적 지표에 의존 → 정확한 예측이 어려움
✅ 지역별 다양한 데이터가 존재하지만, 이상치 처리 및 데이터 정규화 필요

🚀 해결 과정
📌 데이터 수집 및 전처리
데이터셋: 마늘시군별생산정보.csv
(연도, 시군, 재배면적, 생산량, 작황 등 포함)
데이터 전처리 작업
결측치(NaN) 제거 및 "-" 값 → 평균값으로 대체
재배면적(ha), 생산량(M/T), 작황(kg/10a) 단위 변환
이상값 탐지 및 제거 (예: 비정상적으로 높은 작황량)
📌 탐색적 데이터 분석 (EDA)
지역별 마늘 작황량(kg/10a) 분포 분석
산점도(Scatter Plot), 히트맵(Heatmap) 활용하여 특징(feature) 간 상관관계 분석
로그 변환(Log Transformation) 을 통해 데이터 분포 정규화

📌 머신러닝 모델링 및 평가
모델	R² Score	RMSE	MAE
GradientBoostingRegressor	0.86	137.67	90.49
XGBRegressor	0.82	152.83	94.26
LightGBMRegressor	0.82	171.28	101.36
RandomForestRegressor	0.75	188.12	116.43
✅ Gradient Boosting 모델이 가장 높은 성능을 보임


📊 성과 및 기여도
✅ 데이터 전처리 최적화 → 이상치 제거 및 단위 변환을 통해 모델 정확도 개선
✅ Gradient Boosting 모델을 활용하여 R² 0.86 달성
✅ Feature Engineering을 통해 모델 안정성 확보
✅ Python 기반 데이터 분석 및 시각화 100% 수행

