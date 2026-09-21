<div align="center">

# 김광빈 · Gwangbin Kim

**신호에서 이상(異常)을 찾아내는 AI 엔지니어**

한성대학교 컴퓨터공학부 · 방산 AI / 신호처리

</div>

---

## 무엇을 하는 사람인가

스펙트럼, 음성, 센서 시계열 — 형태는 달라도 **"정상 신호를 학습해 벗어난 것을 잡아낸다"**는 문제는 같습니다.
라만 분광 신호의 노이즈 제거에 쓴 이중 인코더 구조를 음성 딥페이크 탐지로 옮기고,
거기서 익힌 재구성 오차 기반 탐지를 다시 UAV/UGV 센서 이상탐지에 적용해 왔습니다.

도메인을 갈아타며 같은 축을 깊게 파는 쪽을 선호합니다.

## 주요 프로젝트

| 프로젝트 | 무엇을 풀었나 | 결과 |
|---|---|---|
| **[haegeum-addon](https://github.com/gawbi/haegeum-addon)** | UAV/UGV 유·무인 복합체계의 센서 스푸핑·이상 거동을 VAE 재구성 오차로 실시간 탐지. Red Agent로 공격 캠페인을 설계해 방어 모듈을 역으로 검증 | UGV F1 **0.927**<br>UAV F1 **0.828** |
| **[hc-roberta-cross-attention](https://github.com/gawbi/hc-roberta-cross-attention)** | 정형 수치 피처와 비정형 텍스트 임베딩이라는 이종 신호를 Cross-Attention으로 융합. 융합 깊이를 3단계로 나눠 대조 실험 | F1 **0.9832**<br>(5-Run 평균) |

> 연구실 과제 및 대회 출품작 2건(라만 스펙트럼 전처리 · 음성 딥페이크 탐지)은 공개 승인 절차 진행 중입니다.

## 기술 스택

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![ROS2](https://img.shields.io/badge/ROS2-22314E?style=flat-square&logo=ros&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**다루는 문제** · 이상탐지(VAE / 재구성 오차) · 어텐션 기반 멀티모달 융합 · 신호 전처리(웨이블릿, 베이스라인 보정) · 생성모델을 이용한 데이터 증강 · 설명가능 AI(LIME / SHAP)

## 지금 하는 일

- 유·무인 복합체계 이상탐지 모듈의 **실시간 추론 성능** 개선
- 스펙트럼 신호 전처리 파이프라인의 재현성 정비
- 방산 AI의 **신뢰성·설명가능성(Trustworthy AI)** 문헌 정리

---

<div align="center">

<img height="150" src="https://github-readme-stats.vercel.app/api?username=gawbi&show_icons=true&hide_border=true&title_color=2F81F7&icon_color=2F81F7&hide=issues" />
<img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=gawbi&layout=compact&hide_border=true&title_color=2F81F7&langs_count=6" />

</div>
