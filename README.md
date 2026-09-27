![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=220&section=header&text=SangCheon%20Park&fontSize=62&fontAlignY=38&desc=Software%20Developer&descAlignY=58&descSize=20)

<div align="center">

### 안녕하세요. 시스템의 흐름을 이해하고 문제를 직접 개선해온 개발자 박상천입니다.

생산·품질 시스템과 MES를 개발·운영하면서 화면 구현부터 API, DB 로직까지 직접 다뤄왔습니다.  
특히 운영 중 발생하는 성능 저하, 데이터 중복, 동시성 문제를 원인부터 확인하고 개선하는 일을 좋아합니다.

</div>

---

## About Me

현재 노리시스템에서 반도체 생산·품질 시스템을 개발하고 있습니다.  
주로 C#/ASP.NET과 Oracle을 사용하며, 화면·API·프로시저를 함께 개발하고 있습니다.

외부 MES 구축 프로젝트에서는 Java/Spring Boot, React, PostgreSQL을 사용해 제조 현장의 작업 흐름을 직접 확인하면서 기능을 구현했습니다.

개인·팀 프로젝트에서는 Docker, Jenkins, AWS를 활용한 배포 환경과 CI/CD를 꾸준히 경험했고, 최근에는 Oracle 실행계획과 SQL 튜닝을 더 깊게 공부하고 있습니다.

---

## Experience

### NORISYSTEM · Software Developer
**2025.03 — Present**

#### SSPS · Samsung Semiconductor Smart Production System
**2025.03 — 2026.05 · 2026.09 — Present**  
`C#` `ASP.NET` `Oracle` `PL/SQL` `JavaScript` `RealGrid2` `ECharts`

반도체 생산·품질 데이터를 조회하고 관리하는 SSPS를 개발·운영하고 있습니다.

- Inbay 재공 현황, 기준정보 관리, 품질 대시보드 등 화면과 API 개발
- Oracle 프로시저와 SQL을 이용한 데이터 조회·적재 로직 개발
- 약 **28만 건의 Carrier 데이터와 2.5만 건의 WIP 데이터를 연계해 약 2만 건의 Inbay 데이터를 생성하는 적재 로직** 분석
- UI 필터 값을 가져오기 위해 사용하던 FLT 테이블 JOIN으로 중간 데이터가 증가하고 GROUP BY, MAX 연산까지 수행되는 구조 확인
- 필요한 쿼리를 DB에 관리하고 적재 시 동적으로 실행하도록 변경해 불필요한 JOIN과 연산 제거
- 데이터 적재 시간을 **약 3분에서 1분 20초로 단축(약 55%)**
- 기준정보 변경 이력을 남기기 위한 Oracle Trigger와 로그 테이블 운영
- 운영 반영 시 프로그램 변경, DB 변경, 기존 데이터 보정 SQL, 적용 순서, 반영 후 확인 항목을 체크하며 배포

#### MCS MES · 제조 현장 MES/WMS 구축
**2026.06 — 2026.08**  
`Java` `Spring Boot` `React` `PostgreSQL`

외부 고객사 제조 현장에 상주하며 MES와 연계되는 WMS 기능을 개발했습니다.

- 작업지시, LOT Split·Merge, 위치 이동, 자재 입·출고 등 화면과 API 개발
- 처음에는 LOT Split과 Merge를 각각 다른 화면으로 구현했으나, 현장 사용자가 두 작업을 연속해서 수행하는 경우가 많다는 피드백을 받아 한 화면에서 처리할 수 있도록 변경
- LOT Split 후 부모 LOT의 QR을 다시 출력하려면 조회 화면으로 이동해야 했던 과정을 개선해 부모·자식 LOT QR을 같은 화면에서 출력하도록 구현
- 작업지시와 LOT Split ID 채번 과정에서 동시 요청 시 같은 번호가 생성될 가능성을 확인
- 채번 테이블의 한 행을 **Row Lock**으로 잠근 뒤 번호를 갱신하고 Commit 시 Lock을 해제하는 방식으로 변경
- 두 대의 PC에서 같은 시점에 요청을 발생시켜 채번 순서와 중복 여부를 직접 확인

---

## Projects

### [S.F.D · Smart Factory Defect Detection](https://github.com/SangCheonP/S.F.D)
**2024.08.16 — 2024.10.11**  
`Python` `Inception-ResNet-v2` `FastAPI` `AWS S3` `SSE` `Docker` `Jenkins`

제조 공정에서 촬영한 이미지를 AI로 분석하고, 정상·불량 판별 결과를 화면에 전달하는 프로젝트입니다.

