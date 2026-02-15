# Colab & Kaggle 가이드

## Google Colab

### 특징
- 무료 Jupyter Notebook 환경
- 무료 GPU/TPU 사용 가능
- 구글 드라이브와 통합
- 라이브러리 설치 간단

### 장점
- 설치 과정 생략 가능
- GPU 학습 시간 제한 있지만 무료
- 직관적인 인터페이스

### 단점
- 재부팅 시 설치 파일 초기화
- 장시간 학습 시 세션이 종료 될 수 있음
- 코드 관리는 로컬이 더 편리할 수 있음

### 활용 팁
```python
# 드라이브 마운트
from google.colab import drive
drive.mount('/content/drive')

# GitHub에서 클론
!git clone https://github.com/your-repo.git
```

## Kaggle

### 특징
- 데이터셋 풍부
- 무료 GPU/TPU 제공
- 대회 참여 가능

### 데이터 활용
```bash
# Kaggle API 설정 후
kaggle datasets download -d dataset-name
```

### 장점
- 대회와 실전 문제 풀이
- 커뮤니티 공유 코드/인사이트
- 동료 학습

### 단점
- 로컬과 동기화 번거로움
- 대회 데이터는 제한적 공개

## 선택 가이드

| 상황 | 추천 |
|------|------|
| 빠른 프로토타이핑 | Colab |
| 대회 참여/데이터 탐색 | Kaggle |
| 재현성 중요 | 로컬 + GitHub |
| 팀 협업 | Colab + Drive 또는 로컬 + GitHub |
