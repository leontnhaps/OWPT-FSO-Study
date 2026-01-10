# 📑 1. A comprehensive review of optical wireless power transfer technology

> **Paper Title:** LED-Based Optical Wireless Power Transmission for Automatic Tracking and Powering Mobile Object in Real Time  
> **Authors:** Mingzhi Zhao, Tomoyuki Miyamoto  
> **Journal:** IEEE Access (2025)
## 📝 2. Abstract
- **LD(Laser Diodes)**를 통해 원격으로 전력을 공급하는 **OWPT(Optical Wireless Power Transfer)**는 여러 이점이 있고, 학계와 산업계에서 주목하고 있음.
- **LPT(Laser Power Transfer)**는 낮은 전송 효율의 한계가 있음.
- **Optical beamforming**, **DLC(Distributed Laser Charging)**, **ADLC(Adaptive-DLC)**, **SLIPT(Simultaneous Lightwave Information and Power Transfer)**, **T2T OWPT(Thing-to-Thing OWPT)**, **HILPB(High Intensity Laser Power Beaming)**에 대해 주요하게 다룸.
- 레이저 선택, 위험 분석, **PV(Photovoltaic) cell**를 OWPT에서 어떻게 적용하는지도 다룸.

## 🚀 3. Introduction
- 모바일 기기의 보급으로 **WPT**가 부상하고 있음.
- **RF Energy harvesting**은 높은 전력을 공급하기 어려운 한계 존재.
- 전자기기를 충전하기 위한 WPT 시스템을 설계하려면 3가지 조건을 만족해야 함.
    1. 1W 이상 전력 전송
    2. 안전 보장
    3. 상용화를 위해 간단하고 비용 효율적이어야 함
- 현재 WPT 기술은 크게 2가지로 나눠짐: **EM** and **Non-EM**.
- **유도결합방식(무선충전패드)**은 충전 거리가 너무 짧아 일부 시나리오에선 제한적임.
- **RF 기반 기술**은 거리가 멀어질수록 효율이 거리의 제곱에 비례하게 감소함.
- RF는 또한 **EMI**를 일으켜 주변 전자기기에 악영향을 일으킴. 그래서 복합적인 이유로 OWPT가 주목받는 중.
- 기존 리뷰 논문과 달리 본 연구에선 최신 OWPT 기술들을 다룸.

## ⚡ 4. Optical Wireless Power Transfer
- OWPT는 전송 거리 문제를 해결할 솔루션이고, 송신부는 LED나 레이저 다이오드(LD) 같은 광원을 사용하여 전력을 빛으로 바꾸고, 수신부는 태양전지(Solar cell/PV cell)을 사용하여 빛을 다시 전력으로 바꿈.
- LED는 안전하고 저가지만 빛이 퍼져서 멀리 보내기 힘듦. 레이저는 빛이 퍼지지 않아 고효율 전송에 유리함.
- **OWPT가 RF보다 좋은 4가지 이유**
    1. 작은 수신 면적을 가진 먼 거리 장치에도 고전력을 보낼 수 있음.
    2. 유효 전송 거리가 훨씬 김. 레이저 전력은 지수 함수적으로 감소하지만, RF는 거리의 제곱에 비례하여 감소.
    3. OWPT는 EMI를 일으키지 않음.
    4. 태양전지를 수신기로 쓰기에 주위 광원으로도 에너지를 얻을 수 있음.
- OWPT는 드론이나 수중 로봇의 장기 임무를 위해서도 사용할 수 있음.

## 🏗️ 5. OWPT projects

### 📚 5.1 OWPT projects from the literature

* **5.1.1 Power and data transfer over light** : Philips Research Laboratories에서 Free space를 고려하여 원거리에서 센서와 액추에이터에 전력을 공급하고 데이터를 읽어오는 초기 시도 성공.
* **5.1.2 Laser-power aircraft** : NASA에서 IR laser 기반 항공기 비행 시연함. 940nm의 1.5kW 다이오드와 적외선 PV를 장착하여 6W 모터 구동 성공.
* **5.1.3 Autonomous rover** : 532nm 녹색 레이저 사용하여 280m 거리의 로버를 카메라로 추적하여 쏴주는 거 성공.
* **5.1.4 OWPT for smartphone charging** : IR 대역의 레이저 사용, Retroreflector를 센서로 사용하여 사람이나 물체 지나가면 시스템 차단.
* **5.1.5 OWPT system for mobile objects** : 이동 물체를 충전하는 과정을 **Dynamic OWPT (DOWPT)**라고 부름. 비가시광선을 기반으로 한 다양한 실험을 통해 시연함. 8W LED 전구를 송신기로 사용하였고 효율은 0cm에서 2%, 3cm에서 1.57% 기록.

