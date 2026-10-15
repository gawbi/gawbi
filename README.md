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

<div align="center">
<a href="https://github.com/gawbi/robotics-rl-study"><img width="100%" alt="Isaac Lab에서 PPO로 학습한 Unitree G1 평지 보행" src="https://raw.githubusercontent.com/gawbi/robotics-rl-study/main/day4-g1-reward-baseline/images/exp0_baseline.gif" /></a>
</div>

**[robotics-rl-study](https://github.com/gawbi/robotics-rl-study)** — PPO를 직접 구현하는 것부터 시작해, Isaac Lab에서 Unitree G1 보행 정책을 학습하고 보상을 하나씩 바꿔 가며 정책이 어떻게 달라지는지 숫자로 확인하는 기록입니다.

`4096 환경 병렬` · `1500 iteration / 27분` · `20초 생존 99.6%` · `직접 구현한 PPO로 CartPole 500점`

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/g1-ablation-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/g1-ablation-light.svg" />
  <img width="100%" alt="feet_air_time을 끄면 넘어짐과 명령 추종은 그대로, 발 미끄러짐 벌점은 32% 커짐" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/g1-ablation-dark.svg" />
</picture>
</div>

보상 하나(`feet_air_time`)만 끈 실험에서 넘어짐과 명령 추종은 그대로였지만, 발 미끄러짐 벌점이 32% 커졌습니다.
보상 항목 하나가 "걸을 수 있느냐"보다 "어떻게 걷느냐"를 바꾼다는 결과입니다. 시드 1개로 얻은 결과라서, 시드 3개 반복으로 다시 확인할 예정입니다.

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

`p99 추론 0.041 ms (UGV) · 0.119 ms (UAV)` · `10 Hz 예산의 0.12 % 이하` · `합성 센서 데이터`

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

<br>

### 도구

<p>
<img src="https://img.shields.io/badge/Isaac_Sim-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
<img src="https://img.shields.io/badge/Isaac_Lab-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/ROS2-22314E?style=for-the-badge&logo=ros&logoColor=white" />
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

**배우고 있는 것**

- 휴머노이드 보행 정책의 sim-to-sim 검증 (Isaac Sim → MuJoCo)
- 행동 청킹 기반 모방학습
- 리더-팔로워 텔레오퍼레이션과 기구학 리타게팅
- 시뮬레이터 기반 정책 검증과 실물 이전
