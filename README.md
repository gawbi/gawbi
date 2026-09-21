<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:1F6FEB,100:2F81F7&height=200&section=header&text=Gwangbin%20Kim&fontSize=54&fontColor=FFFFFF&fontAlignY=36&desc=signal%20%E2%86%92%20anomaly&descAlignY=58&descSize=18" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=3200&pause=900&color=2F81F7&center=true&vCenter=true&width=600&lines=%EC%8A%A4%ED%8E%99%ED%8A%B8%EB%9F%BC%2C+%EC%9D%8C%EC%84%B1%2C+%EC%84%BC%EC%84%9C+%EC%8B%9C%EA%B3%84%EC%97%B4;%EB%8F%84%EB%A9%94%EC%9D%B8%EC%9D%80+%EB%B0%94%EB%80%8C%EC%96%B4%EB%8F%84+%EB%AC%B8%EC%A0%9C%EB%8A%94+%EA%B0%99%EC%8A%B5%EB%8B%88%EB%8B%A4;%EC%A0%95%EC%83%81%EC%9D%84+%EB%B0%B0%EC%9A%B0%EA%B3%A0%2C+%EB%B2%97%EC%96%B4%EB%82%9C+%EA%B1%B8+%EC%9E%A1%EB%8A%94%EB%8B%A4" />

</div>

---

### 안녕하세요 👋

한성대 컴공 다니면서 **신호에서 이상한 걸 잡아내는 일**을 하고 있습니다.

라만 분광 스펙트럼의 노이즈를 걷어내는 구조를 만들었는데, 그게 음성 딥페이크 탐지에도 먹히더라고요.
거기서 배운 재구성 오차 방식을 다시 드론 센서 이상탐지에 갖다 썼습니다.

도메인은 계속 바뀌는데 하는 일은 결국 똑같습니다 — **정상을 학습해서, 벗어난 걸 잡는다.**

지금은 방산 AI 쪽을 보고 있습니다. 🛰️

<br>

### 🔧 만든 것들

<table>
<tr>
<td width="50%" valign="top">

#### 🛸 <a href="https://github.com/gawbi/haegeum-addon">haegeum-addon</a>

드론이랑 지상로봇 센서가 조작당했는지 VAE로 실시간 탐지합니다.
공격하는 쪽(Red Agent)도 직접 만들어서 방어 모듈을 두들겨 봤어요.

`UGV F1 0.927` · `p99 0.04ms` · `실시간 여유 2,400배`

SHAP 붙여보다가 <b>예전에 제가 뽑은 분석이 틀렸던 것도 발견</b>했습니다.

</td>
<td width="50%" valign="top">

#### 🧬 <a href="https://github.com/gawbi/hc-roberta-cross-attention">hc-roberta-cross-attention</a>

숫자 피처랑 텍스트 임베딩처럼 <b>성격이 다른 두 신호</b>를 Cross-Attention으로 붙이는 실험입니다.

`F1 0.9832` · `5-Run 평균`

융합을 얕게 / 깊게 3단계로 나눠서 뭐가 실제로 효과 있는지 비교했습니다.

</td>
</tr>
</table>

> 🔒 연구실 과제랑 대회 출품작 2개(라만 스펙트럼 전처리 · 음성 딥페이크 탐지)는 공개 승인 기다리는 중입니다.

<br>

### 🛠️ 쓰는 것들

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" />
<img src="https://img.shields.io/badge/ROS2-22314E?style=for-the-badge&logo=ros&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
</p>

**요즘 파고 있는 것** — 이상탐지(VAE) · 어텐션 융합 · 웨이블릿 신호처리 · GAN 데이터 증강 · 설명가능 AI(SHAP)

<br>

### 🐍 제 잔디 먹는 뱀

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gawbi/gawbi/output/github-snake.svg" />
  <img alt="contribution snake" src="https://raw.githubusercontent.com/gawbi/gawbi/output/github-snake.svg" />
</picture>
</div>

<br>

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=gawbi&show_icons=true&hide_border=true&bg_color=00000000&title_color=2F81F7&icon_color=2F81F7&text_color=8B949E&hide=issues" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=gawbi&layout=compact&hide_border=true&bg_color=00000000&title_color=2F81F7&text_color=8B949E&langs_count=6" />

<br><br>

<img width="92%" src="https://github-profile-trophy.vercel.app/?username=gawbi&theme=discord&no-frame=true&no-bg=true&margin-w=6&row=1&column=6" />

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:2F81F7,50:1F6FEB,100:0D1117&height=120&section=footer" />

</div>