### ⚙️ 5.2 OWPT working principle
- OWPT의 기본 구성은 송신부(광원), 수신부(태양광 패널)로 구성됨.
- 단순하고 컴팩트한 시스템 설계로 장거리 전력 전송 달성할 수 있음.
- 효율 저하 요인으로는 **조사 면적**이 중요함. 태양전지 수신 면적이 빛이 비치는 면적보다 작으면 효율 감소.
- **매질에 의한 감쇠 손실** 또한 효율 저하 요인 중 하나. 악천후 조건에서 큰 손실을 겪는데, 대기 중의 미세입자에 의해 빛이 흡수되거나 산란되는 특성 때문.
- 그 외에 조준 오차, 장애물, 이동성 등등이 우려 사항으로 꼽힘.
- 이러한 과제들을 해결하기 위해 빔 제어 시스템, Monochromatic source, 효율적인 수신기가 필수적임.
- 높은 효율을 위해서는 **Monochromatic source(단색광)**이 중요함. 이유는 PV가 특정 파장의 빛에서 효율이 잘 나오기 때문. 해당하는 파장에 맞는 광을 써야 효율이 좋음.
- 상업적인 태양전지는 GaAs와 Si 전지 2가지가 있는데, 출력 전압을 높이기 위한 해결책은 태양전지 칩을 직렬로 연결하는 것. 자체적으로 전압은 GaAs가 더 높음.

### 📐 5.3 OWPT system design
- OWPT 시스템은 작은 발산각과 작은 레이저 빔 크기 때문에, 먼 거리까지 고강도의 전력을 전달할 수 있는 장점이 있음.
- 빔이 작기에 정확하게 Pointed 되어야 함. 빔을 Steering 하기 위한 별도의 장치가 필요.
- 일부 연구에서는 Four-element PD를 사용하여 타겟의 위치를 감지하고 찾아냄.
- *Wang X et al., 2016; Lim et al., 2019* 에서는 재귀반사 거울을 사용함.
- 최근 DOWPT를 구현하기 위해 IR LED 마커, 이미지 처리가 탑재된 웹캠, 갈바노 미러를 이용한 조향 기술 사용.

## 🧩 6. OWPT components and research contributions
- OWPT 시스템 구성품에 대한 설명.
- OWPT에서는 평행광을 생성하기 위해 반도체 레이저가 적합함.
- 975nm VCSEL와 Si cell로 33%, VCSEL + GaAs로 15% 연구가 과거에 있었음.
- 최근 연구에선 940~980nm 파장의 고출력 LD를 사용하여 65%의 효율을 보고함.
- 레이저는 눈뽕 위험이 있으니, LED를 써보자는 방향이 제기됨.
- 1m 거리에서 41.7%의 태양전지 변환 효율을 보인 연구가 있음.
    - 2014년에 Fakidis는 실내용 OWPT를 연구했는데 백색 LED를 사용했을 때 수집 전력은 18.3mW, 효율이 0.1%에 불과.
    - 후속 연구에서 적색 LD를 1~5개 사용했을 때 수집 전력이 10.4mW, 효율이 0.74%에 불과.
    - 낮은 효율을 보인 이유는 태양전지와 LD 자체의 낮은 효율 때문. 태양전지 간의 Mismatch로 분석됨.
- 결론적으로 **VCSEL**이 빔 품질도 좋고, 가격도 싸고, OWPT에 가장 적합한 광원으로 평가받고 있음.

