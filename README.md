# DevPath AI — Storyboard

**DevPath AI** 화면 설계 스토리보드입니다. 외부 라이브러리 없이 단일 HTML 파일로 구현된 인터랙티브 슬라이드 형식이며, 학습자(LEARNER)·관리자(ADMIN)·비회원(PUBLIC) 역할별 화면 약 30종을 담고 있습니다.

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
| 화면 내 버튼·입력 | 시뮬레이션 모드 — 모달, 토스트, 탭, 유효성 검사 동작 |

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

## 🔗 관련 문서

- 화면 기능 정의: [documents/06_화면_기능_정의서](https://github.com/DevPathAi/documents/blob/main/06_화면_기능_정의서.md)
- 화면 흐름 시퀀스: [documents/05_화면_흐름_시퀀스_다이어그램](https://github.com/DevPathAi/documents/blob/main/05_화면_흐름_시퀀스_다이어그램.md)
- 마크다운 스토리보드: [documents/08_스토리_보드](https://github.com/DevPathAi/documents/blob/main/08_스토리_보드.md)
