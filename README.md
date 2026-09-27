![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=220&section=header&text=SangCheon%20Park&fontSize=62&fontAlignY=38&desc=Software%20Developer&descAlignY=58&descSize=20)

<div align="center">

### 👋 문제를 분석하고 개선하여 가치를 만드는 개발자 박상천입니다.

생산·품질 시스템과 MES를 개발·운영하며  
**업무 흐름과 데이터 처리 구조를 이해하고, 성능·정합성·운영 안정성을 개선해왔습니다.**

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-PDF-181717?style=flat-square&logo=adobeacrobatreader&logoColor=white)](https://github.com/SangCheonP/dev-portfolio/blob/main/dev-portfolio.pdf)

</div>

---

## 👨‍💻 소개

> **제조 IT · 풀스택 · 데이터/SQL 최적화 · CI/CD**

- 🏭 반도체 생산·품질 시스템 **SSPS 개발 및 운영**
- ⚙️ 제조 현장 **MES 풀스택 개발**
- 📊 Oracle SQL·PL/SQL 기반 **데이터 처리 및 성능 개선**
- 🔒 동시 요청 환경을 고려한 **데이터 정합성 및 동시성 제어**
- ☁️ Docker·Jenkins 기반 **배포 환경 및 CI/CD 구축**
- 🤖 AI 이미지 분석 시스템의 **이벤트 기반 처리 구조 및 인프라 구축**

---

## 💼 경력

### 노리시스템 · 소프트웨어 개발자
**2025.03 — 현재**

#### SSPS · Samsung Semiconductor Smart Production System
**2025.03 — 2026.05 · 2026.09 — 현재**

> **역할** · 풀스택 개발 · Oracle SQL/PLSQL · 성능 개선  
> **기술** · `C#` `ASP.NET` `Oracle` `PL/SQL` `JavaScript` `RealGrid2` `ECharts`

> 반도체 생산·품질 데이터를 조회·관리하고, 운영 중 발생하는 성능과 데이터 처리 문제를 개선

- Inbay 재공 현황, 기준정보, 품질 대시보드 등 **화면·API·DB 기능 개발**
- 약 **28만 건 Carrier + 2.5만 건 WIP → 2만 건 Inbay 데이터**의 적재 흐름을 분석해 불필요한 JOIN·GROUP BY·MAX 연산을 제거하고 **적재 시간 약 3분 → 1분 20초, 55% 단축**
- 운영 중 발생한 **데이터 오류 원인을 분석·정상화**하고, 현업 요구사항을 반영해 기능 개선
- 운영 반영 시 프로그램·DB 변경사항, 데이터 보정 SQL, 적용 순서와 검증 항목을 확인하는 절차 정립

<br/>

#### MES · 제조 현장 MES/WMS 구축
**2026.06 — 2026.08**

> **역할** · 풀스택 개발 · WMS 개발 · 요구사항 개선  
> **기술** · `Java` `Spring Boot` `React` `PostgreSQL`

> 제조 현장의 자재 이동과 작업 흐름을 관리하고, 실제 사용자 요구사항을 반영해 기능을 개선

- 작업지시, LOT Split·Merge, 위치 이동 등 **MES/WMS 기능 개발**
- 실제 사용자 업무 흐름을 확인해 Split·Merge 기능을 **한 화면에서 연속 처리**하도록 개선
- 채번 테이블에 **Row Lock + Commit** 기반 동시성 제어를 적용해 ID 중복 방지
- 2대의 PC에서 동시 요청을 발생시켜 Lock/Commit 동작과 중복 미발생 검증

---

## 🚀 프로젝트

### [SSMART OFFICE](https://github.com/SangCheonP/SSMART-OFFICE)
**2024.10.14 — 2024.11.22**

> **역할** · 인프라 · CI/CD  
> **기술** · `Docker` `Docker Compose` `Jenkins` `AWS EC2`

> 인사 관리를 위한 올인원 서비스

- Docker Compose 기반 **MSA 배포 환경** 구축
- Jenkins 기반 **CI/CD 파이프라인** 구축
- Config Server와 Discovery Server 상태 확인을 위한 Docker Health Check 구성

<br/>

### [S.F.D · Smart Factory Defect Detection](https://github.com/SangCheonP/S.F.D)
**2024.08.16 — 2024.10.11**

> **역할** · 인프라 · CI/CD · AI 모델 학습  
> **기술** · `Python` `Inception-ResNet-v2` `AWS S3` `SSE` `Docker` `Jenkins`

> 제조 이미지를 AI로 분석해 정상·불량을 판별하고 결과를 제공하는 시스템

- ImageNet 사전학습 모델 기반 **전이학습·파인튜닝 및 데이터 증강** 수행
- 학습률·Batch Size·Epoch 등을 조정해 **Accuracy 92% 이상** 달성
- Accuracy와 Confusion Matrix로 정상/불량의 **오분류 방향까지 검증**
- **이미지 촬영 → S3 저장/이벤트 기반 AI 처리 → AI 분석 완료 → 결과 이벤트 → SSE로 프론트 전달**
- 합의된 아키텍처에 맞춰 **Docker·Jenkins 기반 인프라 및 CI/CD 환경 구축**

<br/>

### [0CHA](https://github.com/SangCheonP/0CHA)
**2024.07.01 — 2024.08.16**

> **역할** · 인프라 · 백엔드 · 실시간 채팅  
> **기술** · `Spring Boot` `WebSocket` `STOMP` `JWT` `Docker` `Jenkins`

> 운동 루틴·기록 관리, 피드, AI 자세 교정, 중고거래 기능을 제공하는 헬스 관리 플랫폼

- WebSocket·STOMP 기반 **실시간 채팅 기능 개발**
- HTTP JWT 인증만으로 처리되지 않던 WebSocket 연결 인증을 별도 인터셉터로 분리해 **401 오류 해결**
- Docker 기반 배포 환경 및 Jenkins CI/CD 구축

<br/>

### 추가 프로젝트

- **[알바닷컴](https://github.com/kw-ic-web/23-teampjt-webssulme)** — Spring Boot 기반 API 개발 및 Docker·GitHub Actions 기반 CI/CD 환경 구축
- **[Kampus](https://github.com/SangCheonP/KWU-Kampus)** — 대학 생활을 위한 웹 서비스 개발 및 Tomcat·GitHub Actions 기반 배포 자동화
- **[OfficetelLink](https://github.com/SangCheonP/OfficetelLink)** — 월세 정보·게시판·마이페이지·메일 인증 기능을 제공하는 웹 서비스 개발

---

## 🛠 기술 스택

<table>
<tr>
<td><b>백엔드</b></td>
<td>
<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" />
<img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/ASP.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
</td>
</tr>
<tr>
<td><b>프론트엔드</b></td>
<td>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
</td>
</tr>
<tr>
<td><b>데이터베이스</b></td>
<td>
<img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
</td>
</tr>
<tr>
<td><b>인프라 / DevOps</b></td>
<td>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
</td>
</tr>
</table>

---

## 🎓 교육

| 기간 | 내용 |
| :---: | --- |
| **2024.02** | 광운대학교 소프트웨어학부 졸업 |
| **2024.01 — 2024.12** | 삼성 청년 SW 아카데미(SSAFY) 11기 · **1,600시간** |

---

## 📜 자격증

| 취득일 | 자격증 |
| :---: | --- |
| **2025.01** | AWS Certified Cloud Practitioner |
| **2025.01** | 리눅스마스터 2급 |
| **2024.09** | 정보처리기사 |
| **2024.06** | SQLD |

---

## 🤝 업무 방식

| | |
| --- | --- |
| 🔍 **전체 흐름에서 원인을 찾습니다.** | 특정 코드나 SQL만 보지 않고 데이터가 생성되고 처리되는 구조를 함께 분석합니다. |
| ✅ **예외 상황까지 검증합니다.** | 동시 요청과 운영 데이터 등 실제 환경에서 발생할 수 있는 조건을 고려합니다. |
| 👥 **사용자의 업무를 먼저 이해합니다.** | 요구사항 자체보다 왜 필요한지와 실제 사용 흐름을 확인합니다. |
| 🤝 **공동의 목표를 기준으로 협업합니다.** | 의견이 다를 때 프로젝트 목표와 객관적인 기준을 바탕으로 방향을 선택합니다. |
