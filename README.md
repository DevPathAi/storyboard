# DevPath AI — Storyboard

**DevPath AI** 화면 설계 스토리보드입니다. 외부 라이브러리 없이 단일 HTML 파일로 구현된 혼합 모드 슬라이드 형식이며, 핵심 LCS 학습 루프는 인터랙티브로, 나머지 화면은 개발 핸드오프용 정적 목업으로 구성합니다.

## 🖥 보는 방법

`storyboard.html` 파일을 브라우저에서 열면 바로 동작합니다. 빌드나 서버가 필요 없습니다.

```
storyboard.html  # 더블클릭 또는 브라우저로 열기
```

## ⌨️ 주요 조작

| 조작 | 동작 |
|------|------|
| `←` / `→`, 클릭 | 슬라이드 이동 |
| 좌측 사이드바 (TOC) | 화면 목차로 바로 이동 |
| 우측 상단 역할 필터 | ALL / PUBLIC / LEARNER / ADMIN 화면만 보기 |
| 화면 내 버튼·입력 | 핵심 LCS 루프 중심 시뮬레이션 — 토스트, 화면 전환, 입력, 모달 동작 |

## 핵심 인터랙티브 루프

`콘텐츠 학습 -> 실습 실패 -> 일반 AI 한계 -> LCS 기반 리뷰 -> 보정된 다음 과제` 흐름을 클릭으로 확인할 수 있습니다.

| 단계 | 슬라이드 | 의미 |
|------|----------|------|
| 콘텐츠 | `SCR-W-CNT-001` | 학습자가 JPA 페치 전략을 읽고 실습으로 진입 |
| 실습 실패 | `SCR-W-SBX-001` | `testFetchJoin` 실패와 막막함 노출 |
| 일반 AI 한계 | `GENERAL-AI-COMPARE` | 맞지만 개인 맥락 없는 일반 답변 |
| LCS 리뷰 | `SCR-W-MEN-001 + LCS` | 현재 단원, 경로, 최근 실패를 자동 첨부한 리뷰 |
| 경로 보정 | `SCR-W-DASH-001` | LCS 리뷰 결과로 다음 과제가 보강됨 |

## 📋 수록 화면

| 영역 | 화면 ID | 내용 |
|------|---------|------|
| 온보딩 | `SCR-W-ONB-*` | 랜딩, 비회원 진단, OAuth2 가입, 목표/트랙 설정 |
| 학습 경로 | `SCR-W-PATH-*` | AI 개인화 학습 경로 (1st Aha) |
| 콘텐츠/실습 | `SCR-W-CNT-*`, `SCR-W-SBX-*` | 인터랙티브 콘텐츠, Sandbox 실습 |
| AI 리뷰/멘토 | `SCR-W-REV-*`, `SCR-W-MEN-*` | AI 코드 리뷰 (2nd Aha), AI 멘토 채팅 |
| 커뮤니티 | `SCR-W-COM-*` | Q&A·자유·프로젝트 게시판, 평판, 배지 |
| 대시보드/알림 | `SCR-W-DASH-*`, `SCR-M-NTF-*` | 스트릭·진척률, 알림 |
| 관리자 | `SCR-A-*` | 콘텐츠·사용자·FinOps·Sandbox 악용 탐지 관리 |

각 화면 슬라이드에는 API 명세(메서드·상태 코드), View Model 트리, 액션/에러/유효성 정의 패널이 포함되어 있습니다.

## 🚀 배포

`main` 브랜치에 push하면 GitHub Actions가 `storyboard.html`을 `index.html`로 복사해 GitHub Pages에 배포합니다.

배포 대상:

```text
https://devpathai.github.io/storyboard/
```

GitHub 저장소 Settings에서 Pages source가 **GitHub Actions**로 설정되어 있어야 합니다.

## 🔗 관련 문서

- 화면 기능 정의: [documents/06_화면_기능_정의서](https://github.com/DevPathAi/documents/blob/main/06_화면_기능_정의서.md)
- 화면 흐름 시퀀스: [documents/05_화면_흐름_시퀀스_다이어그램](https://github.com/DevPathAi/documents/blob/main/05_화면_흐름_시퀀스_다이어그램.md)
- 마크다운 스토리보드: [documents/08_스토리_보드](https://github.com/DevPathAi/documents/blob/main/08_스토리_보드.md)