## 💡 7. LED-based IoT-assisted OWPT
- IoT 기기에서 배터리 Endurance는 주요 문제임.
- 두 가지 개선 방안이 있는데 하나는 충전 기술 개선, 다른 하나는 배터리 용량 늘리기임.
- 이런 시나리오에서 WPT를 사용하여 배터리 지속시간을 늘리는 것이 올바른 접근 방식으로 보임.
- 이전 연구에서는 휴대용 손전등처럼 설계된 OWPT 시스템이 제안되었음.
- 레이저는 pointing이 중요하지만 LED는 발산하기에 대충 비춰도 됐었음.

### 📤 7.1 Optical transmitters for IoT-assisted OWPT
- 태양전지의 최대 변환 효율은 bandgap energy의 spectrum limit 근처에서 나타남.
- GaAs는 1.424eV bandgap energy를 가지므로, 870nm보다 낮아야 함.
- 이 값을 초과하면 태양전지의 효율이 급격하게 떨어짐. 그래서 보통 850nm를 씀.
- 유의미한 전력을 얻으려면 high intensity IR LED가 필요함.
- 이전 연구에서 -40~40˚ 발산각과 1.04W의 810nm IR LED로 41.7%의 효율을 얻는 데 성공함.
- 고효율을 위해서는 적절한 렌즈 시스템도 필요함.

### 📥 7.2 Optical receivers for IoT-assisted OWPT
- 태양전지는 OWPT 시스템에서의 최고의 에너지 수집기로 간주됨. GaAs와 Si 태양전지.
- Si가 더 저렴하지만 가벼운 특성과 높은 밴드갭 에너지에 기반한 높은 효율로 GaAs가 선호됨.
- LED 파장과 매칭되는 Single-Junction GaAs가 고효율을 달성하기에 적합함.
- IoT 센서용으로는 5cm x 5cm는 너무 크고, 1.7cm x 1.7cm의 GaAs를 이용한 OWPT 시스템 시연 사례가 있음.

## 🛠️ 8. OWPT techniques

### 🔦 8.1 Optical beamforming
- Beamforming은 빛을 한 점으로 집중시키는 기술, 전송 거리와 효율을 높이는 핵심 기술.
- SLM이 Beamforming에 널리 사용됨. 하지만 SLM은 낮은 전력 처리 능력과 낮은 효율의 한계가 있음.
- 따라서 렌즈 기반 빔포밍이 고려됨. 렌즈를 사용하여 빔을 평행하게 만들고 집광시킴.

### 🕸️ 8.2 Distributed laser charging
- DLC는 여러 기기를 동시에 충전할 수 있는 기술.
- 송신기는 전용 추적 메커니즘을 사용하여 수신기를 자동으로 감지하고 추적하여 빔을 조향하여 충전.
- 안전 이슈로 DLC는 재귀반사 기반의 안전 메커니즘을 채택하고 있음.
- LOS 경로를 장애물(사람)이 막으면, 되돌아오는 반사 빔이 차단되고 즉시 레이저 방출 중단.

### 🔄 8.3 Adaptive distributed laser charging
- 기존 DLC에서 배터리 과충전이나 에너지 낭비, 안전 문제를 일으킬 수 있음.
- DLC는 WPT와 유사하며 일정한 전력을 제공.
- 흔히 쓰이는 리튬이온 배터리와 같은 배터리는 가변적인 전류와 전압을 필요로 하기에 동적인 전력 공급이 필요.
- 대안으로 **ADLC** 도입됨.
- 무선 통신에서 정보 전송을 최적화하기 위해 사용하는 Link adaptation 기술과 유사함.
- 여러 연구가 있었는데 TDMA 기반의 스케줄링 알고리즘 도입한 게 있음. 유연한 구동 전력 제어, 개별 사용자 전력 제어, 일정한 구동 전력 유지, 동시 충전, 연속 충전 기능을 제공한 사례가 있음.

### 📶 8.4 Simultaneous lightwave information and power transfer
- 기존 기능에 통신 기능 추가한 것.
- 가시광선/비가시광선 상관없이 기술 구현할 수 있음.
- SLIPT는 정보와 전력을 동시에 전송할 수 있는 장점을 제공함.

