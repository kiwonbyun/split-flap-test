# Split-Flap 1개 모듈 만들기 — 입문자 단계별 플랜

## Context
이 저장소는 scottbez1/splitflap (Apache 2.0) 오픈소스의 로컬 클론으로, ESP32 기반 분할 플랩 디스플레이의 **기구·전자·펌웨어**가 한곳에 모여 있다. 사용자는 입문자로서 **모듈 1개**만 동작하는 것을 첫 목표로 한다. 따라서 풀 디스플레이 빌드(108모듈 등)가 아닌 "1개를 끝까지 켜본다"는 학습 트랙이 필요하다.

저장소의 권장 라인은 **v2 (52플랩)** 이며 2025-01-19부터 stable이다. v2 문서(`docs/v2/`)가 현재 진실의 원천(SOT). 미국 외 사용자는 "Easy route(미국 전용 Bezek Labs Etsy)"를 그대로 쓸 수 없어 **Complete route 기반의 글로벌 발주 + 핵심만 키트로 구매**하는 하이브리드가 현실적이다.

최종 산출물: 12V 전원 인가 후, USB로 ESP32에 연결해 웹 UI에서 'A' 한 글자를 보내면 플랩이 정확히 그 글자로 회전·정지하는 동작 모듈 1개.

---

## 단계별 목표 (Phase 0 ~ Phase 7)

각 단계는 **목표 → 산출물(완료 기준) → 핵심 참조 파일/문서** 형식.

### Phase 0. 사전 학습 & 환경 준비 (1~2시간)
- **목표**: 프로젝트 구조와 v2 빌드 흐름을 이해하고, 빌드 도구를 설치한다.
- **할 일**:
  - 다음 문서 정독 (이 순서):
    - `README.md` (Design Overview 섹션)
    - `docs/DocumentationIndex.md`
    - `docs/v2/OrderingEasy.md` — 발주 큰 그림
    - `docs/v2/Assembly.md` — 조립 큰 그림
  - 도구 설치:
    - **VS Code + PlatformIO 확장** (펌웨어 빌드/업로드용)
    - (선택) Python 3.8+ — 추후 컴퓨터 제어 SW용
  - Discord 커뮤니티 가입 (막힐 때 질문용)
- **산출물**: 빌드 도구 설치 완료, `pio run -e chainlink` 로컬 시도 시 컴파일 통과.

### Phase 1. 부품 발주 (모듈 1개 BOM, 2~4주 리드타임)
- **목표**: 모듈 1개를 위한 모든 물리 부품을 손에 넣는다.
- **발주 경로 (한국 기준 권장)**:
  | 카테고리 | 품목 | 추천 공급처 |
  |---|---|---|
  | 기구(레이저컷) | 3mm 아크릴 프레임 1세트 (52플랩용 zip 업로드) | Elecrow 레이저컷 서비스 |
  | 센서 PCB | Hall sensor PCB + 4mm 자석 + 핀헤더 | JLCPCB(자체 발주) 또는 Bezek Labs 키트 + 배대지 |
  | 모터 | 28BYJ-48 **12V 버전** (64:1, ~100Ω, 레이저각인 라벨) | AliExpress (사양 확인 필수) |
  | 플랩 | 52장 (사전인쇄 "Epilogue" 권장) | Bezek Labs Etsy + 배대지 / 또는 PVC 카드 DIY |
  | 컨트롤러 | Chainlink Driver v1.1 + Chainlink Buddy [T-Display] + Lilygo T-Display ESP32 | Bezek Labs / JLCPCB self-fab |
  | 전원 | 12V 1A 이상 어댑터 (DC 잭) | 국내 부품상 |
  | 체결구 | M4×10 버튼헤드 볼트 ×10, M4 너트 ×10 | 국내 볼트상가 / McMaster |
  | 와이어 | 22AWG(신호용), 20AWG(12V) 약간 | 국내 부품상 |
