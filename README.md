# ⏱️ TOPIK II Digital Examination & Proctoring Dashboard
> **Official TOPIK II Real-time Exam Clock, Automated Stage Countdown & Proctoring Management System**  
> *Bilingual (Uzbek & Korean) | Optimized for Classroom Projectors & Exam Auditoriums*

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://en.wikipedia.org/wiki/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://en.wikipedia.org/wiki/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://en.wikipedia.org/wiki/JavaScript)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

---

## 📌 English Documentation

### 🌟 Overview
The **TOPIK II Digital Examination & Proctoring Dashboard** is a web-based, standalone digital proctoring solution built specifically for administering official **TOPIK II (Test of Proficiency in Korean)** examinations.

Designed for high-visibility display on classroom projectors, large TV monitors, and proctoring stations, it provides real-time timekeeping, automated exam-stage transitions, time warnings, answer sheet previews, and examination rules equipped with bilingual AI audio narration.

---

### ✨ Key Features

- **🕒 Real-time Synchronized Digital Clock & Stage Countdown**
  - High-precision digital clock (`HH:MM:SS`) tracking the exact local exam time.
  - Dynamic countdown timer displaying remaining time for each exam stage.
  - High-contrast typography designed for readability from the back of large examination halls.

- **📅 Official TOPIK II Timetable Integration**
  - **Preparation & Room Entry**: `09:20 – 09:40` (20 min)
  - **Session 1 — Listening (Eshitish / 듣기)**: `09:40 – 10:40` (60 min, 50 questions)
  - **Session 1 — Writing (Yozish / 쓰기)**: `10:40 – 11:30` (50 min, 4 questions)
  - **Intermission / Break (Tanaffus / 휴식)**: `11:30 – 11:50` (20 min)
  - **Session 2 Room Entry & Preparation**: `11:50 – 12:00` (10 min)
  - **Session 2 — Reading (O'qish / 읽기)**: `12:00 – 13:10` (70 min, 50 questions)
  - **Exam Conclusion**: `13:10` onwards

- **⚠️ Automated Visual & Countdown Alerts**
  - **10-minute warning**: Visual alert notification at 10 minutes remaining.
  - **5-minute warning**: Visual alert notification at 5 minutes remaining.
  - **2-minute final countdown**: Full 2-minute countdown banner (`Listening/Writing/Reading ending soon...` / `듣기/쓰기/읽기 시험 종료 임박...`) with pulsing red alert styling until the section concludes.

- **🌐 Instant Bilingual Toggle (Uzbek 🇺🇿 / Korean 🇰🇷)**
  - Seamless one-click switching between Uzbek and Korean for all headings, exam stages, timetables, rules, and alert messages.

- **📝 Interactive Answer Sheet Guide**
  - Detailed instructions on completing OMR answer sheets and handwriting fields.
  - Built-in full-screen zoom preview for sample OMR sheets.

- **📢 Proctoring Rules & Built-in AI Audio Narration**
  - Categorized list of exam violations and disqualification penalties (immediate voiding, 2-year ban, 4-year ban).
  - Integrated audio player bar (**Play ▶**, **Pause ⏸**, **Stop ⏹**, elapsed timer, and live status badge).
  - High-quality AI voice narration in both Uzbek and Korean.
  - Clean floating layout placed conveniently beside the Zoom/Close button to guarantee 100% unobstructed text readability.

- **🛠️ Interactive Testing & Simulation (Demo Panel)**
  - Concealed/collapsible simulation control bar to test any stage of the exam in real-time.
  - One-click presets for all milestones (`09:40`, `10:00`, `10:38`, `10:40`, `11:00`, `11:20`, `11:25`, `11:28`, `11:30`, `11:50`, `12:00`, `12:30`, `13:00`, `13:05`, `13:08`, `13:10`).
  - Custom time machine input with live second-by-second forward progression.
  - "Non-Exam Day" indicator mode.

- **⚙️ Dynamic Configuration (`config.js`)**
  - Adjust exam round number (e.g. `108`, `109`, `110`) and target exam date (`DD.MM.YYYY`) simply by editing a lightweight configuration file in any text editor.

---

### 🕒 Official TOPIK II Examination Schedule

| Period | Time | Duration | Subject / Stage | Details |
| :---: | :---: | :---: | :--- | :--- |
| **Prep** | `09:20 - 09:40` | 20 min | Room Entry & ID Check | Candidate entry, seating & instructions |
| **Session 1** | `09:40 - 10:40` | 60 min | **Listening (듣기)** | 50 Questions (Q1 - Q50) |
| **Session 1** | `10:40 - 11:30` | 50 min | **Writing (쓰기)** | 4 Questions (Q51 - Q54) |
| **Break** | `11:30 - 11:50` | 20 min | Intermission / Rest | Restroom & hallway break |
| **Prep** | `11:50 - 12:00` | 10 min | Session 2 Room Entry | Re-entry & reading material distribution |
| **Session 2** | `12:00 - 13:10` | 70 min | **Reading (읽기)** | 50 Questions (Q1 - Q50) |
| **End** | `13:10` | — | **Exam Finished** | Collection & verification of answer sheets |

---

### 📂 Directory Structure

```text
topik2.ukiu.uz/
├── index.html               # Main application (UI, countdown engine, audio player)
├── config.js                # Dynamic configuration (Exam Round & Date)
├── README.md                # Project documentation (English & Korean)
├── 404.html                 # Custom 404 error page
├── 502.html                 # Custom 502 error page
├── .htaccess                # Apache server configuration & MIME settings
├── .user.ini                # PHP/Server runtime settings
└── index.files/             # Static media assets
    ├── answer-sheet-uz.jpg  # OMR sample answer sheet image
    ├── image001.jpg         # Visual guideline / diagram
    ├── rules-audio-uz.mp3   # Uzbek AI voice narration of exam rules
    └── rules-audio-ko.mp3   # Korean AI voice narration of exam rules
```

---

### 🚀 Getting Started

#### 1. Configuration
Open `config.js` in any code or text editor (e.g., Notepad, VSCode):
```javascript
window.CONFIG = {
  TOPIK: "109",              // Exam round number
  TOPIK_DATE: "27.10.2026"   // Exam date in DD.MM.YYYY format
};
```

#### 2. Running Locally
Simply double-click `index.html` or open it with any modern web browser (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari). No backend server or database setup is required.

#### 3. Running with a Local Server (Recommended for audio testing)
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (npx serve)
npx serve .
```
Then navigate to `http://localhost:8000` in your browser.

#### 4. Deployment
Upload all repository files to any web hosting service, VPS, or static hosting platform (GitHub Pages, Vercel, Netlify, Apache, Nginx, or cPanel).

---

### 💻 Tech Stack
- **Frontend**: Pure Vanilla JavaScript (ES6+), Semantic HTML5, Modern CSS3 (CSS Grid, Flexbox, Clamp typography)
- **Audio**: HTML5 Web Audio API
- **Dependencies**: 0 external libraries or frameworks (100% lightweight and dependency-free)

---
---

## 📌 한국어 설명 (Korean Documentation)

### 🌟 프로젝트 소개
**TOPIK II 실시간 시험장 타이머 및 감독 대시보드**는 한국어능력시험(TOPIK II) 고사장에서 수험생과 시험 감독관을 위해 개발된 웹 기반 디지털 타이머 및 감독 관리 시스템입니다.

고사장 빔 프로젝터, 대형 TV 모니터, 감독관 PC 화면에 최적화되어 있으며, 실시간 초 단위 시계, 각 교시별 자동 잔여 시간 카운트다운, 종료 임박 알림, OMR 답안지 작성 가이드, 그리고 부정행위 규정 AI 음성 안내 방송 기능을 제공합니다.

---

### ✨ 주요 기능

- **🕒 초 단위 실시간 디지털 시계 및 교시별 카운트다운**
  - 고정밀 로컬 실시간 디지털 시계 (`HH:MM:SS`).
  - 현재 진행 중인 교시의 잔여 시간 자동 계산 및 대형 카운트다운 표시.
  - 대형 고사장 맨 뒤 좌석에서도 선명하게 보이는 고대비 다크모드 디자인.

- **📅 공식 TOPIK II 시험 일정 완벽 연동**
  - **수험생 입실 및 준비 시간**: `09:20 – 09:40` (20분)
  - **1교시 듣기 시험**: `09:40 – 10:40` (60분, 50문항)
  - **1교시 쓰기 시험**: `10:40 – 11:30` (50분, 4문항)
  - **휴식 시간**: `11:30 – 11:50` (20분)
  - **2교시 입실 및 준비 시간**: `11:50 – 12:00` (10분)
  - **2교시 읽기 시험**: `12:00 – 13:10` (70분, 50문항)
  - **시험 종료**: `13:10` 이후

- **⚠️ 자동 잔여 시간 알림 및 종료 임박 경고**
  - **종료 10분 전**: 10분 전 알림 배너 표시.
  - **종료 5분 전**: 5분 전 알림 배너 표시.
  - **종료 2분 전**: 2분 전부터 종료 시점까지 붉은색 펄스 알림 및 `듣기/쓰기/읽기 시험 종료 임박...` 안내 문구 유지.

- **🌐 한국어 / 우즈베크어 실시간 언어 전환**
  - 클릭 한 번으로 모든 화면 요소(헤더, 일정표, 상태 메시지, 규정 안내)를 한국어(KR)와 우즈베크어(UZ)로 즉시 전환.

- **📝 OMR 답안지 작성 안내 및 확대 보기**
  - 컴퓨터용 사인펜 사용법, 수정 테이프 사용법, 답안지 교체 주의사항 안내.
  - OMR 답안지 샘플 이미지를 전체화면으로 확대(Zoom)하여 확인 가능.

- **📢 부정행위 규정 안내 및 AI 음성 안내 방송 탑재**
  - 유형별 제재 조치 (해당 시험 무효 처리, 2년간 응시자격 제한, 4년간 응시자격 제한) 명시.
  - 오디오 플레이어 탑재 (**재생 ▶**, **일시정지 ⏸**, **정지 ⏹**, 실시간 재생 시간 표시).
  - 고품질 한국어 및 우즈베크어 AI 오디오 안내 방송 파일 내장.
  - 규정 본문을 가리지 않도록 닫기/확대 버튼 옆 우측 하단에 정돈된 레이아웃.

- **🛠️ 시험 리허설을 위한 시뮬레이션(Demo) 패널**
  - 고사장 사전 점검 및 리허설을 위한 테스트 패널 내장.
  - 시험 전체 일정별 프리셋 버튼 원클릭 지원 (`09:40`, `10:38`, `11:28`, `11:30`, `11:50`, `12:00`, `13:08`, `13:10` 등).
  - 임의의 시간 설정 및 실제 초 단위 시계 흐름 시뮬레이션.
  - 시험 당일이 아닐 경우 "시험 당일 아님" 안내 모드 지원.

- **⚙️ 간편한 설정 파일 (`config.js`)**
  - 소스 코드를 수정하지 않고 `config.js` 파일에서 시험 회차(예: `108`, `109`, `110`)와 시험 일자(`DD.MM.YYYY`)를 자유롭게 변경 가능.

---

### 🕒 TOPIK II 시험 시간표

| 교시 | 시간 | 소요 시간 | 영역 및 진행 내용 | 비고 |
| :---: | :---: | :---: | :--- | :--- |
| **준비** | `09:20 - 09:40` | 20분 | 수험생 입실 및 본인 확인 | 유의사항 안내 및 신분 확인 |
| **1교시** | `09:40 - 10:40` | 60분 | **듣기 (Listening)** | 50문항 (1번 ~ 50번) |
| **1교시** | `10:40 - 11:30` | 50분 | **쓰기 (Writing)** | 4문항 (51번 ~ 54번) |
| **휴식** | `11:30 - 11:50` | 20분 | 휴식 시간 | 화장실 이용 및 휴식 |
| **준비** | `11:50 - 12:00` | 10분 | 2교시 입실 및 문제지 배부 | 2교시 입실 완료 및 준비 |
| **2교시** | `12:00 - 13:10` | 70분 | **읽기 (Reading)** | 50문항 (1번 ~ 50번) |
| **종료** | `13:10` | — | **시험 종료** | 답안지 및 문제지 회수 확인 |

---

### 🚀 사용 및 실행 방법

1. **설정 (`config.js`)**:
   `config.js` 파일을 메모장 또는 텍스트 에디터로 열어 시험 회차와 날짜를 지정합니다:
   ```javascript
   window.CONFIG = {
     TOPIK: "109",              // 시험 회차 (예: 109회)
     TOPIK_DATE: "27.10.2026"   // 시험 일자 (DD.MM.YYYY)
   };
   ```

2. **실행**:
   별도의 웹 서버 설치 없이 `index.html` 파일을 브라우저(Chrome, Edge 등)로 바로 열어 사용할 수 있습니다.

3. **호스팅 및 배포**:
   GitHub Pages, Vercel, Netlify, 일반 웹 호스팅 서버에 업로드하여 즉시 고사장에서 온라인으로 접속 가능합니다.

---

### 📄 License
This project is licensed under the [MIT License](LICENSE).
