# 📑 Simple Online and Realtime Tracking (SORT)

> **Paper Title:** Simple Online and Realtime Tracking
> **Authors:** Alex Bewley, Zongyuan Ge, Lionel Ott, Fabio Ramos, Ben Upcroft
> **Conference:** ICIP (2016)
> **Keywords:** `#Computer Vision`, `#Multiple Object Tracking`, `#Detection`, `#Data Association`

---

## 1. 📑 Abstract
* MOT(다중객체추적)의 실용적인 접근방식 탐구.
* **검출 품질**이 추적 성능에 영향을 미치는 핵심요소임을 확인, 검출기 변경만으로 추적성능 **18.9% 향상** 확인.
* 칼만 필터와 헝가리안 알고리즘의 조합만으로 online trackers SOTA 알고리즘들과 견줄 수 있음.
* 단순성으로 인해 **260Hz** 속도로 업데이트 가능하며, 이는 기존 방식보다 20배 이상 빠름.

---

## 2. 🚀 Introduction
* **Tracking-by-detection:** 매 프레임마다 객체를 검출하고 이를 B-box(Bounding box)로 표현하는 MOT 문제를 해결하기 위한 경량화된 프레임워크 제시.
* **온라인 추적:** 이전 프레임과 현재 프레임의 검출 정보만을 추적기에 제공하는 것이 목표.
* **Data Association:** 비디오 시퀀스 전체에서 검출된 객체들을 연관시키는 문제로 접근.
* **성능의 균형:** MOT 벤치마크 순위에서 발생하는 속도와 정확도의 Trade-off 관계를 극복하고 두 가지 모두 우수한 성능을 보임.
* **오캄의 면도날:** 결과가 똑같다면 과정이 단순한 것이 좋다는 법칙에 따라 외형 특징(Appearance)은 제외하고, 바운딩 박스의 위치와 크기만 연관을 위해 사용.
* **핵심 알고리즘:** 움직임 예측을 위한 **칼만 필터(Kalman Filter)**와 데이터 연관을 위한 **헝가리안 방법(Hungarian method)** 채택.
* **검출기 성능 :** 검출기의 성능이 좋으면 추적 알고리즘이 단순해도 됨을 강조. Faster R-CNN 같은 고성능 CNN 검출기를 쓰고 알고리즘을 최적화함.

---

## 3. 📚 Literature Review
* 다중객체 추적은 과거 MHT(Multiple Hypothesis Tracking), JPDA(Joint Probabilistic Data Association) 필터를 사용하여 해결되어 왔음.
* 하지만 객체 할당에 대한 불확실성이 높을 때 결정을 뒤로 미루는 방식은 객체 수가 기하급수적으로 증가할 때 실시간 응용에 부적합함.
* **Geiger 등의 방법:** 헝가리안 알고리즘을 2단계 프로세스로 사용(프레임 간 연관으로 tracklets 형성 후 다시 연관). SORT 알고리즘은 이 방식의 추적 구성요소에서 영감을 받음.

---

## 4. ⚙️ Methodology
핵심 요소: 검출(Detection), 객체 상태를 다음 프레임으로의 전파(Propagating), 검출값과 기존 객체의 연관(Associating)

### 4.1 Detection
* **Faster R-CNN 프레임워크 사용:** 2단계로 구성된 End-to-End Framework.
* 첫 번째 단계에서 특징을 추출하여 영역을 제안하고, 두 번째 단계에서 제안된 영역 내의 객체를 분류.
* 출력 확률이 50%보다 큰 보행자 검출 결과만을 추적 프레임워크로 전달.

### 4.2 Estimation Model
* 각 타겟의 상태 모델링: $x = [u, v, s, r, \dot{u}, \dot{v}, \dot{s}]^T$
    * $u, v$: B-box의 중심 좌표
    * $s$: B-box의 넓이(Scale)
    * $r$: 가로세로 비율(Aspect ratio)
    * $\dot{u}, \dot{v}, \dot{s}$: 각 성분의 속도(Velocity)
* 검출값이 타겟에 연관되면 칼만 필터를 통해 속도 성분을 최적으로 예측.
* 연관된 검출값이 없는 경우 보정 없이 선형 속도 모델만을 사용하여 예측.

### 4.3 Data Association
* **IOU(Intersection-over-Union):** 두 박스가 얼마나 겹치는지를 나타내는 지표.
* SORT는 많이 겹칠수록 같은 Object일 확률이 높다고 가정하여 헝가리안 알고리즘으로 최적의 일대일 매칭 수행.
* $IOU_{min}$보다 낮은 값들은 매칭에서 제외.

### 4.4 Creation and Deletion of Track Identities
* 새로운 ID 생성 및 기존 ID 소멸 기준 설정.
* $IOU_{min}$ 이하의 검출값은 새로운 객체로 간주하여 초기화(속도는 0으로 설정).
* **수습 기간(Probationary period):** False Positives(노이즈) 방지를 위해 일정 기간 검출값과 연관되어야 함.
* **$T_{Lost}$ 설정:** 프레임 동안 검출되지 않으면 종료. 본 논문 실험에서는 **1**로 지정.
* **$T_{lost}$가 1인이유 :** 1. 등속도 모델은 실제 역학을 예측하기에 부족함. 2. 객체 재식별(Re-ID)은 본 연구의 범위 밖임.

---

## 5. 🧪 Experiments
### 5.1 Metrics
* MOTA(정확도), MOTP(정밀도), MT, ML, ID sw, Frag 사용.
* MOTA ~ MT까지는 높을수록 좋고, 나머지는 낮을수록 좋음.

### 5.2 Performance Evaluation
* 당시 사용됐던 Online Trackers 중 가장 높은 정확도(MOTA) 및 가장 낮은 ML(Most Lost) 달성.

### 5.3 Runtime
* Intel i7 2.5GHz 기기에서 **260Hz**로 실행되어 압도적인 속도 증명.

---

## 6. 🧐 Conclusion
* 추적 품질이 검출 성능에 크게 의존함을 입증.
* 단순한 알고리즘(Kalman + Hungarian)만으로도 SOTA급 추적 품질을 달성할 수 있음을 보여줌.
* 다만, 장기 폐색(Occlusion)을 처리하기 위한 객체 재식별 문제가 남아있음.

---

## 7. 📝 Review

### 내 연구와의 비교 및 적용 방안
* **한계점:** 내 연구에서는 15°씩 Pan-tilt를 하나의 축에 있는 모터로 조절하기에 칼만 필터나 단순 선형 모델로 예측이 불가능함(추가적인 미세보정이 필요함).
* **적용 방안:** 결국 이전 상태를 보고 비교하거나 예측을 잘하는 것이 핵심인데, 높은 수준의 예측 모델을 직접 만들기보다는 **데이터 연관(Data Association)**을 강화하는 방향이 현실적임.
* **다음 단계:** 본 논문에서 비교 및 참고했던 **Geiger 등의 방법**을 읽어보고, 끊어진 궤적(tracklets)을 다시 연결하는 로직을 분석해볼 필요가 있음.

---

## 8. 💡 New Knowledge & Terms
* **오캄의 면도날(Occam's Razor):** 어떤 사실에 대한 설명들 중 동일한 조건이라면 가장 단순한 것이 정답일 확률이 높다는 원칙.