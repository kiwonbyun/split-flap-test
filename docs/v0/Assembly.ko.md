# Splitflap v0 조립 가이드
[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

## 소개
split-flap 디스플레이를 만들고 계신가요? 진행 중이거나 완성된 프로젝트의 사진/영상을 보내주시면 정말 기쁘게 받아보겠습니다! 이 프로젝트는 몇 년간 저의 취미였으며, 가장 멋진 부분은 단연코 다른 분들이 직접 만들고 작동시키는 모습을 보고 듣는 것입니다. 언제든지 scott@bezeklabs.com 으로 이메일을 보내주시거나 🙂, [Discord 서버에 참여](https://discord.gg/wgehm3PcrC)하셔서 더 넓은 split-flap 커뮤니티와 공유하고 토론하실 수 있습니다!

# 1. 부품 준비

부품 주문 정보는 [전체 주문 가이드 (v0)](OrderingComplete.ko.md) 또는 [간편 가이드 (v0)](OrderingEasy.ko.md)를 참고하세요.


- Controller PCB 1개
- Sensor PCB 4개
- 자석 4개
- 컨트롤러 보드 및 센서 보드 부품들

&nbsp;

- 레이저 컷 패널 4세트
- 글자 스티커 팩 2개
- 모터 4개
- 센서 케이블 4개
- 플랩 약 165개 (160개가 필요함)
- M4 볼트 약 46개 (44개가 필요함)
- M4 너트 약 46개 (44개가 필요함)

&nbsp;

- 12V 2A 전원 공급장치
- 도구:
    - 미터법 육각 렌치
    - 납땜 용품
    - 캘리퍼스 또는 미터 자
    - 공작용 칼
    - 비닐 랩과 유리 보관 용기 (글자 스티커 부착용)
    - [플랩을 직접 자르는 경우] 배지 슬롯 펀치
# 2. Sensor PCB 조립
https://www.youtube.com/watch?v=vQMnWK6PwJ0&



> 💡 **새로 추가됨 (영상에는 없음!):** 레이저 컷 파일에는 5.8mm 간격을 직접 측정하지 않고도 Hall sensor를 정확하게 배치할 수 있는 지그(jig)가 포함되어 있습니다. 아래 사진을 참고하세요.
>  
> 최신 PCB 디자인에는 센서를 더 쉽게 납땜할 수 있도록 구멍 간격이 더 넓어진 홀이 있습니다. 센서의 핀을 바깥쪽으로 구부려 구멍에 맞춰야 합니다.

대략적인 단계는 다음과 같습니다:

- 90도 핀 헤더를 *상단 면에서* 납땜합니다 ([0:21](https://www.youtube.com/watch?v=vQMnWK6PwJ0&t=21s))
- Hall sensor의 리드를 90도로 구부립니다 ([2:00](https://www.youtube.com/watch?v=vQMnWK6PwJ0&t=120s))
- PCB 뒷면(핀 헤더의 반대쪽)에서 Hall sensor를 삽입합니다 ([2:45](https://www.youtube.com/watch?v=vQMnWK6PwJ0&t=165s))
- 센서 뒷면과 PCB 사이에 약 5.8mm 간격이 생기도록 Hall sensor를 조정합니다 ([3:00](https://www.youtube.com/watch?v=vQMnWK6PwJ0&t=180s))
- Hall sensor를 제자리에 납땜합니다 ([3:30](https://www.youtube.com/watch?v=vQMnWK6PwJ0&t=210s))
- 남는 핀 길이를 잘라냅니다 ([4:24](https://www.youtube.com/watch?v=vQMnWK6PwJ0&t=264s))

<a href="https://paper-attachments.dropbox.com/s_DBFFE29691B90C2EDDE2A687CA2E739A14BF58F2DE09EF37D4E0562373661460_1643174894237_123306848-a4ecbc00-d4d6-11eb-9b46-d47165f3abe7.jpg">
    <img src="https://paper-attachments.dropbox.com/s_DBFFE29691B90C2EDDE2A687CA2E739A14BF58F2DE09EF37D4E0562373661460_1643174894237_123306848-a4ecbc00-d4d6-11eb-9b46-d47165f3abe7.jpg" width="500"/>
</a>
<a href="https://paper-attachments.dropbox.com/s_DBFFE29691B90C2EDDE2A687CA2E739A14BF58F2DE09EF37D4E0562373661460_1643174893952_123306852-a6b67f80-d4d6-11eb-9466-73a11368e9a7.jpg">
    <img src="https://paper-attachments.dropbox.com/s_DBFFE29691B90C2EDDE2A687CA2E739A14BF58F2DE09EF37D4E0562373661460_1643174893952_123306852-a6b67f80-d4d6-11eb-9466-73a11368e9a7.jpg" width="500" />
</a>


> 흰색 아크릴로 잘라낸 센서 간격 지그


<a href="https://paper-attachments.dropbox.com/s_DBFFE29691B90C2EDDE2A687CA2E739A14BF58F2DE09EF37D4E0562373661460_1643174982515_123307566-7de2ba00-d4d7-11eb-8d17-976c0b2a1335.png">
    <img src="https://paper-attachments.dropbox.com/s_DBFFE29691B90C2EDDE2A687CA2E739A14BF58F2DE09EF37D4E0562373661460_1643174982515_123307566-7de2ba00-d4d7-11eb-8d17-976c0b2a1335.png" width="500" />
</a>

> 레이저 컷 부품이 통째로 한 장에 잘려 도착한 경우(예: Ponoko는 그렇지만 Elecrow는 다름), 위 그림에서 빨간색으로 강조 표시된 모터 컷아웃 안에서 지그를 찾을 수 있습니다.


# 3. 기계 조립

참고: MDF/목재 대신 아크릴을 사용하는 경우, 부품이 잘 맞지 않으면 *억지로 끼우지 마십시오*. 아크릴은 매우 깨지기 쉽고 *반드시* 갈라집니다. 필요한 경우 작은 줄을 사용하여 여분의 재료를 제거하십시오. 디자인은 꼭 맞도록 설계되었지만, 레이저 커터마다 제거되는 재료의 양이 다를 수 있어 구멍이나 슬롯이 작게 잘릴 수 있습니다.

https://www.youtube.com/watch?v=zHM8W6Rm2i4&


대략적인 단계는 다음과 같습니다:

- 레이저 컷 부품을 분리합니다 ([0:12](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=12s))
- 보호 필름을 제거합니다 ([0:34](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=34s))
- 스풀(Spool):
    - 스풀 지지대(strut)를 조립합니다 ([1:31](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=91s))
    - 스풀 고정 부품에 볼트와 너트를 부착합니다 ([2:16](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=136s))
    - 스풀 디스크에 스풀 지지대를 끼웁니다 ([2:50](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=170s))
    - 다른 스풀 디스크를 스풀 지지대에 눌러 끼웁니다 ([3:25](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=205s))
    - 자석의 극성을 확인하고 자석을 스풀에 삽입합니다 ([3:40](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=220s))
- 모터를 측면 구멍을 통과시키고 볼트 2개로 고정합니다 ([5:05](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=305s))
- Hall sensor 모듈을 장착하고 볼트로 고정합니다 ([6:02](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=362s))
- 스풀을 모터 샤프트에 눌러 끼웁니다 ([7:15](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=435s))
- 레이저 인그레이브 글자가 위쪽을 향하고 원형 구멍이 뒤쪽을 향하도록 하여 바닥 부품을 왼쪽 부품에 압입합니다 ([7:50](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=470s))
- 원형 구멍이 뒤쪽을 향하도록 하여 상단 부품을 왼쪽 부품에 압입합니다 ([8:14](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=494s))
- 오른쪽 부품을 상단/바닥 부품에 압입하고 스풀 축과 정렬합니다 ([8:34](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=514s))
- 두꺼운 면이 왼쪽에 오도록 하여 전면 부품을 상단/바닥 부품에 압입합니다 ([9:05](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=545s))
- 캡티브 너트와 볼트를 사용하여 인클로저 부품들을 고정합니다 ([9:27](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=567s))
- 플랩 백스톱(backstop) 볼트/너트를 부착합니다 ([10:26](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=626s))
- 다른 모듈에 연결하려면 전면 부품을 제거하고, 모듈 간 커넥터를 삽입한 후, 전면 부품을 다시 끼웁니다 ([10:55](https://www.youtube.com/watch?v=zHM8W6Rm2i4&t=655s))
# 4. 글자 스티커 부착
https://www.youtube.com/watch?v=3lFECISLwyI&

## 추가 참고 사항 (위 영상에는 없음):

기본적으로 splitflap 코드는 플랩이 특정 순서로 나타난다고 가정하므로, 다음과 같이 스티커를 부착하는 것이 가장 쉽습니다:

    (space), A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, (period), (comma), (apostrophe)

참고: 주로 *카운트 다운*하는 디스플레이의 경우, 카운트 다운 시 매번 한 바퀴 전체를 회전할 필요가 없도록 숫자 순서를 반대로 하는 것이 합리적일 수 있습니다.

기본값과 다른 것을 사용하는 경우, 글자가 어떤 순서로 나타나는지 알려주기 위해 제어 소프트웨어를 약간 수정해야 합니다.

6단계까지는 플랩을 스풀에 삽입하지 마십시오 (순서대로 보관만 하십시오).

# 5. 전자 부품 조립

전자 부품 조립 및 사용에 대한 전체 지침은 [Electronics Guide](../ElectronicsGuide.ko.md)를 참조하십시오.


# 6. 최종 조립 및 보정

대략적인 단계:

- 설정
    - [Microsoft Visual Studio Code](https://code.visualstudio.com/)를 다운로드하여 설치합니다.
    - PlatformIO와 splitflap 코드를 설정하려면 다음 단계를 따르십시오 ([영상 보기](https://youtu.be/uyG5mEKzKcg) [스크린캐스트](https://www.youtube.com/watch?v=C8mcExG-VVo)):
        - PlatformIO 확장 프로그램을 설치합니다.
        - Explorer 사이드바에서 “Clone Respository”를 선택하고 git 저장소 URL을 입력합니다: `https://github.com/scottbez1/splitflap.git`
            - 참고: GitHub에서 소스를 zip 파일로 다운로드하는 것은 **권장하지 않습니다**. 문제가 발생했을 때 도움을 받기 어려워지기 때문입니다 (git은 체크아웃한 코드의 정확한 버전과 변경 사항을 추적하므로 디버깅에 큰 도움이 됩니다).
        - 저장소를 엽니다. PlatformIO 확장 프로그램이 실행될 수 있도록 폴더를 “Trust”해야 할 수 있습니다.
        - 디바이스에 splitflap 펌웨어를 설치하고 시리얼 모니터를 엽니다.
            - PlatformIO 사이드바를 열고 `chainlink` → `Upload and Monitor` 작업을 실행합니다.
- 다음과 같은 시작 메시지가 나타나는지 확인합니다:
    {"type":"init", "num_modules":12, "character_list":" abcdefghijklmnopqrstuvwxyz0123456789.,'"}
- 모든 모터와 센서를 연결합니다.
- 12V 모터 전원을 연결합니다.
- 마이크로컨트롤러를 재시작합니다.
    - 스풀이 홈 위치에 도달할 때까지 천천히 회전한 다음, 전속력으로 한 바퀴 회전해야 합니다.
    - 스풀이 올바른 방향으로 회전하는지 확인하십시오.
    - 다음 단계로 진행하기 전에 4개의 RGB LED가 모두 녹색인지 확인하십시오.
- Serial Monitor 열기 - 모터가 올바르게 구성되었는지 확인하기 위해 몇 가지 테스트를 수행합니다.
    - `=    \n` (등호, 스페이스 4개, 줄바꿈) 을 보냅니다.
    - 모든 모터가 한 바퀴 완전히 회전하고 멈추는지 확인합니다.
    - 이 과정을 10번 더 반복하고, 이 테스트 중에 모듈이 재보정(시작 절차에서처럼 천천히 회전)할 필요가 없는지 확인합니다.
    - 보고된 `"count_missed_home":0, "count_unexpected_home":0` 값이 4개 모듈 모두 0인지 확인합니다.
- Serial Monitor에서 `@`를 보내 모든 모듈이 강제로 재보정되도록 하고, `=    \n`을 보내 모든 모듈이 홈 위치로 이동하도록 합니다.
- 플랩을 설치합니다.

  ![엄지손가락으로 플랩을 부드럽게 구부려 추가하거나 제거합니다](../img/flaps/addRemoveSpool.jpg)

    - 빈(공백) 문자의 상단 및 하단 절반을 가져오는 것부터 시작합니다. 상단 절반을 스풀의 “-” 표시가 있는 구멍에 삽입합니다. 하단 절반을 그 아래의 스풀 구멍에 삽입합니다.
    - 스풀을 몇 글자 앞으로 회전시키고 (예: `=e\n`을 보내거나 손으로 스풀을 부드럽게 회전시켜) 다음 몇 개의 플랩을 삽입합니다. 40개의 플랩이 모두 설치될 때까지 이 과정을 반복합니다.
- 보정
    - Serial Monitor를 사용하여 모듈에 문자를 보냅니다.
    - 일부 글자에서 모듈이 일관되게 충분히 회전하지 않거나 약간 너무 많이 회전한다면, 홈 위치 센서를 조정해야 할 수 있습니다:
        - Hall sensor 볼트를 풉니다.
        - 모듈이 충분히 회전하지 않았다면, 센서를 모듈의 **뒤쪽**으로 밀어줍니다.
        - 모듈이 약간 너무 많이 회전했다면, 센서를 모듈의 **앞쪽**으로 밀어줍니다.
        - Hall sensor 볼트를 다시 조입니다.
        - `@`를 보내 재보정합니다.
        - 보정이 더 나아졌는지 확인합니다.

# 레거시 Classic Controller 조립

https://www.youtube.com/watch?v=VmKuWdmhPtM&&feature=youtu.be


극성이 있는 부품에는 아래에서 ⚠️ 기호로 표시되어 있습니다 - 방향을 정확하게 맞추도록 주의하십시오!

권장 조립 순서:

- 4개의 WS2812b RGB LED - U5, U6, U7, U8 - A B C D 라벨 근처 중앙
    - ⚠️ 극성을 정확히 맞춰야 합니다 - LED 노치는 직각 실크스크린 라인과 정렬됩니다 - 왼쪽 상단 모서리 (일부 PCB에서는 이 표시가 없거나 잘 보이지 않을 수 있으므로, 노치가 왼쪽 상단 모서리를 향하는지만 확인하십시오)
- Arduino 핀 헤더 (BOTTOM SIDE):
    - 3핀 직선형 수 헤더 - 하단의 “Arduino D4 D5 D6” 라벨
    - 2x3 암 헤더 - 하단의 ISP 라벨
    - 2핀 직선형 수 헤더 - 하단의 VIN 라벨
- 470 저항 (노랑 보라 갈색) - R9 (상단 면 중앙, 두 개의 MIC5842 자리 사이)
- 왼쪽 상단 모서리:
    - 2핀 직선형 수 헤더 - JP1
    - **노란색** LED - D1 (Mot+) - ⚠️ 극성을 정확히 맞춰야 합니다 - 평평한 면을 실크스크린에 맞추십시오
    - **녹색** LED - D2 (5V) - ⚠️ 극성을 정확히 맞춰야 합니다 - 평평한 면을 실크스크린에 맞추십시오
    - 2.2k 저항 (빨강 빨강 빨강) - R1
    - 220 저항 (빨강 빨강 갈색) - R7
- 커패시터:
    - 100uF 전해 커패시터 - C1 - ⚠️ 극성을 정확히 맞춰야 합니다
    - 100uF 전해 커패시터 - C3 - ⚠️ 극성을 정확히 맞춰야 합니다
    - 0.1uF 커패시터 - C2 (“A” LED의 왼쪽)
- 배럴 잭 커넥터 - 우측 상단의 “5-12V” 라벨
- 센서 커넥터 (납땜 시 정확한 정렬을 위해 센서 케이블을 3개 모두에 꽂은 상태로 한 번에 배치하십시오)
    - 4핀 직선형 수 헤더 - “GND” 라벨
    - 4핀 직선형 수 헤더 - “5V” 라벨
    - 4핀 직선형 수 헤더 - “A” 및 “D” 라벨
- 47k 저항 (노랑 보라 주황) - R3 R4 R5 R6 R10
- 모터 커넥터 - P1 P2 P3 P4 - ⚠️ 극성을 정확히 맞춰야 합니다 (실크스크린에 맞춤)
- IC - 극성을 정확히 맞추도록 절대적으로 주의하십시오!!!!
    - MIC5842 - U2 - ⚠️ 극성을 정확히 맞춰야 합니다 (실크스크린에 맞춤 - 노치가 **왼쪽**을 향함)
    - MIC5842 - U4 - ⚠️ 극성을 정확히 맞춰야 합니다 (실크스크린에 맞춤 - 노치가 **왼쪽**을 향함)
    - 74HC165 - U3 - ⚠️ 극성을 정확히 맞춰야 합니다 (노치가 **아래쪽**을 향함 - 1번 핀 근처의 직각 실크스크린 라인 참조)


![선택적 EXP OUT 커넥터가 장착된 조립된 Driver PCB (EXP OUT은 4개 이상의 모듈을 지원하기 위해 컨트롤러를 체인으로 연결할 때만 필요합니다. 자세한 내용은 아래 참조)](https://paper-attachments.dropbox.com/s_DBFFE29691B90C2EDDE2A687CA2E739A14BF58F2DE09EF37D4E0562373661460_1572753846051_file.jpeg)


다음 부품들이 남아 있어야 합니다:

- 점퍼 커넥터 - 일반적으로 필요하지 않은 선택적 부품입니다. 정말로 필요하다고 확신하지 않는 한 빼두십시오. **JP1 점퍼가 꽂혀 있는 상태에서는 절대로 Arduino의 USB 케이블을 어디에도 연결하지 마십시오!** JP1은 Arduino를 드라이버 보드의 모터 전원으로 구동하여 컴퓨터 연결 없이도 Arduino가 작동할 수 있게 해줍니다. - 이론적으로 Arduino는 VIN 핀을 통해 USB 커넥터로 12V가 역류하는 것을 방지하지만, 그 보호 기능이 실패하거나 (저렴한 모조 Arduino 클론에서는 어떤 이유로 구현되지 않을 수도 있음) 작동하지 않으면 컴퓨터가 손상될 위험이 있습니다.
