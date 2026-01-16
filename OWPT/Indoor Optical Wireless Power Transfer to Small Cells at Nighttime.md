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

### 4-A. Objective
- **연구 목적**: 이전 저자의 연구에서 생성된 **5m OW 링크**의 에너지 효율을 높이는 것.

### 4-B. Analytical Model
- 다이오드에서 생성된 빔, 렌즈, 렌즈에 의해 재형성된 빔, 태양광 패널, 전체 링크 및 구성 요소의 효율에 대한 모델링.
- 다이오드에서 생성된 레이저 빔은 **타원형 가우시안 모델(Elliptical Gaussian Model)**이 고려됨.

#### 4-B-1) Generated Beam From the Laser Diode
- LD 패키지 내부에 배치된 방출층 크기는 $2W_{0x} \times 2W_{0y}$.
- $W_0$은 각각 **Beam Waist (빔 반경)**.
- LD에서 생성된 빔은 파장을 발산각으로 나눈 값에 비례함.
- 파장은 레이저의 파장값, 발산각은 레이저의 세기가 절반이 되는 **HWHM (Half Width at Half Maximum)** 값 기준으로 계산.
- 광 빔은 어떠한 손실 없이 LD의 패키지를 통과하는 것으로 간주.
- LD 앞에 있는 보호 유리창도 빔의 강도에 영향이 없는 것으로 간주.
- $z$에 따른 비율은 방사된 거리만큼의 퍼짐 비율을 곱하여 산출 가능 **(식 3, 4)**.
- 이 식은 레이저 출발점부터 렌즈에 닿기 직전까지만 유효함.
- 식에서의 $z_0$는 LD 빔의 **Rayleigh range**를 나타내며, 이는 빔이 퍼지지 않고 직진할 수 있는 구간의 스펙임.
- **Rayleigh range**: 빔 반경이 최소값에서 $\sqrt{2}$배 커지는 지점까지의 거리.
- 렌즈를 통과해 퍼지는 빔도 마찬가지로 계산 가능.
- 렌즈 곡률 반경에 따른 가우시안 빔의 곡률 반경 식은 **(식 7, 8)**과 동일.
- 렌즈 곡률($R$)과 $W$를 계산한 파라미터 $q$ 내용 포함.
- 빛의 강도에 관한 식에서 $G_0$은 최대 강도를 의미.
- 생성된 빔의 총 광전력 식은 **Appendix B**에 적분으로 증명되어 있음.

#### 4-B-2) Thick Lens
- 광학 시스템에서 입력과 출력을 연관시키는 방법으로 **ABCD 행렬** 사용.
- ABCD 방식은 전자공학 분야에서 이미 통용된 방법.
- 가우시안 빔에 ABCD 법칙을 사용하려면 **$q$-파라미터**를 사용해야 함.
- 렌즈의 지름은 $D$와 혼동을 피하기 위해 $\delta$(델타)를 사용.
- 관련 수식은 **(식 14~17)** 참고.

#### 4-B-3) Reshaped Beam From the Lens
- 렌즈를 통과한 빔이 모이는 초점을 계산하는 식 유도.

#### 4-B-4) Physical Model of Solar Panel and Curve Fitting
- 앞에서 계산한 레이저 빛 $G$를 패널이 받았을 때, 실제로 전기가 얼마나 나오는지 계산하기 위한 모델.
- 태양광 패널을 수학적으로 다루기 위해 **Single Diode Model**을 도입.
- **키르히호프 법칙** 적용 시 패널 밖으로 나오는 전류:
    - (빛으로 만든 전류) - (다이오드가 소비하는 전류) - (저항이 소비하는 전류).
- 다이오드의 전류식은 **Shockley Diode Equation** 사용.
- 저항이 소비하는 전류는 **옴의 법칙**으로 계산 가능.
- 이때 각각의 변수들에서 필요한 값들은 제조사가 알려주지 않는 이상 알 수 없으므로 **최적화**를 통해 값을 찾아야 함.
- **MSE (Mean Squared Error)**를 통해 역으로 계산해냄.
- 본 논문에서는 21번 측정하여 값을 찾음.

#### 4-B-5) Total Link and Components Efficiency
- WPT의 가장 중요한 측면은 구성 요소 링크의 **전체 효율**.
- LD 외부 전력 효율은 $P_T / P_{in} \times 100\%$.
- 광무선 채널에선 **LoS (Line of Sight)** 조건이 가정됨.
- 실내 환경에서 수행되므로, 분자 흡수 및 산란 효과로 인한 **대기 감쇠는 고려되지 않음**.
- 오직 기하학적인 손실만 가정됨.
- 전체적인 효율은 **(Panel에 들어온 빛 / 쏜 빛)**의 비율로 계산.
- 패널 자체의 성능은 **광-전기 변환 효율**로 계산:
    - (최대 생산 전기 / 받은 빛 에너지) $\times 100\%$.