- **산출물**: 모든 부품 입고 + BOM 체크리스트 100% 표시.
- **참조**: `docs/v2/OrderingComplete.md`, `docs/Flaps.md`, `docs/MotorGuide.md`.
- **주의**: 모터는 **반드시 12V/100Ω 사양**. 5V 28BYJ-48이 외형상 유사하지만 토크 부족으로 실패함.

### Phase 2. 부품 검수 & 작업대 셋업 (1~2시간)
- **목표**: 부품 누락/파손 확인, 도구 준비.
- **필요 도구**: 인두기·솔더, M4 육각 렌치, 펜치(자석/IDC 작업), 보석세공 줄(아크릴 다듬기), 순간접착제 + 경화촉진제, 멀티미터.
- **검수 체크**:
  - 레이저컷 부품 수량 (Assembly.md 1장 기준 비교)
  - 모터 코일 저항 멀티미터 측정 (~100Ω)
  - 자석 극성 확인용 센서 PCB LED 동작 (3.3V 인가 시)
- **산출물**: 모든 부품 ✓, 작업 공간 확보.

### Phase 3. 기구 조립 — 드럼 & 인클로저 (3~5시간)
- **목표**: 모터·센서·플랩을 제외한 기계 구조 완성.
- **순서** (`docs/v2/Assembly.md` 기준):
  1. 플랩 드럼 접착(스트럿 + 휠 + 센터 스페이서, M4 볼트 가이드 사용)
  2. 인클로저 좌측판에 모터 + 센서 PCB 가조립 (M4×10)
  3. 드럼을 모터축에 접착
  4. 상/하/우측판 + 정면판 결합 (M4 볼트·너트)
  5. 플랩 백스톱 볼트 설치
- **산출물**: 빈 인클로저(플랩 미장착)가 손으로 부드럽게 회전.
- **주의**: 본드 경화 전 정렬 확인. 비뚤어지면 플랩 마찰 발생.

### Phase 4. 전자 — 센서 & 컨트롤러 납땜 (2~3시간)
- **목표**: 모듈 1개를 제어할 수 있는 전자부 완성.
- **할 일**:
  - 센서 PCB 패널에서 1개 분리, 라벨 면에서 우각 핀헤더 삽입 후 납땜 (스루홀, SMD 없음)
  - Chainlink Driver의 모터 JST XH 커넥터, 센서 3핀 헤더, 리본/스크류터미널 납땜
  - Chainlink Buddy [T-Display]에 T-Display ESP32 장착
  - 자석 극성 테스트 (PCB LED로 확인 후 드럼에 자석 삽입)
- **산출물**: 12V 인가 시 센서 LED가 자석에 반응. 납땜 점 광택·체결 OK.

### Phase 5. 플랩 장착 & 배선 (1~2시간)
- **목표**: 모듈을 완성된 형태로 만든다.
- **할 일**:
  - 플랩 52장 순서대로 삽입 (홈 위치가 0번 플랩이 되도록)
  - 모듈 ↔ Chainlink Driver A포지션 연결:
    - 모터 → 흰색 JST XH (A 슬롯)
    - 센서 케이블 → 3핀 헤더 (A 슬롯, GND/Sig 방향 주의)
  - Chainlink Driver ↔ Buddy: 리본케이블(Output→Input) + 3.3V/GND/12V 스크류
  - 12V 어댑터 → Chainlink Driver 전원 입력
- **산출물**: 모든 케이블 결선 완료, 통전 전 멀티미터로 단락 점검 OK.

### Phase 6. 펌웨어 빌드 & 플래싱 — `NUM_MODULES=1`로 수정 (1시간)
- **목표**: ESP32에 1모듈 펌웨어 업로드, 부팅 시 자동 호밍.
- **수정 파일**:
  - `platformio.ini` — 신규 환경 추가:
    ```ini
    [env:single-module]
    extends = esp32base
    build_flags =
        ${esp32base.build_flags}
        -DNUM_MODULES=1
    ```
    *(원본 `chainlink` 환경의 `NUM_MODULES`를 1로 줄여도 됨. 기본값은 `firmware/src/config.h:13`의 `#define NUM_MODULES (12)`.)*
  - 필요 시 `firmware/src/config.h`의 `flaps[]` 배열 순서를 실제 장착한 플랩 순서와 맞춤.
