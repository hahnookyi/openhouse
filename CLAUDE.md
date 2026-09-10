# openhouse

「에어비앤비 트렌드 연구 밋업 - 웰컴 커뮤니티」 행사 안내 **단일 페이지**.
GitHub Pages 로 배포된다(`.nojekyll` 있음, Vercel 아님).

현재 게시 중인 회차: **2026년 9월** (9/11 금, 9/17 목).

## 이 파일은 이제 손으로 고쳐도 된다

이전 `index.html` 은 3.4MB 짜리 base64 번들이었다. 문구 한 줄을 못 고치는 구조였다.
2026년 9월 개편 때 **사람이 읽고 고칠 수 있는 순수 HTML/CSS 한 장으로 다시 썼다.**

- 약 350줄, 20KB 미만. 빌드 도구 없음, 의존성 없음
- 이미지는 base64 로 박지 않고 같은 폴더의 파일로 둔다
- 서체는 Pretendard CDN 링크 한 줄. 실패해도 시스템 서체로 떨어진다
- 문구를 바꾸려면 `<main class="page">` 안쪽만 고치면 된다

## 구성

```
index.html          안내 페이지 (수정 가능한 소스)
hanok-night.jpg     본문 히어로 사진 (960x640)
share.png           카카오톡·네이버 공유 카드 (1200x630)
og-image.png        share.png 와 동일본
wmh-logo.png / ai-living-stay-white.png
.nojekyll           GitHub Pages Jekyll 처리 비활성화
```

## 다음 회차를 열 때 고치는 곳

1. `<title>` 과 `og:title` / `og:description` 의 날짜
2. 상단 배지 `.badge` 의 "9월 · 부암동 한옥 모임"
3. 도입부 문구와 `<h2>` 아래 본문 문단
4. `모임 안내` 카드의 일시 / 주제 / 정원 / 신청 / 연락처 / 주차
5. `share.png` 와 `og-image.png` 교체
6. 배포 주소가 정해지면 `og:image` 와 `og:url` 의 `YOURSITE` 두 곳

## 스타일 토큰

`:root` 에 모아 두었다. 강조색은 `--accent: #ff385c` 하나만 쓴다.
배지, 본문 강조어, 전화 버튼, 맺음 구분선 네 곳이다. 다른 색을 추가하지 않는다.

## 글쓰기

- 행사 안내 문구는 한국어. 담백하게 쓰고 과장된 마케팅 톤을 쓰지 않는다.
- em dash 와 en dash 는 쓰지 않는다. 하이픈(-)만 쓴다.
- 한 문단은 두 줄을 넘기지 않는다. 줄바꿈은 `<br>` 로 직접 잡는다.
