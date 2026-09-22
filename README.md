<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-light.svg" />
  <img width="100%" alt="Gwangbin Kim — signal to anomaly" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-dark.svg" />
</picture>
</div>

<br>

신호를 다룹니다. 스펙트럼에서 시작해 음성을 거쳐, 지금은 로봇 센서를 봅니다.

**정상을 학습해서, 벗어난 것을 잡는다.**

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/journey-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/journey-light.svg" />
  <img width="100%" alt="signal processing to anomaly detection to robotics" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/journey-dark.svg" />
</picture>
</div>

<br>

### 지금 향하는 곳

**매니퓰레이터 모방학습.** 사람이 리더암으로 시연한 동작을 로봇이 배워 스스로 반복하게 만드는 쪽을 보고 있습니다. 텔레오퍼레이션으로 시연을 모으고, 행동 청킹 계열 정책으로 학습하고, 시뮬레이터에서 검증한 뒤 실물로 옮기는 흐름입니다.

이제 막 시작했습니다. 논문과 구현을 읽는 단계이고, 앞으로 올라올 저장소는 대부분 여기에 올릴 예정입니다.

**[robotics-from-scratch](https://github.com/gawbi/robotics-from-scratch)** — 좌표계부터 직접 구현하며 공부하는 기록입니다.
읽은 것을 옮겨 적지 않고, 구현한 뒤 독립된 기준과 대조해 숫자로 확인하는 것을 규칙으로 삼습니다.
IK 해는 FK에 다시 넣어 오차를 재고, 해석적 야코비안은 수치 미분과 비교합니다.
검증 숫자가 없는 단계는 끝난 것으로 치지 않습니다.

<br>

### 과거 진행내용(포트폴리오 X)

<table>
<tr>
<td width="50%" valign="top">

#### <a href="https://github.com/gawbi/haegeum-addon">haegeum-addon</a>

ROS2 위에서 도는 UAV · UGV 이상탐지 모듈. 센서가 조작됐는지 VAE 재구성 오차로 판별합니다. 공격자 에이전트를 따로 만들어 방어 모듈을 검증했습니다.

`UGV F1 0.927` · `p99 0.04ms` · `실시간 여유 2,400배`

SHAP을 붙이는 과정에서 <b>이전 분석의 오류를 찾아내 바로잡았습니다.</b>

</td>
<td width="50%" valign="top">

#### <a href="https://github.com/gawbi/hc-roberta-cross-attention">hc-roberta-cross-attention</a>

성격이 다른 두 신호를 Cross-Attention으로 융합하는 실험. 정형 수치 피처와 텍스트 임베딩을 붙였지만, 구조 자체는 센서 융합과 같은 문제입니다.

`F1 0.9832` · `5-Run 평균`

융합 깊이를 3단계로 나눠 무엇이 실제로 성능을 만드는지 분리했습니다.

</td>
</tr>
</table>

<br>

### 도구

<p>
<img src="https://img.shields.io/badge/ROS2-22314E?style=for-the-badge&logo=ros&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" />
</p>

**다뤄온 문제**

- 변분 오토인코더 기반 이상탐지
- 크로스 어텐션 기반 이종 신호 융합
- 웨이블릿 변환 기반 신호 전처리
- 적대적 생성 신경망 기반 데이터 증강
- 섀플리 값 기반 모델 설명

**배우고 있는 것**

- 행동 청킹 기반 모방학습
- 리더-팔로워 텔레오퍼레이션과 기구학 리타게팅
- 시뮬레이터 기반 정책 검증과 실물 이전

추후 포트폴리오 작성부분(나중에 작성하고나서 깃허브 리드미 파일 배치변경)

<br>

<br>

<div align="center">

</div>
