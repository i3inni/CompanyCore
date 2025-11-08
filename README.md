![header](https://capsule-render.vercel.app/api?type=rect&color=auto&height=250&section=header&text=CompanyCore%20(Client)&fontSize=70)

> JavaFX 기반 기업용 그룹웨어 데스크톱 애플리케이션 (팀 스터디)

<br>

## :open_book: 목차
- [프로젝트 소개](#프로젝트-소개)
- [👤 저의 기여](#-저의-기여)
- [🛠️ 기술 스택](#-기술-스택)
- [📁 프로젝트 구조](#-프로젝트-구조)
- [🔗 관련 레포지토리](#-관련-레포지토리)

<br>

<a id="프로젝트-소개"></a>
## 📋 프로젝트 소개

**CompanyCore**는 풀스택 개발 역량 함양을 위한 **팀 스터디** 프로젝트로, JavaFX로 구축된 기업용 그룹웨어 데스크톱 클라이언트입니다.

이 애플리케이션은 `companycoreserver`(백엔드)와 REST API로 통신하여 사용자 인증, 근태 관리, 메일, 전자 결재, 일정 관리 등 사내 시스템의 핵심 기능을 사용자에게 GUI로 제공합니다.

### 🚀 주요 기능
- **인증:** 로그인 및 토큰 기반 세션 관리
- **메인:** 홈 대시보드
- **근태 관리:** 출퇴근 기록, 휴가 신청 및 승인 현황 조회
- **메일:** 수신/발신 메일함, 메일 작성 및 조회
- **업무:** 전자 결재 요청/승인, 공지사항, 회의록 조회
- **캘린더:** 개인 및 공용 일정 관리
- **인사 관리:** 직원 정보 조회 및 관리 (관리자)

<br>

<a id="-저의-기여"></a>
## 👤 저의 기여

저는 이 풀스택 스터디 프로젝트에서 **클라이언트(프론트엔드) 개발**을 전반적으로 담당했습니다.

* **UI/UX 구축:** **JavaFX**와 FXML을 사용하여 로그인, 메인 대시보드, 근태 관리, 메일, 업무, 캘린더 등 **대부분의 페이지 UI를 구축**하고 화면 레이아웃을 설계했습니다.
* **API 연동:** `companycoreserver`의 REST API와 연동하여 JSON 데이터를 파싱하고, JavaFX 컴포넌트에 데이터를 바인딩하는 로직을 구현했습니다.
* **네비게이션 설계:** `MainController`와 `SidebarController`를 중심으로 화면 간의 네비게이션 로직을 설계하고 구현했습니다.

<br>

<a id="-기술-스택"></a>
## 🛠️ 기술 스택

| 구분 | 기술 |
|------|------|
| **Core** | ![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white) ![JavaFX](https://img.shields.io/badge/JavaFX-F29111?style=for-the-badge&logo=openjfx&logoColor=white) |
| **UI** | FXML, ControlsFX, FormsFX, TilesFX |
| **API/Util** | ![Jackson](https://img.shields.io/badge/Jackson-D00000?style=for-the-badge&logo=json&logoColor=white) (JSON Parsing) |
| **Build** | ![Apache Maven](https://img.shields.io/badge/Apache_Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white) |

<br>

<a id="-프로젝트-구조"></a>
## 📁 프로젝트 구조
```bash
src/main/
├── java/com/example/companycore/
│   ├── Main.java                   # JavaFX 애플리케이션 시작점
│   ├── controller/
│   │   ├── core/
│   │   │   ├── MainController.java     # 메인 컨텐츠 영역 컨트롤러
│   │   │   ├── LoginController.java    # 로그인 화면 컨트롤러
│   │   │   └── SidebarController.java  # 사이드바 네비게이션
│   │   ├── attendance/             # 근태관리
│   │   ├── calendar/               # 캘린더
│   │   ├── hr/                     # 인사관리
│   │   ├── mail/                   # 메일
│   │   └── tasks/                  # 업무
│   ├── model/
│   │   └── dto/                    # API 통신용 DTO
│   └── service/
│       ├── ApiClient.java          # API 클라이언트
│       └── ...
└── resources/com/example/companycore/
    ├── view/
    │   ├── loginView.fxml
    │   ├── mainDashBoardView.fxml
    │   ├── sidebar.fxml
    │   └── content/                # MainController가 로드하는 영역
    │       ├── homeContent.fxml
    │       ├── attendanceRecordContent.fxml
    │       ├── calendarContent.fxml
    │       ├── hrManagementContent.fxml
    │       ├── mailContent.fxml
    │       └── tasksContent.fxml
    └── images/
