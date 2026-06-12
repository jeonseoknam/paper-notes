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

### Loosely-coupled localization fusion system based on track-to-track fusion with bias alignment
- **분야**: Localization, Sensor Fusion, Track-to-Track (T2T) Fusion, Kalman Filter
- **출처**: IEEE ICRA 2023 ([link](https://ieeexplore.ieee.org/document/10160567))
- **내용**: 다중 측위 시스템을 느슨하게(loosely-coupled) 융합할 때 각 시스템이 갖는
  slow-varying bias를 무시하면 추정이 왜곡되는 문제를 다룬다. (1) 칼만 필터로 reference 대비
  target의 bias 차이를 추정·정렬한 뒤, (2) bias-aligned 추정치를 T2T 기법(KF / CU / CI / Split CI)으로
  융합해 일관성 있고 정확한 측위 결과를 얻는다.
