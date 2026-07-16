# Drive - Ü

> 운전면허교육 및 발급시스템

운전면허 필수교육인 교통안전교육과 면허 발급을 한 곳에서 처리할 수 있는 **원스톱 운전면허 시스템**입니다.
사용자가 온라인으로 교통안전교육을 이수하고 관련 학습을 통한 비용절감이 가능하고 전체적인 면허 절차를 확인하고 사용할 수 있습니다.
사용자가 필수 학과 교육 이수 후 순차적으로 각 시험을 응시 및 합격하여 최종적으로 운전면허 발급 신청까지 가능하도록 구현했습니다.

<br>

## 프로젝트 개요

| 항목 | 내용 |
| :--- | :--- |
| **프로젝트명** | Drive - Ü |
| **팀명** | Green - Light |
| **개발 기간** | 2026.05.07 ~ 2026.06.04 (약 1개월) |
| **팀 구성** | 7인 |
| **소속** | DW아카데미 메타버스 에듀테크 개발자트랙 11회차 |

<br>

## 프로젝트 선정 배경

> 현행 운전면허 교통안전교육에 대한 사용자의 불만족이 높은 문제를 인식했습니다.
> 그 원인으로는 높은 운전면허학원 비용, 비효율적인 학과교육, 기능시험 및 도로주행의 연수 부족이 주를 이뤘습니다.
> 실질적인 교육의 질 확보, 3D Unity 기반의 기능시험 및 도로주행 코스 시뮬레이션을 통해 문제를 해결하고자 했습니다.

<br>

## 프로젝트 목표

- 사용자에게 **필수 교통안전교육의 온라인 제공**
- 교통안전교육 > 학과시험 응시 > 신체검사 > 기능시험 > 도로주행 > 운전면허 발급신청의  **운전면허 취득 절차 안내** 구현
- **Spring Security** 기반 역할별 접근 제어
- 사용자의 편의를 위한 **시험장별 혼잡도 예측 서비스** 구현
- 기능시험 및 도로주행 코스의 **3D Unity 시뮬레이터** 구현

<br>

## 기술 스택

### Backend
- Java 17
- Spring Boot
- Spring Security
- JPA
- Lombok

### Frontend
- HTML / CSS / JavaScript
- Thymeleaf

### Database
- Maria DB

### Infra & Tool
- Tomcat
- IntelliJ
- Notion (협업)
- GitHub (버전 관리)

<br>

## 팀 소개 및 역할 분담

