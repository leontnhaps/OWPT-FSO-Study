# 📑 Indoor Optical Wireless Power Transfer to Small Cells at Nighttime

> **Paper Title:** Indoor Optical Wireless Power Transfer to Small Cells at Nighttime  
> **Authors:** John Fakidis, Stefan Videv, Stepan Kucera, Holger Claussen, Harald Haas  
> **Journal:** JOURNAL OF LIGHTWAVE TECHNOLOGY, VOL. 34, NO. 13, JULY 1, 2016  
> **Keywords:** `#Diode lasers`, `#Energy efficiency`, `#Energy harvesting`, `#Laser beams`, `#OWPT`, `#Quantum well lasers`, `#RF`, `#Rectennas`, `#Small cells`, `#Solar energy`

## 📝 1. Abstract
- **환경**: 실내 OWPT 환경, 주변 빛이 없는(Darkness) 조건에서 진행.
- **실험 구성**: 4개의 **Red Laser Diodes (LDs)**, 5.2m 거리 떨어진 **Si Solar Panel**.
- **성능 지표**:
    - **Fill Factor (FF)**: 69% 측정.
    - **OW Link 효율**: 3.2% 측정.
- **전력 수준**: 실험에서 수확된 전력은 **mW** 수준인 반면, 실제 SC(Small Cell) 작동에는 **1W**가 필요함.
- **시뮬레이션**: 시뮬레이션 도구인 **Zemax**를 사용하여 **42개의 레이저 기반 송신기**를 설계함.
- **결과 예측**: 시뮬레이션 결과, **30m 거리**에 **7.2W**를 전달할 수 있음을 보여줌.

## 🚀 2. Introduction
- **SC(Small Cells)**: 모바일 네트워크의 수요 증가에 따른 해결책 중 하나. 네트워크 용량 증대 및 전력 소비 감소의 이점이 있으나, **높은 설치 비용**이 제한 요소임.
- **광섬유 기술**: SC에 **Backhaul Communication**을 제공하기 위한 해결책 중 하나이나, 설치 비용과 전원 공급 장치 요구 사항이 단점.
- **대안**: 대체 전원 공급원과 무선 백홀 통신은 SC의 배치를 효율적으로 만들 수 있음.
- **EH(Energy Harvesting)의 한계**: 태양이나 바람은 날씨 조건 변동성의 단점이 존재함.
- **WPT(Wireless Power Transfer)**: 보완적이고 신뢰할 수 있는 솔루션. **RF**와 **Optical** 방식으로 나뉨. 본 논문은 **Optical** 방식에 집중.
- **OWC(Optical Wireless Communications)** 분류:
    - **FSO(Free Space Optical)**: 주로 송신기에 레이저, 수신기에 PD를 사용하여 데이터 전송.
    - **VLC(Visible Light Communications)**: 주로 LED와 PD 사용.
- **최종 목표**: 실외 소형 셀에 **1W의 전력**과 **고속 FSO 백홀 통신**을 동시에 제공하는 OWPT의 적용.
- **연구 단계**:
    1. 첫 번째 단계로 **실내**에서 테스트 진행. 주변에 수확할 빛이 없을 때도 작동해야 하므로 **깜깜한 환경(Nighttime)** 선택.
    2. **Study I**: 태양광 수신기 효율이 입력 광 전력에 따라 어떻게 변하는지 관찰하기 위해 **mW 단위**의 광 전력 전송에 소수의 LD 사용. 물리적 모델에 따라 1W 수확 전력을 달성하는 데 필요한 LD 수 추정.
    3. **Study II**: 레이저 빔 발산(Divergence)을 결정하기 위한 연구.
    4. **Study III**: 다중 레이저 송신기의 설계.

## 📚 3. Previous Work
- **테슬라의 연구**: 주로 RF, 전자기 스펙트럼의 마이크로파 영역에서 연구 수행.
- **WPT 분류**: Near field magnetic resonance coupling, Inductive coupling, RF, Laser의 4가지로 분류됨.

### 📡 3-A. Radio Frequency Based WPT
- **자기공명 방식**: 2m 거리에서 60W 전송 성공했으나, 최종 기기까지의 전체 효율이 **15%**로 낮음.
- **IPTS(유도 전력 전송)**: 30cm 거리에서 105W 전송이 **77%** 효율로 시연됨.
- **SC 적용 한계**: SC의 실외 설치는 **100~300m** 링크 거리에서 **1W** 전력을 필요로 하기에, 기존 방식은 불가능하고 **RF 또는 레이저 소스**를 이용한 전송 기술뿐임.
- **Rectenna**: RF 전파를 받아 전기로 바꿔주는 장치. 효율은 1~90%까지 다양하나, 장거리 전송에 대한 결과가 부족함.

