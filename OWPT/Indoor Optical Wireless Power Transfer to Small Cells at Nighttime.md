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
- 연구 1의 목표는 이전 저자의 연구에서 생성된 5m OW 링크의 에너지 효율 높이기.

### 4-B. Analytical Model
- 다이오드에서 생성된 빔, 렌즈, 렌즈에 의해 재형성된 빔, 태양광 패널, 전체 링크 및 구성 요소의 효율에 대한 모델.
- 다이오드에서 생성된 레이저 빔은 타원형 가우시안 모델이 고려됨.

#### 4-B-1) Generated Beam From the Laser Diode
- LD에서 패키지 내부에 배치된 방출층은 $2W_{0x} \times 2W_{0y}$.
- $W_0$은 각각 Beam Waist (빔 반경).
- LD에서 생성된 빔은 파장을 발산각으로 나눈 값에 비례함.
- 파장은 레이저의 파장값, 발산각은 레이저의 세기가 절반이 되는 HWHM 값 기준으로 계산.
- 광 빔은 어떠한 손실 없이 LD의 패키지를 통과하는 것으로 간주.
- LD 앞에 있는 보호 유리창도 빔의 강도에 영향 X로 간주.
- z에 따른 비율은 방사된 거리만큼의 퍼짐 비율을 곱해서 구할 수 있음 (식 3, 4).
- 레이저 출발점부터 렌즈 닿기 직전까지만 유효.
- 식에서의 $z_0$는 LD 빔의 Rayleigh range를 나타내는데, 빔이 얼마나 안 퍼지고 직진할 수 있는 스펙.
- Rayleigh range는 빔 반경이 최소값에서 $\sqrt{2}$배 커지는 지점까지의 거리.
- 렌즈에서 퍼지는 것도 마찬가지로 계산 가능.
- 렌즈 곡률 반경에 따른 가우시안 빔의 곡률 반경 식은 식 (7), (8)과 동일.
- 렌즈 곡률(R)과 W를 계산한 파라미터 q 내용.
- 빛의 강도에 관한 식, $G_0$은 최대 강도.
- 생성된 빔의 총 광전력 식, Appendix B에 적분으로 증명되어 있음.

#### 4-B-2) Thick Lens
- 광학 시스템에서 입력과 출력을 연관시키는 방법은 ABCD 행렬 사용.
- ABCD 방식은 이미 전자과에선 통용된 방법.
- 가우시안 빔에 ABCD 법칙 사용하려면 q-파라미터를 사용.
- 렌즈의 지름은 D와 안 헷갈리기 위해 델타 사용.
- 식은 식 14~17 참고.

#### 4-B-3) Reshaped Beam From the Lens
- 렌즈를 통과한 빔의 모이는 초점을 계산하는 식 유도.

#### 4-B-4) Physical Model of Solar Panel and Curve Fitting
- 앞에서 계산한 레이저 빛 G를 패널이 받았을 때, 실제로 전기가 얼마나 나오는지 계산하기 위한 모델.
- 태양광 패널을 수학적으로 다루기 위해 **Single Diode Model**을 도입.
- 키르히호프 법칙 적용 시 패널 밖으로 나오는 전류는 (빛으로 만든 전류) - (다이오드가 먹는 전류) - (저항이 먹는 전류).
- 다이오드의 전류식은 **Shockley Diode Equation**.
- 저항이 먹는 전류는 옴의 법칙으로 계산 가능.
- 이때 각각의 변수들에서 필요한 값들은 제조사가 알려주지 않는 이상 알지를 못하기에 최적화를 통해 값을 찾아야 함.
- MSE를 통해서 역으로 계산해냄.
- 본 논문은 21번 측정해서 값 찾음.

#### 4-B-5) Total Link and Components Efficiency
- WPT의 가장 중요한 측면은 구성 요소 링크의 전체 효율.
- LD 외부 전력 효율은 $P_T/P_{in} \times 100\%$.
- 광무선 채널에선 LoS 조건이 가정됨.
- 실내 환경에서 수행되므로, 분자 흡수 및 산란효과로 인한 대기 감쇠는 고려되지 않음.
- 기하학적인 손실만 가정됨.
- 전체적인 효율은 (Panel에 들어온 빛 / 쏜 빛)의 비율로 계산.
- 패널 자체의 성능은 광-전기 변환 효율로 계산.
- (최대 생산 전기 / 받은 빛 에너지) $\times 100\%$.
- 최종적인 최대 링크 효율은 (최종 생산 전기 / 콘센트에서 나온 전기) $\times 100\%$.
- 전체 효율 = 레이저 효율 $\times$ 렌즈 투과율 $\times$ 빔 수집 효율 $\times$ 패널 변환 효율로 계산이 가능.
    - 어디서 손실이 많이 나는지 확인도 가능.

