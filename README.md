# 🏎️ TIBCO Spotfire를 활용한 레이싱 시뮬레이션 데이터 분석

> 시뮬레이션 게임을 기반으로 수집한 레이싱 데이터를 Spotfire를 통해 시각화하고 분석함으로써, 운전 습관, 브레이크 구간, 휠슬립 발생 지점 등을 파악할 수 있는 데이터 기반의 레이싱 전략 분석 프로젝트입니다.

---

## 📌 프로젝트 개요

레이싱 게임 데이터를 활용하여 실제 주행처럼 분석 가능한지 실험하였습니다. 'Assetto Corsa Competizione' 게임에서 랩 데이터를 추출한 뒤, 이를 TIBCO Spotfire로 시각화 및 분석하였습니다.

* 시뮬레이터로 생성된 고정밀 데이터 기반 분석
* 가속도, 브레이크 포인트, 휠슬립 등 핵심 주행 요소 탐색
* Spotfire의 시계열 분석, 지도 시각화, 클러스터링 기능 활용

---

## 🎮 데이터 수집 방식

* **게임 환경**: Assetto Corsa Competizione (국제 규격 시뮬레이션)
* **데이터 추출**: Sim Racing Telemetry를 활용하여 CSV로 저장
* **샘플 랩 수**: 약 9랩, 약 25분 간 주행하며 로그 수집
* **샘플 주기**: 약 0.015초 간격으로 고속 로그 기록

---

## 🌍 Spotfire 분석 요소

### 1️⃣ 지도 기반 시각화

* Spotfire의 맵차트 기능을 활용하여 WGS84 좌표계 기반 트랙 위치를 시각화
* 상대좌표 데이터를 GPS 좌표로 변환하여 주행 경로 중첩 시각화

### 2️⃣ 가속도 계산

* CSV에는 직접적인 가속도 정보가 없어, 속도의 차분(difference)으로 근사 계산
* Spotfire에는 미분 기능이 없어 차분으로 대체하였으며, 고속 샘플링 데이터이므로 충분한 정밀도 확보

### 3️⃣ G-Force 활용

* 가속도 이외에도 G-Force 값을 활용하여 브레이크 강도 및 급커브 구간 추정

### 4️⃣ 휠슬립 분석

* 휠슬립은 특정 시점에만 발생하므로 이상값 분석 필요
* 평균의 함정에 빠지지 않도록 분포 기반 시각화 적용

---

## 🔍 고급 기능 및 확장 가능성

### 📊 K-Means 클러스터링 적용

* 드라이버 별 운전 스타일 분류 가능 (공격형 / 보수형 / 중립형)
* 충분한 랩 데이터 확보 시 머신러닝 기반 주행 성향 분석

### 🔄 스트리밍 데이터 적용

* 실시간 센서 데이터를 Spotfire Data Streams 기능으로 불러올 경우,
  실시간 주행 분석 및 경기 중 피드백 가능

---

## ✅ 기대 효과

* 가정용 시뮬레이터 기반으로도 의미 있는 데이터 분석 가능
* 실제 레이싱에 준하는 의사결정 훈련 가능
* 데이터 기반 레이싱 전략 구성 가능
* BI 도구인 Spotfire를 창의적으로 응용한 사례

---

## 📁 파일 설명

1. ACC-1741114758491.csv
   > Steam에 존재하는 전용 Telemetry Add-on 프로그램을 통해 추출된 주행 데이터.
   > 용량 문제로 인해 필요시 전송해드립니다.

2. Mashup.dxp
   > 주행 시각화를 담고 있는 Spotfire 분석 전용 확장자 파일.

3. TIBCO Spotfire 활용 예시 오동근 발표
   > 인턴십 기간 동안 진행한 Spotfire의 활용 예시 발표.
   > 용량 문제로 인해 아래 페이지에 수록하였습니다.


---

> ⓒ 오동근 | TIBCO Spotfire 기반 시뮬레이션 분석 프로젝트