### ☀️ 3-B. Optical Wireless Power Transfer and EH From Sunlight
- **레이저 기반 OWPT**: 위성 응용에서 처음 도입됨.
- **고출력 LD 기술**: 최근 940~980nm 파장 영역에서 **65% 이상의 변환 효율**로 **10W 이상의 출력** 수준 보고.
- **렌즈 사용**: 빛의 시준(Collimation)을 위한 렌즈 사용은 매우 높은 지향성을 가지면서도 복잡하지 않은 시스템을 만들 수 있음.
- **이전 실험 (LED)**: 고휘도 백색 LED, 대형 파라볼라 거울, 5m 거리에 배치된 a-Si 태양광 패널 사용.
    - 최대 효율 **0.1%**, 수확 전력 **18.3mW**에 불과.
    - 상당한 광 손실과 a-Si의 매우 낮은 에너지 효율, LED의 **Lambertian 패턴** 때문으로 분석됨.
- **후속 연구 (Laser)**: 레이저로 교체하고 패널을 **Multi-c-Si**로 변경.
    - 효율 **0.74%**, 수확 전력 **10.4mW**.
    - 여전히 낮은 태양광 패널 효율과 동일 패널 내 셀 간의 **불일치(Mismatch) 손실** 효과로 설명됨.

### 📶 3-C. Simultaneous Wireless Communication and Power Transfer
- **Rectenna 기반**: EH 및 데이터 통신은 입증되었으나, 거리가 **1m 내**로 너무 짧음.
- **VLC 기반**: 데이터 전송은 광범위하게 조사되었으며, LED 광원을 이용한 속도 타당성 입증 사례 존재.
- **Solar Panel 활용**: 태양광 패널을 사용하여 **mW 단위 전력**과 **12Mb/s 데이터 속도**의 OWC 동시 수행이 **95cm 링크 거리**에서 시연됨.

#### ☁️ 3-C-1. Challenges Induced by an Atmospheric Channel
- **제약 요인**: 대기 채널을 통과하는 레이저 빔 전파는 **Atmospheric attenuation**, **Scintillation**, **Misalignment**, **Ambient light noise** 등의 제약을 받음.
    - **Atmospheric Attenuation (대기 감쇠)**: 광파의 전력 감소 야기.
    - **Scintillation (섬광/대기 난류)**: 대기 굴절률 변화로 인한 빛 강도의 불규칙한 변화.
    - **Misalignment (정렬 불량)**: FSO는 고지향성 레이저 빔을 사용하므로, 최대 전력 수신을 위해 정밀한 정렬 필요.
    - **Ambient Light Noise**: 태양빛 같은 외부 빛이 노이즈로 인식될 수 있음.

#### 🛡️ 3-C-2. Potential Solutions to the Atmospheric Channel's constraints
- **날씨 영향**: 맑은 날씨에서의 대기 손실은 무시할 수 있는 수준. 짙은 안개 조건은 FSO 링크 사용을 힘들게 하지만 드물게 발생함.
- **MRC (Maximum Ratio Combining)**: 여러 개의 송신기와 수신기로 다중 FSO Link를 만들어 최적의 채널을 선택하는 기법 적용 가능.
- **Aperture Averaging**: 섬광의 영향은 수신기의 면적을 넓게 만들어 빛을 평균화(Aperture Averaging)함으로써 완화 가능.
- **Large Receiver**: 수신기를 크게 만드는 것이 섬광과 정렬 불량 효과에 대한 효과적인 기술로 간주됨.

## 🧪 4. Study 1 : Total Link And Components Efficiency
내일 마저 읽음요

## 💡 New Knowledge & Terms
- **Fill Factor (FF)**: 태양전지 특성 평가 파라미터. 최대 전력점을 (개방단 전압 $\times$ 단락 전류)로 나눈 값.
- **Backhaul Communication**: 계층적 통신망에서 Edge networks를 Core networks나 Internet에 연결하는 역할. 셀룰러 네트워크에선 무선접속망(RAN)과 핵심망(CN) 간 연결을 의미.
- **Rectenna**: Antenna와 Rectifier를 결합한 장치. 주변의 전자기파를 수신하여 직류 전기로 변환하는 기술.
- **Maximum Ratio Combining (MRC)**: 여러 안테나로 수신된 신호들을 각각의 신호 품질에 비례하여 가중치를 적용해 최적으로 결합, 전체 신호의 품질을 최대화하는 수신 다이버시티 기술.