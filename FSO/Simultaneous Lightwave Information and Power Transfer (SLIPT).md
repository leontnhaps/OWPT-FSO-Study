# 📑 Simultaneous Lightwave Information and Power Transfer (SLIPT)

> **Paper Title:** Simultaneous Lightwave Information and Power Transfer (SLIPT)  
> **Authors:** Panagiotis D. Diamantoulakis, George K. Karagiannidis, Zhiguo Ding  
> **Journal:** IEEE TRANSACTIONS ON GREEN COMMUNICATIONS AND NETWORKING, VOL. 2, NO. 3, SEPTEMBER 2018  
> **Keywords:** `#VLC`, `#IRC`, `#Energy harvesting`, `#Wireless power transfer`, `#SLIPT`, `#Time-splitting`, `#DC bias`, `#FoV`

## 📝 1. Abstract
- **연구 제안**: 태양광 패널이 탑재된 **VLC(가시광 통신)**나 **적외선 통신(IRC)** 시스템에서 성능을 최적화할 수 있는 **SLIPT** 기법을 제안함.
- **최적화 전략**: 송신부와 수신부 양쪽에서 수행되며, 각각 다음과 같이 명명됨.
    - **Adjusting Transmission** (송신 조정)
    - **Adjusting Reception** (수신 조정)
    - **Coordinated Adjustment** (협력적 조정)
- **시뮬레이션 결과**: 컴퓨터 시뮬레이션을 통해 분석한 결과, 기존 방식과 달리 **수확된 에너지(Harvested Energy)**를 상당히 증가시키는 것으로 나타남.

## 🚀 2. Introduction
- **IoT 시대의 도래**: 유망한 응용 기회들이 열리고 있으며, 현재 IoT 장치들의 무선 접속은 주로 **RF 기술**로 구현됨.
- **대안 기술의 부상**: 실내 IoT 장치들에 접속을 제공하기 위한 **OWC, VLC, IRC** 등의 방법들이 유망한 대안 혹은 보완 기술로 인정받고 있음.
- **성능 우위**: 실내 VLC/IRC 네트워킹을 통해 보고된 데이터 전송률은 **WiFi**보다 훨씬 높음.
- **OWC(Optical Wireless Communication)의 장점**:
    1. 가용 대역폭 증가.
    2. 쉬운 대역폭 재사용.
    3. 에너지 효율 증가 및 상당한 에너지 절약.
    4. **RF 오염(Pollution)** 없음.
    5. **RF 간섭(Interference)**으로부터의 자유.
- **경제성**: **LED**와 **PD(Photodiode)**는 RF 장비보다 상당히 저렴한 편임.
- **에너지 제약**: IoT 기기가 무선 접속에 강하게 의존함에 따라 배터리에 의한 제약을 받음.
- **Energy Harvesting (EH)**: 에너지를 전기로 변환하는 EH는 IoT 기기들의 운영과 유지보수에 있어 주요한 부분이 됨.
- **기존 EH의 한계**:
    - 전통적인 EH 방법은 제어 불가능한(**Uncontrollable**) 천연자원에 의존해 왔음.
    - 주요 방법들은 원하지 않는 간섭이 발생하거나, **EM(전자기파) 노출** 위험이 존재함.
- **SWIPT의 필요성**: 정보 전송과 에너지 전송을 통합하는 **SWIPT**를 통해 이러한 문제들을 해결할 수 있음.

## 💡 3. New Knowledge & Terms
- **OPEX (Operating Expenditure)**: 기업의 운용 비용.