- 최종적인 **최대 링크 효율**은 (최종 생산 전기 / 콘센트에서 나온 전기) $\times 100\%$.
- **전체 효율 공식**:
    - 레이저 효율 $\times$ 렌즈 투과율 $\times$ 빔 수집 효율 $\times$ 패널 변환 효율.
    - 이를 통해 어디서 손실이 많이 발생하는지 확인 가능.

### 4-C) Eye Safety Regulations
- 제조사에 분류되지 않은 레이저는 직접 계산하여 등급을 매겨야 함.
- 등급 순서: **Class 1 (안전) < 2 < 3R < 3B < 4 (매우 위험)**.
- 본 논문에서는 **3B (실명 위험)** 등급이 계산됨.
- **안전 거리**:
    - 렌즈가 없을 땐 **63cm** 이내 접근 금지.
    - 렌즈가 있을 땐 **3.6m**까지 위험.

### 4-D) Experimental System and Results
- **Laser**: Opnext HL6544FM (660nm) 사용.
- **광 수신기**: Multi-c-Si / Mono-c-Si 패널 사용.

#### 4-D-2) Experiment 1 - Objective, Method, Setup and Applied Analytical Model
- **목표**: 5m 거리에서 OW 링크의 실험적 에너지를 증가시키는 연구 수행.
- **전체 시스템 블록**:
    - AC Power Supply $\rightarrow$ DC Power Supply $\rightarrow$ Single/Multiple LD(s) $\rightarrow$ Single/Multiple Aspheric Lens $\rightarrow$ Optical Wireless Channel $\rightarrow$ Solar Panel $\rightarrow$ Variable Resistor.
- **측정**: 가변 저항을 통해 전력 측정.
- **시나리오 1**: 송신기 개수 **1~4개**, **Multi-c-Si** 사용.
- **시나리오 2**: 송신기 개수 **1~3개**, **Mono-c-Si** 사용.
- 가변 저항의 전압을 조절하여 전력 측정.
- 각 V-P 곡선에서 **최대 수확 전력**이 존재하며, 이는 완벽한 부하 매칭 조건 하에서 가능.
- 태양광 수신기의 저항은 부하의 저항과 같음.

#### 4-D-3) Scenario 1 - Results and Discussion
- 광 송신기가 **1개** 사용될 때, 최대 전력값들은 꽤 낮음.
- 여러 셀이 직렬 연결되어 있는데, 하나만 사용 시 가장자리에 위치한 셀들은 적은 광 전력을 받음.
- 더 높은 수신 레벨을 가진 셀들에 의해 생성된 전력이 낮은 조도 레벨을 가진 셀들에 의해 소산됨.
- PV 패널의 전체 전기 출력은 가장 낮은 성능을 가진 셀들에 의해 결정됨 (**Mismatch Loss**).
- 송신기를 여러 개 사용할수록 성능이 폭발적으로 상승함.
    - 이유: 같은 곳을 쏘는 게 아니라 골고루 나눠서 조사하기 때문 **(그림 4 참고)**.
- **Mismatch 효과**: 송신기를 1 $\rightarrow$ 2, 2 $\rightarrow$ 3으로 늘릴수록 불일치 문제가 점차 개선됨을 확인.

#### 4-D-4) Scenario 2 - Results and Discussion
- **단결정(Mono-c-Si)**에서는 예상과 다르게 폭발적인 상승은 없었음.

#### 4-D-5) IPTS와 비교
- (별도 내용 없음)

#### 4-D-6) Experiment 2 - Objective, Method, Setup, Applied Analytical Model and Results
- **Thorlabs S121B Si**를 통해 LD의 효율값 측정 (LD 제품 편차 확인 목적).
- 같은 모델임에도 입력 전력에 따라 출력 전력이 어느 정도 다른 것을 확인.
- 높은 신뢰도를 얻기 위해선 **가장 효율이 낮은 LD 기준**으로 시뮬레이션 추정을 해야 함.

#### 4-D-7) Experiment 3 - Objective, Method, Setup and Results
- 태양전지의 효율을 결정하기 위해 수행.
- **실험 조건**: 2 LD, 5.2m 거리, **Mono-c-Si** 셀.
- **입력 전력**: 561.3mW.
- **측정 방식**: 셀을 25개의 구역으로 나누어 측정.
- 25개 지점에서 측정 후 셀 유효 면적을 곱하여 광전력을 구함.
- **결과**:
    - 셀이 수신한 광 전력: **134.38 mW**.
    - 실제 생산 전력: **17.8 mW**.
    - 계산된 수집 효율값: **89.4%**.

