# UNIONCOMMUNITY 이메일 서명 생성기

GitHub Pages용 정적 서명 빌더. 서버 불필요.

## 구성
| 파일 | 용도 |
|---|---|
| `index.html` | 직원용 — 이름·부서·연락처만 입력해 서명 생성 |
| `admin.html` | 관리자용 — 회사 공통값 편집 후 config.json 생성 |
| `config.json` | 회사 공통 설정 (로고·배너·주소·SNS·아이콘) |
| `sig-core.js` | 서명 HTML 생성 공통 로직 |
| `icons/` | 연락처 아이콘 (tel/mobile/email/addr) |

## 배포
1. 이 폴더 전체를 리포지토리에 푸시
2. Settings → Pages → Branch: main 설정
3. 직원 공유 주소: `https://<org>.github.io/<repo>/`
4. 관리자 주소: `https://<org>.github.io/<repo>/admin.html`

## 회사 공통값 변경 (관리자)
admin.html 열기 → 값 수정 → "config.json 다운로드" → 리포지토리의 config.json 교체 후 커밋
→ 1~2분 내 전 직원 페이지에 반영

## 아이콘/이미지 교체
모든 아이콘과 로고는 config.json의 URL로 지정됩니다. 회사 웹서버(unionbiometrics.com)에
이미지를 올린 뒤 admin.html에서 해당 https URL을 입력하세요.
주의: sftp:// 경로는 업로드용일 뿐 이메일·브라우저에서 열리지 않으므로 반드시 https URL을 사용해야 합니다.
