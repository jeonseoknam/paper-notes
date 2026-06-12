# Paper Notes

공부하면서 읽은 논문을 기록해두는 개인 아카이브입니다.
각 항목은 **제목 · 연구 키워드(분야) · 핵심 주제 2~3줄**로 간단히 정리합니다.

---

## 기록 양식

```markdown
### <논문 제목>
- **분야**: 키워드1, 키워드2
- **출처**: 학회/저널, 연도 ([link](url))
- **내용**: 핵심 주제와 기여를 2~3줄로 요약.
```

> 새 논문은 **목록 맨 위(최신순)** 에 추가합니다.

---

## 목록

### ORB-SLAM3: An Accurate Open-Source Library for Visual, Visual–Inertial, and Multimap SLAM
- **분야**: Visual SLAM, Visual-Inertial SLAM, Multi-Map SLAM, Localization, Bundle Adjustment
- **출처**: IEEE Transactions on Robotics, 2021 ([link](https://doi.org/10.1109/TRO.2021.3075644))
- **내용**: monocular/stereo/RGB-D 카메라와 IMU를 모두 지원하는 통합 visual·visual-inertial SLAM
  라이브러리. MAP 추정 기반 IMU 초기화와 여러 sub-map을 관리·병합하는 Atlas(multimap) 구조로,
  추적 실패·재방문 상황에서도 robust한 재localization과 높은 정확도를 달성한다.

### ORB-SLAM2: An Open-Source SLAM System for Monocular, Stereo, and RGB-D Cameras
- **분야**: Visual SLAM, Localization, Loop Closing, Bundle Adjustment
- **출처**: IEEE Transactions on Robotics, 2017 ([link](https://doi.org/10.1109/TRO.2017.2705103))
- **내용**: monocular·stereo·RGB-D 카메라를 모두 지원하는 오픈소스 SLAM 시스템. full bundle
  adjustment 기반 loop closing과, 맵을 고정한 채 추적만 수행하는 경량 localization 모드를 제공하며,
  다양한 공개 데이터셋에서 실시간으로 동작함을 보였다.

### ORB-SLAM: A Versatile and Accurate Monocular SLAM System
- **분야**: Monocular Visual SLAM, ORB Features, Loop Closing, Relocalization
- **출처**: IEEE Transactions on Robotics, 2015 ([link](https://doi.org/10.1109/TRO.2015.2463671))
- **내용**: ORB 특징을 tracking·mapping·loop closing·relocalization 전 과정에 일관되게 사용하는
  monocular SLAM. covisibility graph 기반 local map과 survival-of-the-fittest 방식의 keyframe/point
  선택 전략으로, 넓은 환경에서도 정확하고 robust하게 동작한다.

### 3-D Point Cloud Map Compression for Connected Intelligent Vehicles
- **분야**: Point Cloud Map, Map Compression, Localization, Connected/Autonomous Vehicles, Edge Computing
- **출처**: IEEE Internet Computing, 2024 ([link](https://doi.org/10.1109/MIC.2023.3342793))
- **내용**: 저사양 차량이 PCD(3-D point cloud) 맵으로 정확히 측위할 수 있도록, 엣지 서버에서 맵을
  압축·맞춤 제공하는 framework를 제안한다. 각 경로 waypoint에서 voxelization과 localizability 개념을
  결합한 path-aware 압축으로, 요구 측위 성능을 만족하면서 서버·차량의 연산량을 크게 줄인다.

### Localization Fusion Framework Based on Track-to-Track Fusion With Bias Correction
- **분야**: Localization, Sensor Fusion, Track-to-Track (T2T) Fusion, Split Covariance Intersection (SCIF), Bias Estimation
- **출처**: IEEE Transactions on Industrial Informatics, 2025 ([link](https://doi.org/10.1109/TII.2024.3449993))
- **내용**: loosely-coupled 측위 융합에서 각 시스템의 slow-varying bias를 다루는 framework. (1) 칼만
  필터로 reference 대비 target의 bias를 추정해 공통 bias로 정렬하고, (2) 시스템 간 독립성과 상관을 함께
  고려하는 SCIF로 융합해 fusion consistency를 보장한다. 시뮬레이션과 실제 도심 환경에서 검증.

### Loosely-coupled localization fusion system based on track-to-track fusion with bias alignment
- **분야**: Localization, Sensor Fusion, Track-to-Track (T2T) Fusion, Kalman Filter
- **출처**: IEEE ICRA 2023 ([link](https://doi.org/10.1109/ICRA48891.2023.10160567))
- **내용**: 다중 측위 시스템을 느슨하게(loosely-coupled) 융합할 때 각 시스템이 갖는
  slow-varying bias를 무시하면 추정이 왜곡되는 문제를 다룬다. (1) 칼만 필터로 reference 대비
  target의 bias 차이를 추정·정렬한 뒤, (2) bias-aligned 추정치를 T2T 기법(KF / CU / CI / Split CI)으로
  융합해 일관성 있고 정확한 측위 결과를 얻는다. 시뮬레이션 기반 검증이 수행되었다.
