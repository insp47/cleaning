# 반도체 웨이퍼 건조 공정 비교 시뮬레이션
초임계 건조(TEL) vs 승화건식(DNS) — 모세관력 기반 패턴 붕괴 모델

## 개요
반도체 미세 패턴(고종횡비 트렌치)의 습식 공정 후 건조 단계에서 발생하는
모세관력에 의한 패턴 붕괴(stiction) 현상을, 두 공정 기술의 상평형 경로와
빔 굽힘 모델을 통해 인터랙티브하게 시각화한 프로젝트입니다.

## 배경
- 회로 미세화(3nm급 이하)에 따라 트렌치 종횡비가 높아지면서
  건조 시 모세관력에 의한 패턴 붕괴가 수율에 직접적인 영향을 미침
- TEL은 초임계 CO2로 액-기 계면 자체를 없애는 방식,
  DNS는 승화(고체→기체 직접 전이)로 액상을 건너뛰는 방식을 채택
- 두 방식의 물리적 원리 차이를 정량적으로 비교할 수 있는 자료가
  마땅치 않아 직접 모델링

## 구성
1. **CO2 상평형 다이어그램** — 삼중점/임계점 기준 두 공정 경로 애니메이션
2. **트렌치 붕괴 비교** — 캔틸레버 빔-모세관력 모델로 종횡비/트렌치 폭/
   린스액 조건에 따른 붕괴 여부 실시간 계산
3. **정량 비교 패널** — Stiction 비율, 공정 조건, 장비 복잡도 비교

## 물리 모델
- 모세관력: F = 2γcosθ
- 빔 처짐: δ = FH³ / (3EI), I = w³/12
- 처짐이 트렌치 간격의 절반을 초과하면 붕괴로 판정

## 참고 문헌
- Chen et al., "Supercritical Drying: A Sustainable Solution to Pattern
  Collapse of High-Aspect-Ratio and Low-Mechanical-Strength Device
  Structures," ECS Trans. 69(8), 2015
- "Breakthrough of Sublimation Drying by Liquid Phase Deposition," 2021

## 바로가기 사이트
(https://insp47.github.io/cleaning/scco2-drying-comparison-simulation.html)

## 한계
빔 굽힘-모세관력 결합 모델은 문헌들이 공통적으로 설명하는 정성적
메커니즘을 근사한 것으로, 특정 논문의 실험값을 정밀 재현한 시뮬레이션은
아닙니다. 승화건식의 "공정 균일도" 파라미터는 문헌의 정성적 설명을
단순화하여 반영했습니다.
