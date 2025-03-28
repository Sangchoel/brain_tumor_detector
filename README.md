# Brain Tumor Segmentation 🧠  
PyTorch 기반 **UNet** 모델을 활용한 뇌종양 CT 영상 세그멘테이션 프로젝트입니다.  
COCO 형식 어노테이션을 사용하여 마스크 생성, 학습 성능 시각화,  
TensorBoard 기록, Early Stopping 등 실전 구조로 구성되어 있습니다.

---

## 📁 프로젝트 개요

- **목표**: CT 영상에서 뇌종양 부위를 픽셀 단위로 세분화(Segmentation)
- **모델 구조**: UNet (커스텀 구현)
- **데이터 형식**: COCO format (`_annotations.coco.json`)
- **환경**: Python, PyTorch, Google Colab

---

## ⚙️ 주요 기술 스택

| 항목 | 내용 |
|------|------|
| 언어 | Python 3 |
| 프레임워크 | PyTorch |
| 모델 | UNet |
| 데이터 로딩 | COCO 포맷 파싱 (polygon → mask) |
| 시각화 | matplotlib, TensorBoard |
| 성능 기록 | F1 Score, Loss, Early Stopping |
| 로그 | `training_log.txt` 저장

---

## 🧪 핵심 기능

- ✅ COCO format 기반 마스크 생성
- ✅ Dice 기반 이진 세그멘테이션 학습
- ✅ F1 Score, Accuracy 기반 성능 평가
- ✅ TensorBoard로 학습 로그 시각화
- ✅ Early Stopping 및 최적 모델 저장
- ✅ 결과 마스크 시각화 (예측 vs 정답)

---

## 🧰 실행 방법

> Colab or Local (GPU 권장)

1. 필요한 패키지 설치  
```bash
!pip install tensorboard
# PyTorch와 TorchVision 설치 (Colab에 이미 설치된 경우가 많음)
!pip install torch torchvision

# OpenCV 설치
!pip install opencv-python-headless

# Matplotlib 설치
!pip install matplotlib

# Albumentations 설치 (선택 사항, 데이터 증강 시 유용)
!pip install albumentations
