# Claude 교육자료 홈페이지

울산대학교 업무개선 AI 멘토링 — Claude 제품·기능 개요 / Claude in Excel 교육자료 정적 홈페이지입니다.

## 구성 파일

- `index.html` — 본문 (단일 페이지)
- `README.md` — 이 안내 문서

원본 파일(`Claude___standalone.html`, 약 22MB)에 임베딩되어 있던 Inter / Pretendard 웹폰트를 CDN 링크로 교체해 **86KB**까지 경량화했습니다. 시각적 결과물은 동일하지만 첫 로딩 속도가 크게 빨라집니다.

## GitHub Pages로 배포하기

### 1. 새 저장소 만들기

1. GitHub에 로그인 후 우측 상단 `+` → `New repository`
2. 저장소 이름 예: `claude-edu` (계정에서 한 개만 운영한다면 `<사용자명>.github.io`로 만들면 루트 도메인 사용 가능)
3. `Public`으로 설정, `Add a README` 체크 해제
4. `Create repository`

### 2. 파일 업로드

가장 쉬운 방법은 GitHub 웹 업로드입니다.

1. 새로 만든 저장소 페이지에서 `uploading an existing file` 링크 클릭
   (또는 `Add file` → `Upload files`)
2. `index.html`과 `README.md`를 드래그&드롭
3. 하단에 커밋 메시지 입력 후 `Commit changes`

> 참고: 한 번에 여러 파일 업로드 시 100MB 제한이 있으나, 최적화된 `index.html`은 86KB라 문제없이 업로드됩니다.

### 3. Pages 활성화

1. 저장소 상단 메뉴 → `Settings`
2. 좌측 메뉴 `Pages` 클릭
3. `Source` 항목에서 `Deploy from a branch` 선택
4. `Branch` → `main` / 폴더 → `/ (root)` 선택 → `Save`
5. 1~2분 후 페이지 상단에 `Your site is live at https://<사용자명>.github.io/<저장소명>/` 표시

### 4. 접속 확인

- 발급된 URL을 브라우저에 입력
- 첫 접속 시 CDN에서 폰트를 받아오므로 잠시 글꼴이 시스템 폰트로 보일 수 있으며, 곧 Inter / Pretendard로 전환됩니다

## 향후 수정 방법

### 내용을 바꾸고 싶을 때

`index.html`의 텍스트를 직접 수정해도 되고, 원본 `.html` 파일을 같은 방식으로 재최적화해 교체해도 됩니다.

### 사용자 도메인 연결

`Settings → Pages → Custom domain`에서 보유 도메인 입력 후, 도메인 DNS에 GitHub Pages CNAME 또는 A 레코드를 등록하면 됩니다.

### 비공개 운영이 필요할 때

GitHub Pages는 `Public` 저장소만 무료입니다. 비공개로 두려면 GitHub Pro/Team 요금제가 필요하거나, Netlify의 패스워드 보호 기능을 사용하는 편이 더 간단합니다.

## 용량 비교

| 항목 | 크기 |
|------|------|
| 원본 `Claude___standalone.html` | 약 22.0 MB |
| 최적화 `index.html` | 약 86 KB |
| 절감률 | 99.6% |

폰트는 Google Fonts(Inter)와 jsDelivr(Pretendard) CDN을 통해 자동으로 불러옵니다. 별도 라이선스 비용은 없습니다.
