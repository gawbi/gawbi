<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-light.svg" />
  <img width="100%" alt="Gwangbin Kim — signal to anomaly" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-dark.svg" />
</picture>
</div>

<br>

신호를 다룹니다. 스펙트럼에서 시작해 음성을 거쳐, 지금은 로봇이 걷는 법을 강화학습으로 가르칩니다.

**정상을 학습해서, 벗어난 것을 잡는다.**

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/journey-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/journey-light.svg" />
  <img width="100%" alt="signal processing to anomaly detection to robotics" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/journey-dark.svg" />
</picture>
</div>

<br>

### 지금 하고 있는 것 — 휴머노이드 강화학습

**[robotics-rl-study](https://github.com/gawbi/robotics-rl-study)** — 강의 실습으로 PPO를 구현해 보는 것부터 시작해, Isaac Lab에서 Unitree G1 보행 정책을 학습하고 보상을 하나씩 바꿔 가며 정책이 어떻게 달라지는지 숫자로 확인하는 기록입니다.

`4096 환경 병렬` · `1500 iteration / 27분` · `20초 생존 99.6%` · `실습으로 구현한 PPO로 CartPole 500점`

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/g1-ablation-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/g1-ablation-light.svg" />
  <img width="100%" alt="feet_air_time을 끄면 넘어짐과 명령 추종은 그대로, 발 미끄러짐 벌점은 32% 커짐" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/g1-ablation-dark.svg" />
</picture>
</div>

<div align="center">
<a href="https://github.com/gawbi/robotics-rl-study/blob/main/day5-g1-reward-experiment/notes.md"><img width="100%" alt="왼쪽: 실험 0 (기본 보상), 오른쪽: 실험 1 (feet_air_time = 0). 같은 명령으로 걷는 두 정책의 비교" src="https://raw.githubusercontent.com/gawbi/robotics-rl-study/main/day5-g1-reward-experiment/images/exp0_vs_exp1.gif" /></a>
</div>

보상 하나(`feet_air_time`)만 끈 실험에서 넘어짐과 명령 추종은 그대로였지만, 발 미끄러짐 벌점이 32% 커졌습니다.
보상 항목 하나가 "걸을 수 있느냐"보다 "어떻게 걷느냐"를 바꾼다는 결과입니다. 시드 1개로 얻은 결과라서, 시드 3개 반복으로 다시 확인할 예정입니다.

<br>

### 캡스톤 준비 — 말하고 걷는 상상부기

<div align="center">
<img width="300" alt="상상부기 로봇 Day 1: 동상 비율로는 뒤로 기울어 등껍질에 기대고, 배치를 바꾼 균형안은 버티며, 원본 보행 정책으로 걷는 MuJoCo 시뮬레이션" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/bugi-reel-day1.gif" />
</div>

한성대 마스코트 상상부기의 외형으로 이족보행 로봇을 만드는 캡스톤 준비 작업입니다. 오픈소스 [Open Duck Mini v2](https://github.com/apirrone/Open_Duck_Mini)의 다리 기구를 그대로 쓰고, 실물을 만들기 전에 MuJoCo 개념 모델로 외형 배치부터 검증했습니다.
동상 비율 그대로 외피를 씌우면 무게중심이 발 뒤로 가서 서보만으로 서지 못했고, 몸통과 머리를 앞으로 옮기고 배터리를 배 쪽으로 내려 해결했습니다.

`뒤로 넘어지는 각도 3.8° → 11.9° (원본 11.4°)` · `원본 보행 정책 그대로, 부기 무게 모델 13초 86 cm` · `개념 모델 1.96 kg`

보행은 원본 공개 정책을 목 서보를 남긴 부기 무게 모델에 그대로 돌린 결과이고, 목을 고정한 10관절 부기용 재학습과 실물 제작은 다음 학기 과제입니다.
학교 캐릭터를 쓰는 프로젝트라 저장소는 비공개이고, 영상은 시뮬레이션 합성입니다(캐릭터 · 로고 © 한성대학교).

<br>

### 지금 향하는 곳

**휴머노이드 Whole-Body Control.** 시뮬레이터에서 학습한 정책을 다른 시뮬레이터(MuJoCo)로 옮겨 검증하고, 실물로 옮기는 흐름까지 가는 것이 목표입니다.
매니퓰레이터 쪽에서는 리더암으로 시연한 동작을 로봇이 배워 스스로 반복하게 만드는 모방학습도 함께 보고 있습니다.

**[robotics-from-scratch](https://github.com/gawbi/robotics-from-scratch)** — 2링크 팔로 좌표계 · FK · IK · 야코비안을 직접 구현하며 공부하는 기록입니다.
지금은 1~2단계(좌표계, FK) 개념 정리를 마쳤고, 구현은 아직 시작하지 않았습니다.
단계마다 완료 조건을 테스트로 먼저 정해 두었고, IK는 FK에 다시 넣은 오차로, 해석적 야코비안은 수치 미분과 비교해 검증할 계획입니다.
검증 숫자가 없는 단계는 끝난 것으로 치지 않습니다.

<br>

### 이전 프로젝트 — 신호 · 이상탐지

<table>
<tr>
<td width="50%" valign="top">

#### <a href="https://github.com/gawbi/haegeum-addon">haegeum-addon</a>

ROS2 노드로 만든 UAV · UGV 이상탐지 모듈. 센서가 조작됐는지 VAE 재구성 오차로 판별합니다. 공격 에이전트를 따로 만들고, 같은 공격을 오프라인으로 주입해 방어 모듈을 검증했습니다.

`p99 추론 0.041 ms (UGV) · 0.119 ms (UAV)` · `Apple M5 CPU 1스레드 기준` · `10 Hz 예산의 0.12 % 이하` · `합성 센서 데이터`

SHAP을 붙이는 과정에서 <b>이전 분석의 오류를 찾아내 바로잡았습니다.</b>

</td>
<td width="50%" valign="top">

#### <a href="https://github.com/gawbi/hc-roberta-cross-attention">hc-roberta-cross-attention</a>

성격이 다른 두 신호를 Cross-Attention으로 융합하는 실험. 정형 수치 피처와 텍스트 임베딩을 붙였지만, 구조 자체는 센서 융합과 같은 문제입니다.

`F1 0.9832 ± 0.0007 (5-Run)` · `TF-IDF 기준선 0.9744`

비교 모델(Simple Concat, Cross-Attention)을 직접 구현해 팀 제안 모델과 대조했고, <b>누수 감사로 F1의 대부분이 데이터셋의 표층 단서에서 온다는 것을 밝혔습니다</b> (TF-IDF만으로 F1 0.9744).

</td>
</tr>
</table>

**[voice-deepfake-detection](https://github.com/gawbi/voice-deepfake-detection)** — 해커톤 출품작. 멜 스펙트로그램과 웨이블릿 스칼로그램을 2채널로 ResNet-18에 넣는 이중 파이프라인입니다. ASVspoof 2019 LA 5,000 utterance 서브셋·단일 시드에서 dev EER `5.50% → 3.80%`가 관찰됐지만, 두 실험의 입력 길이와 배치가 달라 <b>웨이블릿 효과로 단정할 수 없다는 점을 README에 교란 변수 표로 명시</b>했습니다.

<br>

### 그 외

- **[MENDAI](https://github.com/gawbi/MENDAI)** — 팀 프로젝트. 분류기(DINO)와 탐지기(DETR · YOLO) 실험. DETR 쪽은 신뢰구간과 conf 선택 기준을 적어 두었습니다.
- **[track-digital-twin](https://github.com/gawbi/track-digital-twin)** — 라즈베리파이 자율주행 실습 트랙의 디지털 트윈 도면. 치수마다 측정 · 사진 · 추정 출처를 구분해 표기했습니다.
- **[legacy-archive](https://github.com/gawbi/legacy-archive)** — 2020년 C/C++ 수업 실습 코드 아카이브.

<br>

### 비공개 프로젝트

코드를 올릴 수 없는 작업들입니다. 데이터가 기관 소유이거나, 발표 전 연구이거나, 원 구현의 공개 동의가 아직 없습니다. 주제와 역할만 남깁니다.

| 주제 · 기간 | 무엇을 했나 | 비공개 이유 |
|---|---|---|
| **VLM 보조 라벨링으로 사람 검토 줄이기** · 2026-10 | 로봇 과제의 성공/실패 라벨을 로컬 VLM이 먼저 달고 사람은 일부만 검토하는 파이프라인을 만들고, 합성 데이터로 검토 정책을 비교했습니다. HIL-SERL 보상 분류기용이며, 소프트웨어 시제품과 합성 실험까지 마쳤고 실제 로봇 실험은 아직 전입니다. | 연구실 발표 전 연구 |
| **보상 기반 critic shaping 연구 인수인계** · 2026-10 ~ | 지도교수의 연구를 인수인계 받아 원본 실험 결과를 재집계해 검증하고, 이어받기 위한 학습 교재와 재집계 도구를 작성했습니다. 학습 실험은 재실행하지 않았습니다. | 미발표 연구 |
| **운동화 손상 탐지 — 슈도 라벨 파이프라인** · 2026-10 | CVAT 사람 라벨로 YOLO를 학습하고, 라벨 없는 원본에 슈도 라벨을 달아 검수 뒤 재학습하는 파이프라인을 만들었습니다. 자동 라벨러 세 종(YOLO · Grounding DINO · SAM 3) 비교 스크립트를 포함합니다. 같은 과제의 모델 실험은 [MENDAI](https://github.com/gawbi/MENDAI)에 공개돼 있습니다. | 원본 라벨 파일과 데이터 경로를 포함 |
| **라만 스펙트럼 전처리** · 2026-01 ~ 07 | 선행 연구자의 RSGAN · RSBPCNN 구현을 인수인계 받아 베이스라인 생성기와 쌍 지도학습으로 개선하고 재학습했습니다. | 원 구현의 공개 동의 전 |

<br>

### 도구

<p>
<img src="https://img.shields.io/badge/Isaac_Sim-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
<img src="https://img.shields.io/badge/Isaac_Lab-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" />
</p>

**다뤄온 문제**

- PPO 직접 구현과 디버깅 (GAE, ratio · clip_fraction 관찰)
- 휴머노이드 보행의 보상 설계 실험 (Isaac Lab, Unitree G1)
- 변분 오토인코더 기반 이상탐지
- 크로스 어텐션 기반 이종 신호 융합
- 웨이블릿 변환 기반 신호 전처리
- 적대적 생성 신경망 기반 데이터 증강
- 섀플리 값 기반 모델 설명

**다음에 보려는 것** (아직 저장소에 코드가 없습니다)

- 휴머노이드 보행 정책의 sim-to-sim 검증 (Isaac Sim → MuJoCo)
- 행동 청킹 기반 모방학습
- 리더-팔로워 텔레오퍼레이션과 기구학 리타게팅
- 시뮬레이터 기반 정책 검증과 실물 이전
