# COVE — 천천히 채우는 하루를 위한 라이프스타일 브랜드

라이프스타일 카테고리 단일 페이지 랜딩. Figma 레퍼런스(카카오 지속가능성 랜딩,
`node-id=1-817`)의 섹션 구성과 그리드 수치를 그대로 따르고, 브랜드/카피만
가상의 라이프스타일 브랜드 **COVE**로 리스킨했습니다.

- 헤더(고정) → 히어로(풀블리드) → 프로모 스트립(3분할 플러시 카드) →
  브랜드 철학 모자이크(4×8, 330px 모듈 — Figma 원본 그리드 좌표 1:1 복제) →
  라이프스타일 중점 아젠다(4×3, 빈 셀 2칸까지 동일 위치) → 소식(3카드) →
  CTA 배너(풀블리드) → 푸터(7열)
- 캐러셀/페이지네이션 등은 랜딩페이지 하드룰에 따라 정적 그리드로 대체했습니다.
- 이미지 영역은 전부 `#d9d9d9` 플레이스홀더(`--color-placeholder` 토큰)입니다.
- 컬러는 브랜드 컬러가 별도로 지정되지 않아 디자인 키트의 무채색 토큰만 사용했습니다.

## Stack

순수 HTML / CSS(빌드 도구 없음). GitHub Pages에서 바로 서빙됩니다.

## Structure

```
index.html            메인 페이지
css/styles.css         공용 디자인 키트 원본 (토큰·그리드·리셋 — 수정하지 않음)
css/site.css            COVE 컴포넌트 (헤더·히어로·모자이크·아젠다·뉴스·CTA·푸터)
assets/favicon.svg      파비콘
.github/workflows/deploy.yml  GitHub Pages 자동 배포 워크플로우
```

## 로컬 실행

```bash
python3 -m http.server 8000
# http://localhost:8000 접속
```

## 배포

`main` 브랜치에 push하면 GitHub Actions가 자동으로 GitHub Pages에 배포합니다.
저장소 Settings → Pages → Source가 "GitHub Actions"로 설정되어 있어야 합니다.