#### 🌊 8.4.1 SLIPT for IoUT
- 최근 IoUT 장치에 전력을 공급하기 위해 SLIPT가 제안됨.
- 수중 데이터 전송은 광파, 전파, 음파를 사용하여 진행되는데 일반적으로 수중 응용 분야에는 수 킬로미터를 커버할 수 있는 음향 통신을 사용함.
- 음향의 주파수 범위는 10Hz에서 1MHz임.
- 그러나 이것은 제한된 대역폭, 낮은 전파 속도, 높은 지연 시간의 경향을 띔.
- RF는 30~300Hz로 먼 거리 전파가 가능하지만, 심각한 감쇠를 겪음.
- 수중 광무선통신(UOWC)는 넓은 대역폭으로 수 Gb/s의 높은 전송 데이터를 제공함.
- 수중 매체를 논의한 것은 소수에 불과.

#### 🚧 8.4.2 Open issues in SLIPT
- SLIPT의 미해결 과제로는 무선 수중 매체를 통한 전파 효과나 배터리 수명 및 태양 전지의 대역폭과 같은 하드웨어 관련이 있음.
    1. **LOS 문제**: 결정적인 과제임. 이는 자외선 산란을 강화하여 NLOS 경로를 확립하는 방향이 있음. 하지만 자외선의 파장에 맞는 solar-blind cell이 필요함.
    2. **Beam divergence**: 기하학적 감쇠(geometrical attenuation)라고 함.
    3. **Propagation effects**: 빛이 물을 통과할 때 빛의 강도가 지수적으로 감소함.
    4. **하드웨어 과제**: SLIPT 성능의 제한 요소는 수신 부품의 대역폭. 데이터 속도에 대한 제약은 M-QAM, OFDM과 같은 변조 방식을 사용하여 완화할 수 있음. 태양전지 대신 PD를 사용하여 전력 분할 SLIPT 접근 방식 또한 존재함.

### 🦟 8.5 Fly-eye lens system for OWPT
- 파리눈 렌즈(Fly-eye lens)라는 특수 렌즈를 달아 고주파의 다중 광원을 사용하여 2m 거리에서 10W 전력을 전송한 연구가 있음.
- 20-40W의 고출력 VCSEL array 사용.
- 파리눈 렌즈를 통해 균일하게 퍼지게 할 수 있는 기능.
- 파리눈 렌즈는 이러한 특성으로 반도체 제조 장비나 프로젝터에 사용.

### 🌈 8.6 OWPT system by spatial wavelength division and distributed laser cavity resonance
- 공간적으로 분산된 레이저 시스템은 광학 충전 시스템을 위한 유망한 솔루션임.
- 이 방식에서 광 전력은 2개의 직교하는 diffraction gratings를 사용하여 2차원 FOV로 전체 전송.

### ⚡ 8.7 OWPT-based rapid charging
- 모바일 휴대용 장치에 전력을 공급하기 위한 OWPT 시스템이 제시됐었는데, 그 시스템은 광학 안테나, DC-DC 컨버터, GaAs 태양전지 등으로 구성됨.
- GaAs에 나노 구조의 광학 안테나를 심어 plasmonic electric field enhancement effect를 이용하여 충전 과정을 가속화함.
- Single-junction GaAs 태양전지는 높은 효율을 달성하면서 출력 전력을 극대화하기 위해 개발됨.
- 태양전지의 전압을 맞추기 위해 step-up DC-DC 회로 사용됨.

### 🤖 8.8 Thing-to-Thing OWPT
- 이 시스템은 빛의 흡수와 방출이라는 두 가지 작업을 모두 수행하는 단일 장치만을 배치함.
- **Perovskite**라는 특수 물질로 만든 송수신기를 덮어 놓음.
- 이 아이디어는 단방향 WPT의 한계를 제거하고 이동형 및 고정형 물체 모두 간의 양방향 OWPT를 지원함.
- 저렴한 금속 할로겐화물 페로브스카이트로 제작 가능.
- 페로브스카이트 태양전지의 최대 전력 변환 효율은 25.2%임.

