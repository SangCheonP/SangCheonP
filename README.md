![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=220&section=header&text=SangCheon%20Park&fontSize=62&fontAlignY=38&desc=Software%20Developer&descAlignY=58&descSize=20)

<div align="center">

### 👋 안녕하세요, 문제를 분석하고 개선하여 가치를 만드는 개발자 박상천입니다.

생산·품질 시스템과 MES를 개발·운영하며  
**업무 흐름과 데이터 처리 구조를 이해하고, 성능·정합성·운영 안정성을 개선해왔습니다.**

</div>

---

## 🚀 About Me

- 🏭 반도체 생산·품질 시스템 **SSPS Full Stack 개발 및 운영**
- ⚙️ 제조 현장 **MES Full Stack 개발 경험**
- 📊 Oracle SQL·PL/SQL 기반 **데이터 처리 및 성능 개선**
- 🔒 동시 요청 환경을 고려한 **데이터 정합성 및 동시성 제어**
- ☁️ Docker·Jenkins 기반 **배포 환경 및 CI/CD 구축**
- 🤖 AI 이미지 분석 시스템의 **이벤트 기반 처리 구조 및 인프라 구축**

---

## 💼 Experience

### NORISYSTEM | Software Developer
`C#` `ASP.NET` `Oracle` `PL/SQL` `JavaScript` `RealGrid2` `ECharts`

- SSPS Inbay 재공 현황, 기준정보, 품질 대시보드 등 화면·API·DB 기능 개발
- 약 **28만 건 Carrier + 2.5만 건 WIP → 2만 건 Inbay 데이터** 적재 구조 분석
- 불필요한 JOIN·GROUP BY·MAX 연산을 제거해 **약 3분 → 1분 20초, 55% 단축**
- 운영 반영 시 프로그램·DB 변경사항, 데이터 보정 SQL, 적용 순서와 검증 항목을 확인하는 절차 정립

### MES Project | Full Stack Developer
`Java` `Spring Boot` `React` `PostgreSQL`

- 제조 현장에서 작업지시, LOT Split·Merge, 위치 이동 등 MES/WMS 기능 개발
- 실제 사용자 업무 흐름을 확인해 Split·Merge 기능을 한 화면에서 연속 처리하도록 개선
- 채번 테이블에 **Row Lock + Commit** 기반 동시성 제어를 적용해 ID 중복 방지
- 2대의 PC에서 동시 요청을 발생시켜 Lock/Commit 동작과 중복 미발생 검증

---

## 🧩 Projects

### S.F.D | Smart Factory Defect Detection
`Python` `Inception-ResNet-v2` `FastAPI` `AWS S3` `SSE` `Docker` `Jenkins`

- ImageNet 사전학습 모델 기반 전이학습·파인튜닝과 데이터 증강 수행
- 학습률·Batch Size·Epoch 등 학습 조건을 조정해 **Accuracy 92% 이상** 달성
- Accuracy와 Confusion Matrix로 정상/불량 오분류 방향까지 검증
- **이미지 촬영 → S3 저장/이벤트 기반 AI 처리 → AI 분석 완료 → 결과 이벤트 → SSE로 프론트 전달**
- 합의된 아키텍처에 맞춰 인프라 및 CI/CD 환경 구축

### SSMART OFFICE
`Spring Boot` `React` `Docker` `Jenkins` `AWS`

- 인사 관리를 위한 올인원 서비스
- Docker 기반 MSA 배포 환경과 Jenkins 기반 CI/CD 구축
- 서비스별 배포 흐름을 정리하고 빌드·배포 과정 개선

### 0CHA
`Spring Boot` `WebSocket` `STOMP` `JWT` `Docker` `Jenkins`

- WebSocket·STOMP 기반 실시간 채팅 기능 개발
- WebSocket 전용 인증 인터셉터를 구현해 JWT 인증 흐름 보완
- Docker 기반 배포 환경 및 Jenkins CI/CD 구축

---

## 🛠 Tech Stack

### Back-End
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![C%23](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![ASP.NET](https://img.shields.io/badge/ASP.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

### Front-End
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

### Database
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

### Infra & DevOps
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

---

## 📜 Certifications

- 정보처리기사
- SQLD
- AWS Certified Cloud Practitioner
- 리눅스마스터 2급

---

## 🤝 How I Work

- **전체 흐름에서 원인을 찾습니다.** 특정 코드나 SQL만 보지 않고 데이터가 생성되고 처리되는 구조를 함께 분석합니다.
- **정상 동작을 넘어 예외 상황까지 검증합니다.** 동시 요청과 운영 데이터 등 실제 환경의 조건을 고려합니다.
- **사용자의 업무를 먼저 이해합니다.** 요구사항 자체보다 왜 필요한지와 실제 사용 흐름을 확인합니다.
- **공동의 목표를 기준으로 협업합니다.** 의견이 다를 때 프로젝트 목표와 객관적인 기준을 바탕으로 방향을 선택합니다.

<br/>

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-SangCheonP-181717?style=flat-square&logo=github)](https://github.com/SangCheonP)

</div>