### 4-C) Eye Safety Regulations
- 제조사에 분류되지 않은 건 직접 계산하여 등급을 매겨야 함.
- Class 1(안전) < 2 < 3R < 3B < 4(매우 위험).
- 본 논문에서는 **3B (실명 위험)** 등급이 계산됨.
- 렌즈가 없을 땐 **63cm** 이내 접근 금지.
- 렌즈 있을 땐 **3.6m**까지 위험.

### 4-D) Experimental System and Results
- **Opnext HL6544FM** laser 사용. 660nm.
- 광 수신기는 **multi-c-Si / mono-c-Si**로 사용.

#### 4-D-2) Experiment 1 - Objective, Method, Setup and Applied Analytical Model
- 5m에서 OW 링크의 실험적 에너지를 증가시키려는 연구 1의 목표가 수행.
- 전체적인 시스템 블록은:
    - AC power supply -> DC power supply -> Single Multiple LD(s) -> Single/Multiple Aspheric Lens -> Optical Wireless Channel -> Solar Panel -> Variable Resistor.
- 가변 저항을 통해 전력 측정.
- **시나리오 1**: 송신기 개수를 1~4개로 실험하고 multi-c-Si 사용.
- **시나리오 2**: 송신기 개수를 1~3개로 실험하고 mono-c-Si 사용.
- 가변 저항의 전압을 조절하여 전력 측정.
- 각 V-P 곡선에서 최대 수확 전력이 존재하는데, 완벽한 부하 매칭 조건 하에서 가능.
- 태양광 수신기의 저항은 부하의 저항과 같다.

#### 4-D-3) Scenario 1-Results and Discussion
- 시나리오 1에서 광 송신기가 1개 사용될 때, 최대 전력값들은 꽤 낮음.
- 여러 셀이 직렬로 연결되어 있는데 하나를 사용했을 때 가장자리에 위치한 셀들은 적은 광 전력을 받음.
- 더 높은 수신 레벨을 가진 셀들에 의해 생성된 전력은, 더 낮은 조도 레벨을 가진 셀들에 의해 소산됨.
- PV 패널의 전체 전기 출력은 가장 낮은 성능을 가진 셀들에 의해 결정됨 (**Mismatch Loss**).
- 송신기를 여러 개 할수록 성능이 폭발적으로 상승했는데 그 이유는 같은 곳을 쏘는 게 아니라 골고루 나눠서 쏨 (그림 4 참고).
- 미스매치 효과를 1->2, 2->3 점점 늘릴수록 점점 안 좋아짐을 확인.

#### 4-D-4) Scenario 2-Results and Discussion
- 단결정에서는 예상과는 다르게 폭발적인 상승은 없었음.

#### 4-D-5) IPTS 와 비교

#### 4-D-6) Experiment 2-Objective, Method, Setup, Applied Analytical Model and Results
- **Thorlabs S121B Si**를 통해 LD의 효율값 측정 (LD 제품의 문제일 수도 있으니).
- 같은 모델임에도 입력 전력에 따라 출력 전력이 어느 정도 다른 것을 확인.
- 높은 신뢰도를 얻기 위해선 가장 효율이 낮은 LD 기준으로 시뮬레이션 추정을 해야 함.

#### 4-D-7) Experiment 3-Objective, Method, Setup and Results
- 태양전지의 효율을 결정하기 위해 수행.
- 실험 조건은 2 LD, 5.2m, mono-c-Si 셀.
- 입력 전력은 561.3mW.
- 셀을 25개의 구역으로 나눠서 측정.
- 25개의 지점에서 측정을 하고 셀 유효 면적을 곱하여 광전력을 구함.
- 셀이 수신한 광 전력은 **134.38 mW**로 계산됨.
- 실제 생산 전력은 **17.8mW**.
- 계산 결과 수집 효율값은 **89.4%**.