- ImageNet 사전학습 Inception-ResNet-v2를 기반으로 전이학습 진행
- 기존 top layer를 제거하고 정상/불량 분류에 맞는 분류 layer 구성
- 데이터 증강과 학습률, Batch Size, Epoch을 조정하며 학습
- Accuracy와 Confusion Matrix를 확인하면서 정상·불량이 어떤 방향으로 오분류되는지 비교
- 모델 정확도 **92% 이상** 달성
- 처리 흐름은 **이미지 촬영 → S3 저장/이벤트 기반 AI 처리 → AI 분석 완료 → 결과 이벤트 → SSE로 프론트 전달** 방식으로 구성
- 아키텍처를 정하는 과정에서 백엔드가 이미지를 직접 AI 서버로 전달하는 방식과 S3 이벤트 기반 방식을 비교
- 이미지 생성부터 결과 반환까지의 흐름과 전달 단계를 기준으로 팀원과 구조를 검토한 뒤 S3 이벤트 기반 방식으로 결정
- 결정된 구조에 맞춰 Docker, Jenkins, Nginx 기반 인프라와 CI/CD 환경 구축
- SSE 결과 전달 과정에서 Nginx buffering으로 응답이 바로 전달되지 않는 문제를 확인하고 proxy buffering 설정을 조정

<br/>

### [SSMART OFFICE](https://github.com/SangCheonP/SSMART-OFFICE)
**2024.10.14 — 2024.11.22**  
`Spring Boot` `React` `Docker` `Jenkins` `AWS`

인사 정보와 근태, 복지 기능을 관리하는 사내 HR 서비스 프로젝트입니다.

- 약 12개의 서비스를 Docker Compose 기반으로 구성
- Config Server와 Discovery Server를 포함한 서비스 배포 환경 구축
- Jenkins에서 변경된 서비스를 기준으로 빌드·배포하도록 구성
- 서비스별 순차 빌드 구조를 병렬화해 전체 빌드 시간을 약 **4분에서 2분 수준으로 단축**
- Config Server와 Discovery Server의 상태를 확인하기 위한 Docker Health Check 구성

<br/>

### [0CHA](https://github.com/SangCheonP/0CHA)
**2024.07.01 — 2024.08.16**  
`Spring Boot` `WebSocket` `STOMP` `JWT` `Docker` `Jenkins`

사용자 간 실시간 채팅 기능을 포함한 웹 서비스 프로젝트입니다.

- WebSocket·STOMP 기반 1:1 채팅 기능 개발
- 기존 HTTP JWT 인증 로직만으로는 WebSocket 연결 시 인증이 처리되지 않아 401 오류 발생
- WebSocket 연결 과정에서 토큰을 검증할 수 있도록 별도의 인증 인터셉터 구현
- 채팅 메시지 중복 저장을 방지하고 로그를 통해 메시지 흐름을 추적하도록 처리
- Docker 기반 배포 환경과 Jenkins CI/CD 구성

---

## Tech Stack

<table>
<tr>
<td><b>Back-End</b></td>
<td>
<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" />
<img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/ASP.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
</td>
</tr>
<tr>
<td><b>Front-End</b></td>
<td>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
</td>
</tr>
<tr>
<td><b>Database</b></td>
<td>
<img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
</td>
</tr>
<tr>
<td><b>Infra / DevOps</b></td>
<td>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
</td>
</tr>
</table>

---

## Certifications

| 취득일 | 자격증 |
| :---: | --- |
| **2025.01** | AWS Certified Cloud Practitioner |
| **2025.01** | 리눅스마스터 2급 |
| **2024.09** | 정보처리기사 |
| **2024.06** | SQLD |

---

## What I Focus On

프로젝트를 진행할 때 기능이 동작하는 것에서 끝내지 않고, 실제 운영 환경에서 문제가 생길 수 있는 부분을 한 번 더 확인하려고 합니다.

- SQL이 느리면 실행계획만 보는 데서 끝내지 않고 데이터가 생성되고 적재되는 전체 흐름을 확인합니다.
- 여러 사용자가 동시에 요청할 수 있는 기능은 동시성 문제가 없는지 직접 테스트합니다.
- 요구사항이 불편해 보여도 바로 고치기보다 현장에서 실제로 어떤 순서로 사용하는지 먼저 확인합니다.
- 팀에서 의견이 다르면 개인의 선호보다 처리 시간, 단계 수, 운영 방식처럼 비교할 수 있는 기준을 먼저 정합니다.

<br/>

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-SangCheonP-181717?style=flat-square&logo=github)](https://github.com/SangCheonP)

</div>