### 🛰️ 8.9 High intensity laser power beaming
- HILPB 기술은 로봇, UAV, 위성과 같은 장치에 에너지를 전송할 수 있음.
- 모든 구성 요소가 end-to-end 효율성을 보장해야 함.
- 작은 크기, 높은 신뢰성, 높은 효율성이라는 특성 때문에 고출력 LD 사용.
- 송신기는 전력을 LD를 통해 단색 광선 빔으로 변환.
- 이 레이저는 beam director를 통해 태양 전지판을 향하게 됨.
- 수신기에서 광학 신호는 전력으로 변환.
- HILPB에서 시스템 성능은 변환 효율에 의해 제한됨.
- 여러 연구들이 있었는데 재밌는 건 2016년 러시아에서 PV 컨버터와 laser를 사용하여 1.5km 거리에서 휴대폰 충전 성공 사례.

## 🛒 9. Transceiver selection in OWPT
- OWPT를 가능하게 하는 레이저 및 PV 전지와 같은 하드웨어 기술 논의.
- 장치와 성능을 이해하는 것은 효율적인 OWPT 시스템을 설계하는 데 매우 중요함.

### 🎯 9.1 Laser selection
- 미국 국가 표준인 ANSI Z136.1은 광통신 시스템을 위한 레이저의 설치, 작동, 유지 관리 및 서비스에 대한 지침 제공.
- 현재 다양한 유형의 레이저가 상업적으로 이용 가능.
- 전송 매체는 적절한 파장을 가진 레이저의 선택을 요구함.
- 레이저는 모든 OWPT 시스템의 고성능을 위해 최대 에너지 전송으로 작동해야 함.
- **Duncan KJ, 2016. Laser based power transmission...** 은 상용 레이저 기술에 대해 780nm ~ 1100nm 영역이 적절하다는 보고.
- **UAV 전력 전송**에는 800, 900, 1500nm의 spectral windows가 선호됨.
- 레이저의 주요 요소는 3가지:
    1. 지향성 : 일반적으로 낮은 발산을 제공
    2. 간섭성 : 방출된 광자는 일정한 위상 간섭성을 보여줌
    3. 단색성 : 레이저 빔은 좁은 범위의 파장을 포함

| Laser type | Wavelength (nm) | Efficiency (%) |
| :--- | :--- | :--- |
| Diode 10 kW | 850 | 50 |
| Fiber 10 kW | 1060 | 25 |
| Fiber 20 kW | 1060 | 25 |
| Thin disk 25 kW | 1060 | 25 |

- 약한 레이저도 위험할 수 있어, 안전에 유의해야 함.
- LED를 제외한 다른 광원들은 낮은 전력 변환 효율을 가짐. 일부 LED는 LD보다 효율적이지만 그래도 제한적임.
- OWPT 시스템을 위한 광원은 **VCSEL**.
- OWPT는 통신용처럼 아주 정밀한 스펙이 필요 없기에 조건에 맞는 적당한 광원이 주요.

### ☀️ 9.2 PV cell selection
- 가장 전통적인 변환 기술은 thermoelectric, PV, pyroelectric 방식임.
- 위 기술 중 PV 기술이 가장 높은 효율을 제공.
- 고성능을 위해서는 온도, PV 전지 재료, 레이저 전력, 파장이 고려되어야 함.
- 이상적인 주파수를 가진 단색 광원이 이상적인 광원으로 간주.
- 흔히 구할 수 있는 Si 및 GaAs는 각각 900nm와 850nm에 가장 높은 변환 효율을 제공하고, AlGaAs는 550~600nm에서 높은 반응을 제공함.
- PV 전지는 높은 레이저 전력 강도에서 효율적으로 작동.

| | GaAs | Si | InGaAs | InGaP | CIS |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **nm** | 810 | 950 | >1000 | >1000 | >1000 |
| **efficiency (%)** | 60 | 53.4 | 28 | 27.7 ~ 40.6 | 19.7 ~ 40 |
| **intensity** | 110 | 43 | 110 | 10 ~ 23.7 | 2.6 ~ 10 |

- Si PV는 900~950nm 효율이 제일 좋지만 atmospheric absorption 문제가 있음.
- 1000nm 이상 DPSSL을 쓸 때는 InGaP나 InGaAs 같은 재료가 효율적임.
- 열이 높으면 효율이 떨어져 자외선 및 청색광의 짧은 파장을 사용하는 연구는 거의 없었음.
- 현재 상용 장치를 통하면 10~20%의 효율이 가능함. 최고 기록은 50% 정도.
- 고효율 페로브스카이트-실리콘 태양 전지는 유망한 후보로 부상.
- 그 외 다양한 물질로 연구 중임.

