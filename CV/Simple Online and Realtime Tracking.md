# 📑 LED-Based Optical Wireless Power Transmission for Automatic Tracking and Powering Mobile Object in Real Time Review


> **Paper Title:** LED-Based Optical Wireless Power Transmission for Automatic Tracking and Powering Mobile Object in Real Time
> **Authors:** Mingzhi Zhao, Tomoyuki Miyamoto
> **Journal:** IEEE Access (2025)
> **Keywords:** `#Wireless power transmission', '#wireless energy', '#optical engineering', '#optical design', '#beam steering', '#image recognition', '#control systems', '#Internet of Things'

---

## 1. 📑 Abstract
* 동적인 RX 에서 Machine Vision 과 예측 제어 알고리즘을 통해 안정적인 전력 공급을 보장하는 LED를 활용하는 OWPT 시스템.
* 2축 Beam-steering 메커니즘 결합.
* 결과적으로 1m 거리에서 40cm² GaAs(갈륨비소) Solar Cell 로 부터 최대 0.8W 출력 입증.
* 4m 범위내에서 30cm/s 로 움직이는 RX까지 작동 확인.

---

## 2. 🚀 Introduction
* **OWPT의 장점:** Long-range capabilities, high directionality, no electromagnetic interference 등의 장점이 있음.
    > 💡 **Note:** RF 방식의 WPT 보다 OWPT 가 장점이 있다는 내용.

* **LED vs Laser:** 2가지 방식으로 나뉘어 지는데 대부분은 Laser sources 를 사용함. 하지만 위험성과 Lambert's cosine law 로 인하여 더 넓은 발산각을 가지기에 LED 에서 우수함이 있음.
    > 💡 **Note:** 레이저에서는 어차피 장거리 전송효율과 직진성 으로 안전문제만 해결하면 레이저가 더 우수함.

* **Tracking의 필요성:** 송신기와 움직이는 수신기 사이의 지속적인 정렬 보장이 안정적인 전력 공급에 매우 중요, 타겟의 위치 변화에 맞춰 조정하는 실시간 자동추적 기능이 있는 OWPT 가 요구됨. 현재의 OWPT는 주로 정지해있거나 움직이지 않는 응용분야에 집중되어있음.

---

## 3. ⚙️ AUTO-OWPT System Design (시스템 모델)

### A. Optical System Design
* RX는 효율을 극대화 하기위해 GaAS Solar cell 로 채택, LED-array collimation scheme 제안.
* LED, Lens1, Lens2 로 구성되어있고, Lens 1은 퍼지는 빛을 평행광으로 변환해주는 역할.
* Lens 2는 퍼진 평행광을 Rx 로 모아주는 역할.
* 이 시스템을 통해 조사 면적을 작게 유지하면서 고출력을 가능하게함.
    > 💡 **Note:** 나의 경우에는 LED 가 아닌 Laser를 쓰기에 이미 합쳐진 System 이라 생각해도 될거같음, LED 를 통해 어떻게 Laser 처럼 고출력을 할지 렌즈로 설계한거같음.

### B. Beam Aiming System Design
* 2축의 회전을 조절하는 stepping motor 사용(본 논문에선 M1, M2 모터).
* 보통 beam aiming 에서는 빠른 응답속도를 가진 Galvano mirror 를 쓰지만 본 시스템에선 반사경의 크기제한으로 적합하지않음.
* 갈바노 미러의 최대 구경은 50mm 이고, 본시스템에선 너무 작아 beam leakage 를 초래함. 그래서 최소 표면적이 105x200 mm² 인 단일 대형 반사경을 모터에 달아서 사용.
    > 💡 **Note:** 나의 경우에는 어차피 pan,tilt 모터에 카메라를 달고 그위에 레이저를 부착예정이라 참고만.

### C. Control Method
* B 방식으로 모터를 회전시켜 조절했을떄 모터들이 직렬로 연결되어있어 빔의 이동경로가 직선경로를 따르지 않는 문제가 생김.
* M1, M2 모터를 조절했을때 이상적인 직선경로가 나오지 않고 곡선이 나오는데 정밀한 조정을 해야할때 문제가생김.
* 결국 이걸 해결하기위해 빔스팟과, 수신기의 중심좌표를 모두 감지하는 Feedback Control System 을 구현. 시스템은 두 Rx 와 beam 위치의 픽셀 차를 피드백을 통하여 제어.
    > 💡 **Note:** 본질적으로 pan,tilt 카메라를 사용했을때 휘는 이유를 이제 알았음. 카메라의 문제가 아닌 모터의 직렬 연결로 인한거였고, 결론적으로 본 논문은 둘다 인식해서 차이를 통해 제어. 나의 경우는 근데 지금 정확한 RX 의 위치를 모르는경우 -> RX의 위치를 정확하게 할려면 최소 2개의 filter 가 필요함.

---

## 4. 🎯 Detection and Prediction For Mobile Object

### A. Detection for Spot And PV
* Control Method 에서의 설명에서처럼 Beamspot 과 RX(PV)를 동시에 탐지하는것이 필수적임.
* LED 가 IR 이기에 RGB 카메라와 IR 카메라가 통합된 Intel RealSense D435 사용.
* Beamspot 은 IR(적외선)카메라를 사용하고 PV 패널은 RGB 카메라를 사용해 인식 서로 FOV(시야각) 이 다른데 출력 픽셀 범위를 조절해서 최대한 일치하도록 정렬시킴.
* 객체인식은 YOLO 가 아닌 더작은 물체 탐지에 용이한 SSD(Single Shot MultiBox Detector) 알고리즘 사용.
    > 💡 **Note:** 나의 경우는 어차피 YOLO 상위 버젼은 SSD 보다 우수하고, 반사필름을 사용하여 보다 인식률을 높이려 했기에...

### B. Prediction For Mobile Object
* 시스템 Latency 로 인하여 이미지 획득, 모터구동에 소요되는 시간이 발생.
* 측정시 약 0.1초로 측정됨. 이로인해 빔이 RX 에 도달했을때 물체가 이동해 정렬이 어긋남.
* LSTM 등 예측 알고리즘을 사용해봤으나 칼만필터가 최적의 알고리즘으로 선택됨.
    > 💡 **Note:** 아직 정지상태의 Rx를 나는 가정기에 참고만.

### C. Total System Design Including Prediction
* Rx의 Conf Threshold 를 0.5에서 0.2로 낮춤.
* 많은 잠재적 Rx 후보를 포착하게하고, BB의 면적이 너무크면 오인식이기에 버림.
* 그중 가장 작은 BB를 RX로 설정. (멀리있는 타겟이 가장 작기에).

---

## 5. 🧪 Setup And Evaluation
* 실제 실험에서 출력이 0.79W 로 측정. RX 의 크기가 커져야 거리가 멀어도 지속적으로 전력 공급 가능.
* 드론에 RX 달아서 2m~5m 비행하도록 했을때 칼만필터로만 으로도 잘따라감.

---

## 6. 🧐 Review

### 내 연구와의 비교

| Feature | My Project (Proposed) | This Paper |
| :--- | :--- | :--- |
| **Transmitter** | **Laser** (High directionality) | **IR LED** (Eye-safety focus) |
| **Receiver** | **Solar Cell + Retro-reflector** | **GaAs Solar Cell** |
| **Target State** | **Stationary** (Fixed position) | **Dynamic** (Moving drone) |
| **Control** | **Pan-Tilt Servo Motors** | **Lens + 2-Axis Stepping Motors** |
| **Vision Model** | **YOLOv11** (Superior to SSD) | **SSD** |

### 내 연구에 적용하는 방안
결국 나는 정적이기에 예측부분은 제외하고(칼만필터) 결국 두 오차로 계산하는것이 핵심인데:
1. 고휘도 반사필름을 위아래로 같은 거리차로 붙이면 두개를 인식하여 두 좌표의 평균 값으로 Rx 의 픽셀을 구할수 있음.
2. 그러면 최초 위치 추정 단계 에서 대략적인 pan, tilt 추정 값을 구함.
3. 추가보정단계에서 2개를 인식해서 중앙값인 Rx 의 좌표를 구한 후 레이저를 켬.
4. 마찬가지로 레이저의 Beam Spot 을 인식하여 두개의 좌표 차이만큼 Pan tilt 를 움직여 두 좌표의 차이를 0으로 만드는 pan, tilt 값을 추가로 구하는 방안으로 적용가능.

---

## 7. 📝 New Knowledge & Terms
* **GaAs Solar Cell:** 갈륨비소 태양전지. 일반 실리콘보다 효율이 높고 특히 850nm 대역 반응성이 좋음.
* **Galvano Mirror:** 고속 정밀 제어가 가능하나 구경이 작아 고출력/대구경 빔 조향에는 한계가 있음.
* **SSD (Single Shot MultiBox Detector):** 1-stage 객체 인식 알고리즘. (현재는 YOLO 시리즈가 더 우세함)