#### 4-D-8) Estimation of the Number of Optical Transmitters
- **목표**: 5.2m 거리에서 **1W**를 수확하기 위한 LD와 렌즈의 개수 산출.
- 실험 1의 시나리오 2에서 레이저가 2개일 때 $P_m = 17.8mW$ 달성.
- 셀 스펙상 1W 생성 시 **0.537V** 필요.
- 부하 전류 계산 시 **1.86A**.
- 위 식들에 대입하면 **1.96A**가 나옴.
- 태양광 패널 반응성은 4-D-7 계산값 바탕으로 1W당 **0.49A**가 필요함.
- 즉, 패널에 **4W**의 빛이 도달해야 함.
- 역산 결과, **4.47W**의 레이저 출력을 쏴야 함.
- 따라서 계산된 필요 송신기(Tx) 개수는 **61개**임.

#### 4-D-9) Variation of Harvested Power and Link Efficiency Induced by the Application of Data Communication
- **질문**: 데이터 통신을 병행하면 링크 효율이 어떻게 변할까?
- **통신 방식**: **OFDM** 사용 (대역폭 5MHz).
- **결과**:
    - 수신기 평균 데이터 전송률: **16.6Mb/s**.
    - BER: $1.52 \times 10^{-3}$.
- 통신 여부와 관계없이 수신 전력은 **거의 동일하게 유지됨**.
- **이유**: 시간 영역의 OFDM 신호가 평균 **0**을 가지기 때문.
- **수신기 회로 구성**:
    - 에너지 하베스팅(EH) Branch: **DC** 성분 수신.
    - 통신 Branch: **AC** 신호 수신.
    - 각각 인덕터와 커패시터를 포함하여 분리.

## 5~6. Study 2 & 3
- (관심 분야 아님 - 렌즈 시준 및 시뮬레이션 내용이므로 생략)

## 7. Conclusion
- RF나 LED 방식은 효율이 낮았으나, 설계한 **다중 레이저 시스템(42개 LDs)** 시뮬레이션 결과, **30m 거리**의 기지국에 **7.2W** 전송 가능함을 보임 (야간).
- **Mismatch Loss** 문제는 빔을 여러 개 나누어 조사함으로써 해결.

---

### 🧐 8. Review
- **Study 1 모델링**: 내 연구에서도 충분히 적용 및 모델링 가능할 것으로 보임.
    - 현재 렌즈 사용 여부가 미정(현재 미사용)이나, 모델링을 통해 성능 예측이 가능할 듯함.
- **문제점 식별**: 현재 연구에서 사용하는 레이저가 타겟에 비해 너무 큰 편인데, **4-D-3)**의 결과(낮은 효율의 셀이 전체 전력을 제한하는 Mismatch Loss)를 고려할 때 이 부분이 성능 저하의 원인이 될 수 있음.
- **난관**: **Mismatch Loss**가 상당히 중요한 요소로 다뤄지는데, 전체 시스템에서 빔이 셀을 완벽하게 덮도록(Covering) 만드는 것이 핵심 과제이나 구체적인 해결 방안이 막막함.

### 💡 9. New Knowledge & Terms
- **Fill Factor (FF)**: 태양전지 특성 평가 파라미터, 최대 전력점을 (개방단 전압 $\times$ 단락전류)로 나눈 값.
- **Backhaul Communication**: 계층적 통신망에서 Edge networks를 Core networks나 Internet에 연결하는 역할. 셀룰러 네트워크에선 무선접속망(RAN)과 핵심망(CN) 간 연결을 백홀이라 부름.
- **Rectenna**: Antenna와 Rectifier(정류기)를 결합한 장치. 주변 전자기파를 수신해 직류 전기로 변환하는 기술.
- **Maximum Ratio Combining (MRC)**: 여러 안테나로 수신된 신호들에 신호 품질에 비례한 가중치를 적용해 결합, 전체 신호 품질을 최대화하는 수신 다이버시티 기술.
- **Multi-Quantum Well (MQW)**: LED나 LD의 핵심 기술. 밴드갭이 작은 얇은 활성층과 큰 절연층을 교대로 적층하여 강한 빛을 효율적으로 방출.
- **Paraxial Approximation (근축 근사)**: $\sin(\theta) \approx \theta$ (rad)와 같이 근사화하여 계산하는 방식.
- **Complex Beam Parameter**: 광학에서 곡률과 굵기 두 물리량을 계산하는 파라미터 $q$.
- **ABCD Matrix**: 광학 시스템 입출력을 연관 짓는 행렬. $[r_{out}, \theta_{out}]^T = [A, B; C, D] [r_{in}, \theta_{in}]^T$. ($A$: 배율, $B$: 유효거리, $C$: 굴절능, $D$: 각도배율).
- **Shockley Diode Equation**: 다이오드에 흐르는 전류와 양단 전압의 관계를 설명하는 공식.
- **Thorlabs S121B Si**: 400nm~1100nm 파장 범위의 광출력을 측정하는 Si PD.
- **OFDM**: 고속 데이터 스트림을 여러 느린 부반송파로 나누어 직교성을 유지하며 병렬 전송하는 디지털 통신 기술.