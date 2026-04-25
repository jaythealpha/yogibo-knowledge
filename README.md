# Yogibo Knowledge Base

요기보 제품에 대해 검증된 단일 진실 공급원(single source of truth). 영상 제작·광고 카피·SKU 매칭·3D 키링 같은 다양한 작업에 공통으로 사용.

## 구성

| 파일 | 내용 | 용도 |
|---|---|---|
| `PRODUCT_REFERENCE.md` | 16개 셰이프의 상세 형태 가이드 + EN/JP/KR 명칭 매핑 + US 라인업 차이 | LLM 시스템 프롬프트, 영상 스크립트 컨텍스트 |
| `image_manifest.json` | 셰이프별 추천 hero 사진 경로 + products 폴더 위치 + 각도 가이드 | b-roll 선별, 키링 input 자동 매핑 |
| `README.md` (this) | 사용 방법 | — |

## 사용 시나리오

### 1. Claude Project / Custom GPT 지식베이스
- Claude 데스크탑/웹: New Project → Knowledge → 이 폴더 전체 업로드
- 프로젝트 안에서 영상 스크립트 / 광고 카피 / FAQ / 비교표 생성 시 환각 거의 0
- 예시 프롬프트: "유튜브용 60초 Drop 제품 소개 영상 스크립트 짜줘"

### 2. Claude Code / 로컬 작업
- 작업 시작 시 `@/Users/jay/Yogibo/knowledge/PRODUCT_REFERENCE.md` 첨부
- `image_manifest.json`을 코드에서 직접 import해 SKU → 사진 자동 매핑

### 3. 키링 파이프라인 (`~/Yogibo/keyring/meshy_batch.py`)
- `image_manifest.json`의 `curated_hero` 경로를 SKU별로 lookup
- 누락된 셰이프(`bubble`, `rollmidi`, `rollmini`, `ghost` 등)는 별도 수집 필요

## 데이터 신뢰도

- ✅ **PRODUCT_REFERENCE.md**: 공식 사이트 3개국(US/JP/KR) 교차 검증된 형태 정보
- ✅ **EN/JP/KR 명칭**: 사이트 직접 확인 (Pod X = Drop 같은 함정 명시)
- ⚠️ **dimensions_cm**: 일부는 공식 페이지에서 추출, 일부는 hero 사진에서 추론(특히 Prime, Roll Mate 변형별 길이)
- ⚠️ **curated_hero**: 사용자가 수동 선별. Mini는 부적합으로 표기됨 (어린이 앉음)

## 업데이트 정책

새 SKU 추가, 명칭 변경, 더 좋은 hero 사진 발견 시:
1. `image_manifest.json` 해당 셰이프 항목 수정
2. `PRODUCT_REFERENCE.md`도 함께 갱신 (필요 시)
3. `$last_updated` 날짜 갱신
4. 큰 변경은 git commit으로 히스토리 보존 권장

## 누락 데이터 (TODO)

- `bubble` / `ghost`: hero 사진 없음 (JP clearance/exclusive)
- `rollmidi` / `rollmini`: hero 사진 없음
- `mini`: 현재 hero가 부적합 — 깨끗한 unloaded 사진 필요
- 정확한 치수(특히 Prime, Roll Mate 변형별)
- 가격/판매처 정보 (필요 시 별도 파일)
