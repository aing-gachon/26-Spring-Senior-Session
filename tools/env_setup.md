# 개발 환경 세팅 가이드

## Python 버전 선택

### 권장 버전
- **3.10 이상**: 최신 기능 활용
- **3.8 이상**: 대부분의 라이브러리 지원

```bash
python --version
```

## 가상 환경 설정

### Conda
```bash
# 환경 생성
conda create -n project-name python=3.10

# 활성화
conda activate project-name

# 비활성화
conda deactivate
```

### venv
```bash
# 생성
python -m venv venv

# 활성화 (Windows)
venv\Scripts\activate

# 활성화 (Mac/Linux)
source venv/bin/activate
```

## 패키지 설치

### requirements.txt
```bash
pip install -r requirements.txt
```

### 작성 예시
```text
torch==2.0.0
torchvision==0.15.0
numpy==1.24.0
pandas==2.0.0
scikit-learn==1.2.0
```

## 환경 검증

```bash
# Python 경로 확인
python -c "import sys; print(sys.executable)"

# 설치된 패키지 확인
pip list

# GPU 확인 (PyTorch 기준)
python -c "import torch; print(torch.cuda.is_available())"
```


## 트러블슈팅

| 문제 | 해결방법 |
|------|---------|
| 패키지 버전 충돌 | 환경 삭제 후 재생성 |
| GPU 인식 안 됨 | CUDA/cuDNN 버전 확인 |
| 라이브러리 못 찾음 | pip install --upgrade pip |
