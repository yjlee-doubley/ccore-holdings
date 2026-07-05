# 씨코어홀딩스 (CCore Holdings) 회사 홈페이지

소프트웨어 개발·납품, 경영관리 및 투자자문 기업 씨코어홀딩스의 공식 홈페이지입니다.
GitHub Pages로 호스팅되는 정적 사이트입니다.

- **도메인**: https://www.doubley.ai.kr
- **호스팅**: GitHub Pages (main 브랜치 루트)

## 구조

```
.
├── index.html          # 메인 페이지 (단일 페이지)
├── assets/
│   ├── style.css       # 스타일시트
│   └── favicon.svg     # 파비콘
├── CNAME               # GitHub Pages 커스텀 도메인 설정
└── .nojekyll           # Jekyll 빌드 비활성화
```

## 배포

main 브랜치에 push하면 GitHub Pages가 자동으로 배포합니다.

## 커스텀 도메인(DNS) 설정

도메인 등록기관(예: 가비아, 후이즈 등)의 DNS 관리에서 아래 레코드를 추가해야 합니다.

| 타입  | 호스트 | 값                        |
|-------|--------|---------------------------|
| CNAME | www    | `yjlee-doubley.github.io` |

루트 도메인(`doubley.ai.kr`)도 연결하려면 A 레코드 4개를 추가합니다:

| 타입 | 호스트 | 값              |
|------|--------|-----------------|
| A    | @      | 185.199.108.153 |
| A    | @      | 185.199.109.153 |
| A    | @      | 185.199.110.153 |
| A    | @      | 185.199.111.153 |

DNS 반영 후 GitHub 저장소 **Settings → Pages**에서 `Enforce HTTPS`를 활성화하세요
(인증서 발급까지 최대 24시간 소요될 수 있습니다).

## 로컬 미리보기

```bash
python3 -m http.server 8000
# http://localhost:8000 접속
```