- **빌드/플래시**:
  - USB-C로 T-Display ESP32 연결
  - PlatformIO: `pio run -e single-module -t upload`
  - 시리얼 모니터 230400 baud로 부팅 로그 확인
- **산출물**: 12V 인가 + USB 연결 후 부팅 시 모듈이 1회 회전 후 홈 정지.

### Phase 7. 캘리브레이션 & 동작 테스트 (30분)
- **목표**: 'A' 같은 임의 글자에 정확히 정지하는 것 확인.
- **할 일**:
  - 브라우저에서 https://scottbez1.github.io/splitflap/ 접속, T-Display USB 시리얼 권한 부여
  - 우클릭 메뉴에서 **Calibrate** 실행, 안내대로 실제 표시 글자와 펌웨어 인덱스 동기화 → ESP32 flash에 저장
  - 'A', 'Z', ' '(공백) 등 몇 글자를 명령해 정확도 확인
- **산출물**: ✅ 임의 글자 명령 → 정확한 플랩에서 정지.
- **(선택) 다음 단계 후보**:
  - `software/chainlink/` 의 `demo.py` 로 시간/단어 자동 표시
  - 모듈 추가 빌드(2개, 3개… 동일 절차 반복, `NUM_MODULES` 증가)

---

## 이 플랜에서 "수정"할 파일 (펌웨어 단 1곳)
- `platformio.ini` — `[env:single-module]` 환경 추가 또는 기존 환경의 `NUM_MODULES=1` 변경
- (선택) `firmware/src/config.h` — 실제 장착한 플랩 순서와 `flaps[]` 배열 일치시키기

이외의 코드 수정은 입문자 1모듈 빌드에 **불필요**하다.

---

## Verification (모듈 1개가 "완성"되었다고 말할 수 있는 조건)
1. 12V + USB 연결 후 부팅 → 자동 홈 회전이 1회 일어나고 정지한다.
2. 웹 UI(scottbez1.github.io/splitflap)에서 'A' 명령 → 'A' 플랩에서 정확히 정지.
3. 'Z' 명령 → 'Z' 플랩에서 정지(긴 회전 동안 탈조 없음).
4. 시리얼 모니터에 에러 로그 없음.
5. 30분 연속 무작위 글자 명령 시 누적 오차 0 (홈 센서 자동 보정 동작 확인).

위 5개를 모두 만족하면 1개 모듈 빌드 완료로 간주.

---

## 주요 위험 & 대응
| 위험 | 대응 |
|---|---|
| 모터 사양 오발주 (5V/타사양) | Phase 1에서 12V/64:1/~100Ω/라벨 4종 확인 후 결제 |
| 자석 극성 반대로 삽입 | Phase 4에서 LED로 미리 테스트 후 Phase 5 직전에 본드 |
| 레이저컷 정렬 어긋남 | Phase 3에서 본드 경화 전 사각도 확인, 줄로 미세 다듬기 |
| 홈 센서 미동작 (캘리브레이션 실패) | `firmware/src/config.h`의 `HOME_CALIBRATION_ENABLED`를 임시 false로 두고 open-loop로 동작 확인 후 자석/배선 점검 |
| 한국에서 미국 키트 구하기 어려움 | Bezek Labs 품목은 배대지 또는 JLCPCB 자체 PCB 제작으로 대체 |

---

## 예상 일정 (실제 작업시간 기준, 발주 리드타임 별도)
- Phase 0: 1~2h
- Phase 1: **발주 후 2~4주 대기**
- Phase 2~5 (조립): 7~12h
- Phase 6~7 (펌웨어/캘리브레이션): 1.5h
- **합계 작업시간**: 약 10~16시간 + 발주 리드타임
