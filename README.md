# 3D Texture Simulator

브라우저에서 바로 실행되는 3D 텍스쳐 시뮬레이터입니다.  
Three.js 기반으로 원단/소재 텍스쳐 이미지를 업로드하면 실시간으로 3D 엠보 표면을 렌더링합니다.

## 실행 방법

`3D Texture simulator v10.html` 파일을 브라우저에서 열기만 하면 됩니다.

## 주요 기능

- 텍스쳐 이미지 업로드 → 3D 변위(Displacement) 렌더링
- 깊이(Depth), 패턴 밀도(Scale), 불투명도(Opacity) 실시간 조절
- 소재 선택 (금속 / 목재 / 석재 / 패브릭)
- AI Haptic Insight 패널 (촉감 분석 통계)
- PNG / STL 내보내기

## 파일 구조

| 경로 | 설명 |
|------|------|
| `3D Texture simulator v10.html` | 최신 버전 (메인) |
| `image/` | 텍스쳐 이미지 에셋 |
| `versions/` | 이전 버전 기록 (v1 ~ v9) |

## 버전 히스토리

| 버전 | 파일 | 주요 변경 내용 |
|------|------|----------------|
| v1 | `Premium texture.html` | 최초 버전. 2D 평면 지오메트리, 깊이/반복 슬라이더, PNG·STL 내보내기, AI Haptic Insight 패널 |
| v2 | `Premium texture v2.html` | **3D 베이스 블록 도입** (200×200mm 캔버스, 30mm 두께). 소재별 색상 적용, 카메라·조명 전면 재설정 |
| v3 | `Premium texture v3.html` | 반복 슬라이더 범위 및 단위 조정 (RSm 가이드 표시로 변경) |
| v4 | `Premium texture v4.html` | **사출 시뮬레이션 모드** — 컬러 맵 제거, 순수 변위(displacement) 기반 단색 렌더링 |
| v5 | `Premium texture v5.html` | 베이스 두께 30mm → 5mm 축소. 패턴 밀도 슬라이더 범위 조정 |
| v6 | `Premium texture v6.html` | 컬러 맵 복원 (흑백 그레이스케일). 엠보 그림자·AO 효과 회복 |
| v7 | `Premium texture v7.html` | 두께 3mm로 추가 축소. v2 스타일 조명으로 복원, fillLight 재추가 |
| v8 | `3D Texture simulator v8.html` | **UI 전면 개편** — 헤더 디자인, iOS형 토글, 컨트롤 섹션 구조화 ("by KSJ" 크레딧 추가) |
| v9 | `3D Texture simulator v9.html` | **캔버스 200mm → 50mm 축소** (매크로 뷰 최적화). 카메라·조명 근접 재배치, bumpScale 추가 |
| v10 | `3D Texture simulator v10.html` | **불투명도(Opacity) 슬라이더 추가** — 패턴 농도 0~100% 실시간 조절, 이중 텍스쳐 시스템 적용 |

## 기술 스택

- Vanilla HTML + CSS + JavaScript (의존성 없음)
- [Three.js r128](https://threejs.org/) — 3D 렌더링
- OrbitControls — 마우스 회전/줌/패닝
- STLExporter — STL 파일 내보내기
