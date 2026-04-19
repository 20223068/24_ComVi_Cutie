# Cutie+LISA: 비디오 객체 분할 정확도 향상을 위한 그림자 인식 통합 연구

## 프로젝트 개요

본 프로젝트는 기존 비디오 객체 분할 모델인 **Cutie**의 성능 한계를 극복하고자, **객체 간 중첩 문제 해결**과 **그림자 인식 기능**을 추가하는 개선 연구입니다.  
특히, 조명 기반 그림자 인식 기술인 **LISA**를 Cutie에 통합하여 영상 처리의 정밀도와 응용 가능성을 높였습니다.

>  주요 기여:
> - 겹치거나 인접한 객체 분할 정확도 향상  
> - 배경 제거 기반 객체 추적 방식 도입  
> - 그림자 인식 기술(LISA) 통합을 통한 세밀한 객체 마스크 구성  

---

## 핵심 기술 및 방법

### 1. Cutie 개선

- **기존 방식**: 픽셀 기반 + 객체 기반 혼합 VOS(Video Object Segmentation)
- **한계점**:  
  - 근접/겹쳐 있는 객체 구분 실패  
  - 그림자 미인식  
- **개선안**:  
  - 배경을 제외한 객체 마스크 추적 방식 적용  
  - 객체 수 수동 입력 기능 도입 → 명확한 추적 대상 지정 가능  

### 2. LISA 통합

- **LISA**: Light-guided Instance Shadow-object Association
- **기능**:  
  - 조명 분석 기반 그림자 추정 및 경계 감지  
  - 사용자가 그림자 포함 여부 선택 가능  
  - Cutie 결과와 병합하여 정밀한 객체+그림자 마스크 생성  

---

## 기술 스택

| 항목       | 내용                         |
|------------|------------------------------|
| 언어       | Python 3.x                   |
| 프레임워크 | PyTorch, OpenCV              |
| 주요 모델  | Cutie (2024), LISA, SSIS     |
| 실험 환경  | Google Colab Pro             |
| 데이터     | Custom video (MP4), 마스크 이미지 |

---

## 참고 문헌

- [Cutie (2024)](https://github.com/hkchengrex/Cutie)
- [STM (2019)](https://github.com/seoungwugoh/STM)
- [Instance Shadow Detection (2020)](https://github.com/stevewongv/InstanceShadowDetection)
- [SSIS (2021)](https://github.com/stevewongv/SSIS)


- [1] Cheng, H. K., Oh, S. W., Price, B., Lee, J. Y., & Schwing, A. (2024). Putting the Object Back into Video Object Segmentation.
  (https://github.com/hkchengrex/Cutie)

- [2] Oh, S. W., Lee, J. Y., Xu, N., & Kim, S. J. (2019). Video Object Segmentation using Space-Time Memory Networks.
  (https://github.com/seoungwugoh/STM)

- [3] Wang, T., Hu, X., Wang, Q., Heng, P.-A., & Fu, C.-W. (2020). Instance Shadow Detection.
  (https://github.com/stevewongv/InstanceShadowDetection)

- [4] Wang, T., Hu, X., Heng, P.-A., & Fu, C.-W. (2021). SSIS (CVPR 2021 Oral) & SSISv2 (TPAMI 2022).
  (https://github.com/stevewongv/SSIS)

---

## Contributors

- 김지유 (20223068)
- 이지윤 (20221866)
