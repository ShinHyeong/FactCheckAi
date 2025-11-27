# ✔️ FactCheckAI (MVP Ver.)

> **⚠️ Notice: This is the MVP Version.**
> <br>본 문서는 해커톤 기간 동안 개발된 **MVP(Minimum Viable Product) 버전**에 대한 기록입니다.
> <br>개선된 UI와 기능이 포함된 **최종 배포 버전**은 아래 링크에서 확인하실 수 있습니다.

<br>

| 구분 | 링크 (Link) | 비고 |
| :--- | :--- | :--- |
| **🚀 Final Service** | **[최종 버전 Demo Page 바로가기](https://main.dko0436e2g0lv.amplifyapp.com/)** | **실제 서비스 배포 링크** |
| **💻 Final Repo** | **[최종 버전 GitHub 코드 보기](https://github.com/saa-hackathon-2025/factcheck)** | 리팩토링 완료된 최신 코드 |
| **🧪 MVP Demo** | [MVP Demo Page](https://factcheckaideploy.vercel.app/) | 초기 프로토타입 버전 |

<br>

---

## 💡 MVP Introduction : 이력서와 코드를 교차 검증하는 면접 솔루션
![MIT](https://img.shields.io/badge/license-MIT-blue.svg)
![React](https://img.shields.io/badge/React-19.0-61DAFB?logo=react)
![Gemini](https://img.shields.io/badge/Google%20Gemini-2.5%20Flash%20Lite-8E75B2?logo=google)
![Tailwind](https://img.shields.io/badge/Tailwind-CSS-38B2AC?logo=tailwind-css)

<br>

> **"자소서에 쓴 그 기술, 코드로 증명되어 있나요?"**
> <br>단순 CS 암기 테스트를 넘어, GitHub 코드와 자소서를 대조하여 진실성을 검증하는 **팩트 체크 AI 면접관** 서비스입니다.

<br>

## 🧐 Background : 문제 제기

**"취준생인 우리가, 당장 필요해서 만들었습니다."**

개발자 면접 준비 팁을 검색하면 "포트폴리오에 대한 꼬리 질문을 대비하라"는 조언이 쏟아집니다. 하지만 정작 우리는 **어디서, 어떻게 연습해야 할까요?**

* 기존 서비스의 한계: 대부분 범용적인 인성 질문이나, *단순 CS 지식(운영체제, 네트워크 등) 확인*에 그칩니다.
* 구체적 대비 불가: "내가 짠 이 코드"의 로직과 구현 방식에 대해 *날카롭게 파고드는* 질문을 받아볼 곳이 없습니다.

이 간극을 해결하고자 **지원자의 코드와 주장을 직접 대조하는 서비스**를 만들었습니다.

<br>

## ✨ Solution : 주요 기능 (MVP Scope)

**FactCheck AI**는 지원자의 **자소서(주장)** 와 **GitHub 코드(근거)** 를 교차 분석(Cross-Validation)합니다.

### 1. 진위 여부 판독 (Verification)
자소서에 서술된 기술적 경험이 실제 코드에 구현되어 있는지 팩트 체크를 진행합니다.
* **판정 기준:** `검증 완료` / `판독 불가` / `과장 의심` / `허위 사실`의 4단계 등급 산정

### 2. 맞춤형 킬러 문항 생성 (Generation)
JD(직무 기술서)와 내 코드를 분석하여 면접관이 물어볼 법한 '허점'을 찌릅니다.
* *"자소서엔 Redis로 트래픽을 처리했다고 썼는데, 코드엔 설정 파일만 있고 실제 로직이 없습니다. 설명해 주시겠습니까?"*

### 3. 심층 압박 면접 시뮬레이션 (Simulation)
- 단답형으로 끝나지 않습니다. 답변의 논리적 허점을 파고드는 **꼬리물기 질문(Deep Dive)** 을 통해 실전 압박 면접을 대비할 수 있도록 했습니다. 
- 면접 종료 후에는 **방어율 리포트**를 제공합니다.

<br>

## 🎯 Target Audience

| 구분 | 니즈 (Needs) | 제공 가치 (Value) |
| :--- | :--- | :--- |
| **개발직무 지원자** | "면접 가서 기술 검증에 탈탈 털릴까 봐 두렵다." | **사전 모의 방어:** 내 자소서의 과장된 부분을 미리 파악하고, 꼬리 질문을 연습하여 자신감 확보 |
| **채용 담당자** | "허위 스펙 거르는 데 시간 쓰기 싫다." | **검증 비용 절감:** 포크(Fork)만 해둔 껍데기 프로젝트나 허위 기재를 AI가 1차로 필터링 |

<br>

## 🚀 MVP Process : 3단계 워크플로우

### Step 1. Input (원클릭 면접 준비)
사용자가 **JD(채용 공고)**, **자소서**, **GitHub Repository 주소**를 입력합니다. 복잡한 설정 없이 버튼 하나로 분석이 시작됩니다.

<div align="center">
  <br>
  <img src="https://github.com/user-attachments/assets/932ab547-2726-43c1-990f-1933bf79cb52" alt="MVP Service Preview Step1" width="65%">
  <br><br>
</div>

### Step 2. Analysis (진위 판독 및 질문 도출)
AI가 코드와 자소서를 교차 검증하여 분석 결과를 내놓습니다.
- **신뢰도 등급:** 구현 정도에 따른 4단계 진단 (`검증 완료` / `판독 불가` / `과장 의심` / `허위 사실`)
- **의심 포인트:** "구현체 없음", "로직 불일치" 등 면접관의 의구심 시각화
- **예상 질문:** 코드의 취약점을 조준한 맞춤형 질문 리스트업

<div align="center">
  <br>
  <img src="https://github.com/user-attachments/assets/b29cd5bb-dbdf-4e0a-bb11-35f731afe8bf" alt="MVP Service Preview Step2" width="65%">
  <br><br>
</div>

### Step 3. Action (실전 디펜스 & 피드백)
사용자가 질문을 선택하면 AI 면접관과의 실시간 문답이 진행됩니다.
- **Deep Dive:** 2차, 3차 꼬리 질문을 통한 논리 검증
- **Feedback:** 면접 방어율 점수 및 개선 가이드 제공

<div align="center">
  <br>
  <img src="https://github.com/user-attachments/assets/f50667c4-284c-47d6-9d8c-e08b3a19f104" alt="MVP Service Preview Step3-1" width="42%">
  &nbsp;&nbsp; <img src="https://github.com/user-attachments/assets/c6aa5e71-a8ff-42a2-8fb9-30c384e179f8" alt="MVP Service Preview Step3-2" width="42%">
  <br>
</div>

<br>

## ⚖️ Why FactCheckAI? (차별점)

### vs ChatGPT
> "ChatGPT에게 내 코드를 다 긁어주고, 자소서랑 비교해서 면접 질문 뽑아줘라고 프롬프트 짤 시간에, **FackCheckAI는 버튼 하나로 해결합니다.**"
* 프롬프트 엔지니어링 없이 최적화된 결과 도출
* 단순 질문 생성을 넘어선 '검증(Verification)' 로직 특화

### vs 타사 서비스 비교

| 서비스 | 분석 대상 | 한계점 | FactCheckAI의 차별점 |
| :--- | :--- | :--- | :--- |
| **단순 AI 모의면접** | 자소서 텍스트 | 코드를 안 봄. "어려웠던 점은?" 같은 뻔한 질문 | **코드를 직접 분석**하여 구체적 구현 여부 확인 |
| **GitHub 분석기** | 커밋 수, 언어 비율 | "성실함"만 측정함. 내용의 진실성은 모름 | 기술 스택 나열이 아닌, **'자소서 주장 vs 코드 실체'의 일치 여부** 판단 |

<br>