## ⛰️ 10. Challenges and counter measures in OWPT

### 📈 10.1 Efficiency improvement
- HILPB 시스템은 겨우 10%~20% 효율만 제공하기에, 전체적인 효율은 상업적 개발에 적합하지 않음.
- 연구원들은 PV 전지의 효율을 높이기 위해 노력 중.

### 🥽 10.2 Safety
- 레이저 기술은 병원, 사무실, 민간 기업들에서 구현되고 있음.
- 부적절한 사용은 피부와 눈에 부상을 포함한 위험을 초래할 수 있음.
- 엄격한 안전 솔루션을 설계하는 것이 중요.
- (~ 여긴 생략)

### 💬 10.3 Optical communication
- 미래에는 HILPB와 같은 LPT 기술들과 광통신이 결합될 것.
- 통신을 보장하기 위해 PV 전지를 수신기로 사용함.
- 전송되는 광자 에너지에 통신 링크를 통합하는 기술은 최첨단의 강력한 자유 공간 광통신을 도입할 것.

### 📉 10.4 Propagation losses in the optical beam
- Free space에서의 3가지 요소가 성능을 제한함.
    1. 퍼짐
    2. 바람과 온도에 의한 파면의 왜곡
    3. 광자를 산란시키거나 흡수하는 먼지와 물 입자
- 거리는 가장 큰 영향을 미치는 매개변수.
- 거리에 따른 광전력의 적절한 결정 요인인 레이저를 잘 고려해야 함.

### 🌡️ 10.5 Thermal effects on system performance
- 레이저는 더 차가운 조건에서 더 잘 작동함.
- 전력 변환 효율은 냉각 환경에서 더 좋음.
- 열은 광학 시스템의 전체적인 성능을 저하시킴.
- 열은 또한 PV 전압을 감소시킴.
- **Fan**을 통합하는 것이 또 다른 적절한 대안이 될 수 있음.

### 🎯 10.6 Pointing
- 송신기와 수신기 사이에는 정확한 지향이 있어야 함.
- 장치의 흔들림 없이 고정하기 위해서는 좋은 기계적 설계가 요구됨.
- 정확한 광학 배열에 의존하여 수신기와 송신기의 조준이 필요.

## 🏁 11. Conclusion
- WPT 기술은 여전히 초기 단계이다.
- OWPT는 이점이 많다.
- 빔 조향을 위한 추가적인 요소들이 필요하다.
- IoT의 경우 복잡성, 설치 및 유지 보수 비용 때문에 물리적 전선의 배터리는 효과적이지 않다.
- OWPT는 이 충전 메커니즘의 유망한 대안이다.
- OWPT 짱!

## 🧐 12. Review
**내 연구에서의 Review**
- 지금 효율 쓰레기같이 나온 이유를 여러 가지 알게 됨.
1. 현재 SI PV + RED Laser를 쓰는데 이게 효율이 안 좋음.
2. 온도에도 영향이 있는 건 처음 알게 된 사실.
3. OWPT의 다양한 종류들과 접근법들을 알게 됨.

## 🧠 13. New Knowledge & Terms
- **EEL, VCSEL** : Semiconductor laser. EEL은 칩의 옆면에서 빛이 나옴, 광통신에 많이 쓰이지만 고출력은 구조가 복잡함. VCSEL은 칩의 윗면에서 빛이 나옴, 기판 위에 2D array로 찍어내기 쉬워서 고출력 패널을 만들기에 유리함.
- **SLM (Spatial Light Modulators)** : 픽셀 하나하나의 빛을 조절할 수 있는 장치. 렌즈를 기계적으로 안 움직이고 빛의 초점을 바꾸거나 방향을 꺾을 수 있음.
- **IoUT** : Internet of Underwater Things.
- **SOA (Semiconductor Optical Amplifiers)** : 반도체 광증폭기, 빛을 증폭하는 반도체 소자.
- **Perovskite** : 차세대 태양전지, 발광 다이오드 등 첨단 소재로 큰 주목을 받고 있음. 높은 광 효율과 밴드갭 조절 능력 덕분에 얇고 가벼운 필름 형태로 제작 가능.