#### 4-D-8) Estimation of the Number of Optical Transmitters
- 5.2m 거리에서 1W를 수확하기 위한 LD와 렌즈의 개수를 구할 예정.
- 실험 1의 시나리오 2에서 레이저가 2개일 때 $P_m = 17.8mW$ 값을 달성함.
- 셀 스펙에서 1W를 만들 때 **0.537V**가 필요한데.
- 부하 전류는 **1.86A**로 계산됨.
- 이 값들을 위 식들에 대입하면 **1.96A**가 나옴.
- 태양광 패널의 반응성은 4-D-7에서 계산한 값들 바탕으로 1W당 **0.49A**가 필요함.
- 즉 패널에 **4W** 빛이 꽂혀야 함.
- **4.47W** 레이저를 쏴야 함 역산하면.
- 그래서 Tx 계산하면 **61개** 필요.

#### 4-D-9) Variation of Harvested Power and Link Efficiency Induced by the Application of Data Communication
- 만약 데이터도 보내면 링크 효율이 어떻게 변할까?
- 통신을 위해 **OFDM**을 사용함.
- OFDM은 5MHz의 대역폭 사용.
- 수신기에서 평균 데이터 전송률 16.6Mb/s가 달성되었으며 BER은 $1.52 \times 10^{-3}$임.
- 통신을 할 때와 안 할 때를 비교하면 거의 **동일하게 유지됨** 수신 전력이.
- 이유는 시간 영역의 OFDM 신호가 0의 평균을 가지기 때문.
- 수신기 회로는 에너지 하베스팅을 위한 branch와 통신을 위한 branch로 구성됨. 각각 인덕터와 커패시터를 포함함.
- EH branch는 DC 성분을 보고, 통신 branch는 AC 신호를 봄.

## 5) STUDY 2 : Laser Beam Collimation
- 

---

### ?-1. Review
- **Study 1**: 잘 모델링하면 내 연구에서 모델링도 가능할 듯. 우선 나는 아직 렌즈를 쓸지 안 쓸지 모르겠는데 우선 안 쓰고 있으니까 어느 정도 모델링 해서 예측이 가능할 것 같음.
- 현재 내 연구에서 레이저에 비해 너무 큰 걸 쓰고 있는데 4-D-3)의 결과를 보면 결국 낮은 셀이 전체 전력을 총괄한다고 하니까 이 부분도 문제가 생김.

### ?. New Knowledge & Terms
- **Fill Factor(FF)**: 태양전지 특성평가 파라미터, 최대 전력점을 (개방단 전압 $\times$ 단락전류)로 나눈 값.
- **Backhaul Communication**: 계층적 통신망에서 Edge networks를 core networks나 internet에 연결하는 역할. 셀룰러 네트워크에선 무선접속망(RAN)과 핵심망(CN) 간 연결을 백홀이라고 부름.
- **Rectenna**: Antenna와 Rectifier을 결합한 장치로, 주변의 전자기파를 수신하여 직류 전기로 변환하는 기술.
- **Maximum Ratio Combining(MRC)**: 여러 안테나로 수신된 신호들을 각각의 신호 품질에 비례하여 가중치를 적용해 최적으로 결합, 전체 신호의 품질을 최대화하는 수신 다이버시티 기술.
- **Multi-Quantum Well(MQW)**: LED나 LD에서 사용되는 핵심 기술, band gap이 작은 얇은 활성층과 band gap이 큰 절연층을 교대로 쌓은 구조. -> 더 강한 빛을 효율적으로 방출할 수 있게 함.
- **Paraxial Approximation**: 근축근사 -> $sin(\theta) \approx \theta (rad)$ 같이 근사화해서 계산하는 것.
- **Complex Beam Parameter**: 광학에서 곡률과 굵기 두 가지 물리량을 계산하는 파라미터 q.
- **ABCD 행렬**: $[r_{out}, \theta_{out}]^T = [A, B; C, D] [r_{in}, \theta_{in}]^T$, A B C D는 각각 배율, 유효거리, 굴절능, 각도배율.
- **Shockley Diode Equation**: 다이오드에 흐르는 전류와 양단에 걸리는 전압의 관계를 설명하는 공식.
- **Thorlabs S121B Si**: Si PD인데 400nm~1100nm 파장 범위의 광출력 측정하는 데 사용.
- **OFDM**: 하나의 고속 데이터 스트림을 여러 개의 느린 부반송파로 나누어 직교성을 유지하며 병렬로 전송하는 디지털 통신 기술.