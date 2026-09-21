<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-light.svg" />
  <img width="100%" alt="Gwangbin Kim — signal to anomaly" src="https://raw.githubusercontent.com/gawbi/gawbi/main/assets/banner-dark.svg" />
</picture>
</div>

<br>

신호를 다룹니다. 스펙트럼에서 시작해 음성을 거쳐, 지금은 로봇 센서를 봅니다.

방법은 계속 하나였습니다. **정상을 학습해서, 벗어난 것을 잡는다.**

<br>

### 지금 향하는 곳

**ROS2 기반 자율 이동로봇.** 인지와 센서 융합, 그리고 스스로 이상을 알아채는 자율성까지 한 스택 안에서 다루는 것이 목표입니다.

앞으로 올라올 저장소는 대부분 여기에 속합니다. 지금까지의 작업은 그 바탕입니다.

<br>

### 바탕이 된 작업

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

**다루는 문제**

- 변분 오토인코더 기반 이상탐지
- 크로스 어텐션 기반 이종 신호 융합
- 웨이블릿 변환 기반 신호 전처리
- 적대적 생성 신경망 기반 데이터 증강
- 섀플리 값 기반 모델 설명

<br>

### 뱀뱀이

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/output/github-snake.svg" />
  <img alt="contribution snake" src="https://raw.githubusercontent.com/gawbi/gawbi/output/github-snake.svg" />
</picture>
</div>

<br>

<div align="center">

</div>