![Slide1](https://github.com/user-attachments/assets/eda94ca3-b605-47da-8e56-8549c482357b)
![Slide2](https://github.com/user-attachments/assets/27666d3d-9e5a-4c4e-896a-623067184acb)
![Slide3](https://github.com/user-attachments/assets/676323f6-8003-4118-9e10-0be5e5f6b10f)
![Slide4](https://github.com/user-attachments/assets/4bf84a11-c073-404c-a854-524585b15e3f)
![Slide5](https://github.com/user-attachments/assets/a7b0b8bb-a5ad-4394-9245-ffa5e060e251)
![Slide6](https://github.com/user-attachments/assets/780a2486-b919-4354-9137-71aaf3adffb9)
![Slide7](https://github.com/user-attachments/assets/76e6bc56-5c02-4ef7-bb46-5af04c66ea1f)
![Slide8](https://github.com/user-attachments/assets/0fc22183-4938-426c-a822-26f2c710bf98)
![Slide9](https://github.com/user-attachments/assets/a3c7be4d-3fc8-461f-8e1b-2ea9e51386d1)
![Slide10](https://github.com/user-attachments/assets/a8eb0bc4-3a21-4e29-8c01-4a67ed1ce140)
![Slide11](https://github.com/user-attachments/assets/8dee61db-a116-4e70-b0fc-bc15c3d1dd3c)
![Slide12](https://github.com/user-attachments/assets/fd24187e-566a-49c6-88ba-36da2a2c373b)
![Slide13](https://github.com/user-attachments/assets/1349e310-c7f2-4f0c-a529-ed3276b8e4b1)
![Slide14](https://github.com/user-attachments/assets/3ad90347-0291-4035-9686-711dd9bf5632)
![Slide15](https://github.com/user-attachments/assets/54771ca1-33bc-4301-b924-dab5e662026d)
![Slide16](https://github.com/user-attachments/assets/fda7ee71-29bc-4968-85a7-986c3b2eff23)
![Slide17](https://github.com/user-attachments/assets/65637f14-fbe5-4f25-8259-200a4c78a36c)
![Slide18](https://github.com/user-attachments/assets/85db5a2a-a1f7-478f-b221-de54b2b9150b)
![Slide19](https://github.com/user-attachments/assets/3f8c63d7-7087-4c0a-b99f-d4e9cc43b6e8)
![Slide20](https://github.com/user-attachments/assets/6c957d3e-40f4-41fe-959a-301d00e3ac6b)
![Slide21](https://github.com/user-attachments/assets/33cafd5b-a91b-492d-84eb-c3c1f0a57de6)
![Slide22](https://github.com/user-attachments/assets/d5c37577-17f0-486b-9418-63a66243ba32)
![Slide23](https://github.com/user-attachments/assets/3e12fef4-f91a-40e5-a581-db53a00ab887)
![Slide24](https://github.com/user-attachments/assets/349546e8-5edc-4ec7-9657-614f20638796)
![Slide25](https://github.com/user-attachments/assets/d93de448-fb6d-4eb7-85b0-d3ee858612e0)
![Slide26](https://github.com/user-attachments/assets/cac1e698-6355-432d-8cf6-84b9c5f1bcaf)
![Slide27](https://github.com/user-attachments/assets/46d6e9df-de7b-4399-83de-f13962e73b39)
![Slide28](https://github.com/user-attachments/assets/b36f175a-c644-4d84-ab27-f8687a4170cc)
![Slide29](https://github.com/user-attachments/assets/ac653a22-3a4c-4614-a447-9f88b6b56555)
![Slide30](https://github.com/user-attachments/assets/85c1d0a9-1a85-442d-9e46-4977ac0280f3)
![Slide31](https://github.com/user-attachments/assets/4ed0bd63-7b33-4546-adaf-e11893be9820)
![Slide32](https://github.com/user-attachments/assets/4e4a166b-9ede-4acd-a01e-330844cbeec8)
![Slide33](https://github.com/user-attachments/assets/e17f47ec-aaed-4834-b04a-d1646b0d890b)
![Slide34](https://github.com/user-attachments/assets/57d28a1f-2140-4249-9e99-13ce1b24d02d)
![Slide35](https://github.com/user-attachments/assets/2412f0cb-5dc0-4a27-92d3-366d73ee1044)
![Slide36](https://github.com/user-attachments/assets/1f4a1575-8a0a-4f81-8b42-c152c6ed6fc5)
![Slide37](https://github.com/user-attachments/assets/07ed853b-56f6-4437-8b2c-aac2dc600911)
![Slide38](https://github.com/user-attachments/assets/0b9e7381-cb33-450f-8849-a8444e6f6c74)
![Slide39](https://github.com/user-attachments/assets/01462528-66a8-4e45-bcb5-24861a15a5b1)
![Slide40](https://github.com/user-attachments/assets/b6981b0d-157f-4782-806a-532094ec4250)
![Slide41](https://github.com/user-attachments/assets/70d416fd-5d2e-4d60-b7fb-382f4f4e51cd)
