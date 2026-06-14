# fit-tools — 무료 건강·운동 계산기

네이버 위젯이 없는 "전문 운동/다이어트 계산기"로 구글 검색 유입을 받고,
쿠팡 파트너스 + 구글 애드센스로 수익화하는 단일 HTML 사이트입니다.

## 포함된 계산기 7종
1. **TDEE** 하루 칼로리 소모량 (Mifflin-St Jeor)
2. **단백질** 권장 섭취량 (목표별 g/kg)
3. **1RM** 최대중량 추정 (Epley)
4. **체지방률** 추정 (미해군 둘레 공식)
5. **표준체중 / BMI** (아시아인 기준 18.5~22.9)
6. **물 섭취량** 권장량 (체중·활동량 기준)
7. **운동 칼로리 소모량** (MET 기준)

모바일 우선 다크테마, 의존성 없는 단일 `index.html`.

---

## 🚀 배포 방법

### 방법 A) GitHub Pages (이 repo, 무료)
1. 이 repo가 **Public** 인지 확인
2. GitHub repo → **Settings → Pages**
3. **Source: Deploy from a branch** → Branch: `main` / `/(root)` 선택 → Save
4. 잠시 후 `https://<유저명>.github.io/fit-tools/` 로 접속

### 방법 B) Netlify (가장 빠름, 무료, 도메인 불필요)
1. https://app.netlify.com/drop 접속
2. `index.html` 파일을 화면에 드래그&드롭
3. 즉시 `랜덤이름.netlify.app` 주소로 공개

---

## 💰 수익화 설정

### 1) 쿠팡 파트너스 링크 교체
- https://partners.coupang.com 가입 후 상품 링크 생성
- `index.html` 에서 `#REPLACE_쿠팡링크` 를 찾아(3곳) 본인 링크로 교체
- 고지 문구("쿠팡 파트너스 활동의 일환으로...")는 **필수**이니 지우지 마세요

### 2) 구글 애드센스 ID 교체 (트래픽 쌓인 뒤)
- https://adsense.google.com 에서 사이트 승인 받기
- `index.html` `<head>` 의 애드센스 주석 한 줄을 풀고
  `ca-pub-XXXXXXXXXXXXXXXX` 를 본인 게시자 ID로 교체
- ⚠️ 애드센스는 보통 `*.github.io`/`*.netlify.app` 같은 무료 서브도메인을 거절합니다.
  광고를 제대로 붙이려면 본인 도메인(연 1만원대) 연결을 권장합니다.

---

## 🌐 도메인 연결 방법 (선택)
1. 가비아/Cloudflare 등에서 도메인 구매 (예: `fit-tools.co.kr`)
2. **GitHub Pages**: Settings → Pages → Custom domain 입력 + DNS의 CNAME/A 레코드 설정
   또는 **Netlify**: Site settings → Domain management → Add custom domain → 안내대로 DNS 설정
3. `index.html` 의 `<link rel="canonical">` 와 OG `url` 을 실제 도메인으로 교체

---

## 📈 다음에 하면 좋은 것
- 각 계산기를 **별도 페이지(URL)** 로 분리 → 구글에 더 많이 노출
- 계산기별 **상세 설명/가이드 글** 추가 (검색 유입 ↑)
- Google Search Console 등록 → 색인 요청
- 인기 계산기 위주로 계산기 추가 (예: 임신 출산예정일, 평균 페이스, 1RM 종목별)