| GitHub | 직책 | 담당 영역 |
| :--- | :--- | :--- |
| 차진안 | **PM** | 프로젝트 총괄 및 일정 관리, 전체 시스템 흐름 정의, **Unity 도로주행 기능 개발** |
| [@KGyeongSu](https://github.com/KGyeongSu) | **AA** | 개발환경 수립, 면허 취득 절차 개발, 합격자 처리 및 시험 일정 등록 개발, **Spring Security 설계** |
| [@jini9786](https://github.com/jini9786) | **UA** | UI 설계, **길 안내** 개발 |
| 방윤상 | **UA** | UI 설계, **Unity 기능시험 개발** |
| [@SangWoo1124](https://github.com/SangWoo1124) | **TA** | 네트워크 및 보안 설계, **Spring Security 설계**, 면허증 발급 절차 개발, 최신법규 백업, 모의 CBT 등록 개발 |
| [@eun00000](https://github.com/eun00000) | **BA** | 요구사항 분석 및 정의, 일정관리, **시험장 혼잡도 예측 서비스 개발**, 챗봇 개발, 문의사항 및 공지사항 백업, 교육 이수현황 확인 개발 |
| [@jeoninsu99](https://github.com/jeoninsu99) | **DA** | 테이블 설계, **교통안전교육 및 학습영상 시청 및 등록 기능 개발**, 모의 CBT 기능 개발 |



<br>

## 권한 체계

| 권한 | 설명 |
| :--- | :--- |
| **관리자 (ADMIN)** | 교통안전교육 및 학습영상 등록 및 관리, 모의 CBT 등록, 사용자 현황 관리, 시험일정 등록, 고객센터 운영 |
| **사용자 (MEMBER / SOCIALMEMBER))** | 교통안전교육 및 학습영상 이수, 모의 CBT 응시, 기능시험 및 도로주행 시뮬레이션 활용, 운전면허시험 신청 |

<br>

## 주요 기능

### 공통 기능 (메인 / 게시판)
- **메인 페이지**: 한반도 지도 기반의 시험장 혼잡도 예측 서비스, 챗봇, Drive - Ü 최근 소식
- **로그인 / 회원가입**: Spring Security 기반 인증, BCrypt 암호화

### 사용자
- **학습영상**: 교통안전교육 및 학습영상 시청
- **모의 CBT**: 4지선다의 랜덤 40문항, 결과 및 해설 확인
- **기능시험 및 도로주행 시뮬레이터**: 3D Unity 기반의 기능시험 및 도로주행 코스 경험
- **고객센터**: 문의사항 등록 및 답변 확인, 공지사항 및 최신법규를 통한 정보 취득, 길안내를 통한 시험장 위치 확인

### 관리자 대시보드
- **고객센터**: 문의사항 답변 등록, 공지사항 및 최신법규 등록 및 관리
- **사용자 현황 관리**: 사용자의 단계별 진척도 확인 및 검색, 총 사용자 수 / 교통교육 이수율, 시험접수 건수, 시험 합격자 수 확인
- **합격자 처리**: 사용자의 점수 입력을 통한 합격 처리 가능
- **학습영상 등록**: 유튜브 URL Embedded 형식을 통한 수정 및 등록 관리
- **CBT 등록**: CSV 파일 등록을 통한 CBT 등록 및 수정
- **시험일정 등록**: 캘린더를 통한 시험일정 현황 확인 및 시험 일괄 등록

<br>

## DB 설계 (총 34개 테이블)

| 분류 | 테이블 |
| :--- | :--- |
| 사용자 | `MEMBER`, `SOCIAL_MEMBER` |
| 학습영상 | `CHAPTER_PROGRESS`, `CHAPTER_QUIZ`, `CHAPTER_QUIZ_ANSWER`, `CHAPTER_QUIZ_CHOICE`, `CHAPTER_QUIZ_SUMMISSION`,`VIDEO_CHAPTER`, `VIDEO_COURSE`, `VIDEO_PROGRESS` |
| CBT 등록 및 응시 | `CBT_EXAM`, `CBT_EXAM_QUESTION`, `CBT_CHOICE`, `CBT_RESULT`, `CBT_CORRECT_ANSWER` |
| 시험일정 등록 및 관리 | `EXAM_SCHEDULE`, `TEST_CENTER` |
| 면허시험 신청 | `APPLICATION` |
| 면허증 신청 | `EXTERNAL_LICENSE_STATUS`, `LICENSE_APPLICATION`, `USER_LICENSE` |
| 결제처리 | `LICENSE_PAYMENT`, `PAYMENT` |
| 시험장 혼잡도 예측 | `DRIVER_LICENCE_EXAM_STATS`, `DRIVER_LICENCE_ISSUE_STATS` |
| 합격 및 불합격 처리 | `EXAM_FAIL`, `EXAM_PASS` |
| 고객센터 및 기타 | `QUESTION`, `LAWS`, `LAWS_FILE`, `NOTICE`, `NOTICE_FILE`, `EXAM_PASS`, `PRACTICE_LICENSE` |

<br>

## 프로젝트 구조

```
src/main/java/com/zerock/driveu/
├── controller/   # [요청] 클라이언트의 HTTP 요청을 받고 응답을 제어
├── service/      # [로직] 비즈니스 로직 처리 (가장 핵심적인 기능 수행)
├── repository/   # [데이터] DB와 직접 소통하여 데이터 CRUD 수행
├── domain/       # [모델] 데이터베이스 테이블과 1:1 매핑되는 객체
└── dto/          # [전달] 계층 간 이동하는 순수 데이터 객체
└── .gitignore
```

<br>

## 실행 방법

### 사전 요구사항
- Java 17, IntelliJ, Maria DB

### 실행 방법
1. 저장소를 클론합니다
2. IntelliJ에서 Import 합니다
3. `application-local.yaml'을 본인 환경에 맞게 수정합니다

<br>

## 회고 / 향후 개선 방향

### 회고
- 팀 프로젝트에서 GitHub를 활용해 **브랜치 관리와 코드 병합**의 과정을 수월하게 진행
- 역할 분담을 통해 각자의 파트를 책임지고 하나의 시스템으로 통합하는 과정을 학습
- Spring Boot, Security, JPA 등 수업에서 배운 내용을 실제 프로젝트에 적용해 이해도를 높일 수 있었음

### 향후 개선 방향
- Unity 그래픽 리소스 최적화 및 고도화
- 특수면허 컨텐츠 확보
- 모의고사 CBT 등록 파일 확장 (EXCEL 등)
- 챗봇 API 서비스 연동 최적화
