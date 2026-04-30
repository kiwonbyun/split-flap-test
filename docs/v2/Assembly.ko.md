# Splitflap v2 조립 가이드
[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

# 전자장치 1부: 센서 PCB

먼저 인쇄된 안내에 따라 패널 외곽의 레일을 제거한 다음, 개별 센서 보드들을 분리합니다.

![레일 분리하기](https://github.com/user-attachments/assets/7dc43abd-eb2d-48e1-9d75-38d7ca5307b9)
![센서 분리하기](https://github.com/user-attachments/assets/94798594-3956-457c-9944-7eb908802c60)


센서 보드 사이에 남아 있던 스페이서 조각들은 펜치를 사용해 깔끔하게 정리하는 것이 좋습니다.

![](https://github.com/user-attachments/assets/aee4f950-1657-4ca8-9149-f547db5d1adc)
![](https://github.com/user-attachments/assets/6e6aa732-e3dc-48e1-977a-7d642bb4bb4c)


그런 다음 핀이 라벨링되어 있고 “MOTOR”라는 표시가 보이는 면에서 라이트 앵글 헤더를 삽입합니다. 핀 헤더는 PCB 아래쪽으로 돌출되어야 합니다.

![](https://github.com/user-attachments/assets/efd6e9ce-992e-4b58-9436-f1ccdfb29c41)


PCB를 뒤집어서 헤더를 납땜합니다.

![](https://github.com/user-attachments/assets/42bd9cd7-ff77-44f4-9791-78984516ac6c)
![](https://github.com/user-attachments/assets/6c4da269-905a-43d9-9512-75a7c5b1bb0c)


# 전자장치 2부: Chainlink Driver와 Chainlink Buddy [T-Display]
## Chainlink Driver PCB 조립

그림과 같이 커넥터를 삽입하고 납땜합니다. 양쪽 끝에 있는 두 개의 IDC 커넥터는 모두 같은 방향(노치가 왼쪽을 향하도록)을 향해야 합니다.

![](https://github.com/user-attachments/assets/3d87f0e8-7d29-4cd8-bdf9-094483b01335)


리본 케이블을 그림과 같이 커넥터에 삽입한 뒤, 바이스나 펜치로 *부드럽게* 눌러 닫습니다. 반대쪽 끝의 다른 커넥터에서도 같은 작업을 반복하되, 두 커넥터가 **같은** 방향(노치가 왼쪽)을 향하도록 해야 합니다.

![](https://github.com/user-attachments/assets/0fb7ec7c-3cba-4c0e-96bf-d244130d39ed)


(권장하지 않지만, 선택적으로 커넥터에 스트레인 릴리프를 설치할 수도 있습니다. 리본 케이블을 커넥터 위로 접어 올린 뒤 플라스틱 부품을 끼워 딸깍 소리가 날 때까지 눌러 고정합니다. 다만 케이블 길이가 다소 손실되고 커넥터가 더 두껍고 커지므로, 케이블이 거의 움직이지 않을 환경이라면 굳이 설치할 가치는 없다고 판단합니다.)


## Chainlink Buddy 조립

커넥터를 제자리에 납땜합니다(IDC 커넥터의 노치가 PCB에 표시된 대로 왼쪽을 향하는지 확인하세요).

**T-Display Buddy**

![](https://github.com/user-attachments/assets/c7f3a752-202c-4917-b93b-4c45519dcde2)
![](https://github.com/user-attachments/assets/919f9e2e-90d3-4ede-a640-c2ddf2db9ece)



T-Display 본체에는 박스에 포함된 두 줄짜리 수 헤더를 납땜합니다. 그런 다음 모듈 전체를 Buddy 보드에 납땜한 암 헤더에 꽂습니다.

T-Display Buddy PCB의 좌측 하단에 C1, C2 라벨이 붙은 빈 자리와 3개의 스루홀이 있을 수 있는데, 걱정할 필요 없습니다. 이는 고급 빌드를 위한 선택 부품이며 기본 셋업에는 필요하지 않습니다.
자세한 내용은 [Standalone T-Display 동작](../ElectronicsGuide.ko.md#8-optional-standalone-t-display-operation)을 참조하세요.


![](https://paper-attachments.dropboxusercontent.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1647556549613_PXL_20220317_223022886.jpg)


참고: T-Display에는 종종 작은 빨강/검정 와이어 하니스와 커넥터가 함께 제공되지만, Chainlink Buddy와 함께 사용할 수 없으므로 폐기하면 됩니다.

![](https://github.com/user-attachments/assets/ca90d776-3e4b-4e59-9943-03f6655c3e4f)




**Breadboard Buddy (T-Display Buddy 대체)**
다른 ESP32 모듈을 사용하고 싶다면, Breadboard Buddy PCB를 사용해 IDC 케이블을 브레드보드에 손쉽게 연결할 수 있습니다.

![](https://github.com/user-attachments/assets/1bfc087c-02e9-4deb-a77f-ef73282977bc)
![](https://github.com/user-attachments/assets/03e3e7c4-720b-4a18-bee5-24193d3f922a)




## Chainlink Driver를 Chainlink Buddy에 연결하기

먼저 전원 공급 장치나 모듈의 모터/센서 없이 Chainlink Driver만 연결해 테스트해 보겠습니다. 기본 전자장치가 정상 동작함을 확인한 뒤에 나머지를 연결할 것입니다.

**T-Display**

- Chainlink Buddy의 **Output**에서 Chainlink Driver의 **Input**으로 리본 케이블을 연결합니다.
- Chainlink Driver의 “Logic 3.3-5V” 스크류 터미널과 Chainlink Buddy의 “3.3V” 스크류 터미널을 와이어로 연결합니다.
- Chainlink Driver의 “GND” 스크류 터미널과 Chainlink Buddy의 “GND” 스크류 터미널을 와이어로 연결합니다.
- Chainlink Driver의 “Motor 5-12v” 스크류 터미널과 Chainlink Buddy의 “12V” 스크류 터미널을 와이어로 연결합니다.
- ⚠️ Chainlink Buddy를 사용할 때는 절대 T-Display의 배터리 커넥터(TTGO T-Display 모듈 하단의 작은 흰색 커넥터)에 배터리를 연결하지 마세요!

![](https://github.com/user-attachments/assets/a0b0708f-717e-4ff0-b01c-bba70b16b272)



**Breadboard (T-Display Buddy를 사용하지 않는 경우)**
T-Display Buddy 대신 Breadboard Buddy와 함께 다른 ESP32 모듈을 사용한다면, 전체 [Chainlink User Guide](../ElectronicsGuide.ko.md)의 안내를 참조하세요.


# 기구부: 레이저 컷 조립
![](https://github.com/user-attachments/assets/9bc5850b-8e9e-46d7-a3f6-c01906b74ee5)


⚠️⚠️⚠️
아크릴 부품을 사용했다면, 한 번에 맞물리지 않는 경우 절대 강제로 끼우지 마세요. 아크릴은 쉽게 깨집니다! 필요하면 작은 보석용 줄을 사용해 부품을 살짝 다듬어 가며 맞추세요.
⚠️⚠️⚠️


## 플랩 드럼

M4x10 볼트와 너트를 가져와 스페이서 부품에 느슨하게 조립합니다. 볼트가 어느 정도 자유롭게 회전할 수 있어야 합니다. 이 부품은 따로 보관해 둡니다.

![](https://github.com/user-attachments/assets/fd77c5ab-8d4d-42d8-95d3-cea81b99e7e2)


4개의 스트럿을 잡고 박스 모양을 만듭니다. 단차가 있는 탭 끝이 위쪽을 향하게 합니다…

![](https://github.com/user-attachments/assets/4847b5a0-da71-4129-9aea-e9091c4f5679)


… 그 위에 스페이서를 올리되 볼트가 위/바깥쪽을 향하도록 합니다.

![](https://github.com/user-attachments/assets/a62f36a4-c5bd-436a-8a0a-4e4f67cc2d94)


볼트/너트를 돌려 너트의 모서리가 스트럿 탭 2개와 평행을 이루도록 한 뒤, 중앙에 육각 구멍이 있는 휠을 끝부분에 끼웁니다.

![](https://github.com/user-attachments/assets/b9b9e008-6d79-4ece-8595-e944ed243a9b)


그런 다음 반대쪽 끝의 탭에 다른 휠을 결합합니다. 레이저 컷 부품이 다소 헐거우면 이 시점에서 전체 조립체를 손으로 잡아 고정해야 할 수도 있습니다.

![](https://github.com/user-attachments/assets/86f69f9c-dc47-4a1a-9633-3a80c26a7526)


플랩 드럼을 영구 고정하려면 (촉진제와 함께!) CA 글루를 사용하는 것을 권장합니다. 제가 즐겨 쓰는 글루는 Bob Smith Industries thick CA glue입니다([제휴 링크](https://amzn.to/3REVhEM), 또는 [비제휴 링크](https://a.co/d/05jtD1j4)). 참고: 접착 후에는 M4 너트+볼트를 끼울 수 없으므로, 앞에서 미리 설치했는지 반드시 확인하세요!

중앙 스트럿과 휠 끝 사이의 각 접합부에 CA 글루를 작은 점만큼 떨어뜨립니다(총 8개 지점). 이 단계의 작업 가능 시간은 약 30초에서 1분 정도입니다.

![](https://github.com/user-attachments/assets/4bd48f69-88fd-4d32-8bef-19328aea3053)
![](https://github.com/user-attachments/assets/1fe7fdb8-ff59-4e99-88b7-1dcfb29301b8)


조립체가 다소 헐겁다면, **휠 양쪽 끝이 비틀려 있지 않은지 반드시 확인하세요**. 그렇지 않으면 플랩이 비스듬하게 매달리게 됩니다! 왜 문제가 되는지는 아래 사진을 참조하세요:

![❌ 글루 작업 시 드럼이 비틀리지 않게 하세요! ❌ 아직 플랩을 설치하지는 않았지만, 비틀린 드럼은 결국 이런 모습이 됩니다 — 플랩이 비스듬히 매달리고 전면 창의 옆면에 걸려 막힐 수 있습니다!!!](https://github.com/user-attachments/assets/d6641b01-5fa4-41ab-8741-06416aae5fdb)


드럼이 완전히 조립되고 비틀어지지 않았음을 확인한 뒤, CA 촉진제를 분사해 글루를 빠르게 굳힙니다. 부품이 특히 헐거우면, 장갑을 낀 손으로 조립체를 잡고 있으면서 CA 촉진제를 분사하는 것이 좋습니다.

![](https://github.com/user-attachments/assets/de5e5030-7959-44a6-9b84-423ec60a67c3)


💡 **중요한 CA 글루 팁:** 촉진제를 사용하지 않으면 아크릴 부품 전체에 흰 안개나 잔여물이 생기기 쉽습니다. 이는 미량의 CA 글루가 기화되어 공기 중 수분과 반응해 굳으면서 부품(과 주변 책상, 컴퓨터 등!)에 영구적인 흰 안개로 침착되기 때문입니다. 추천하는 Bob Smith Industries 글루를 동봉된 촉진제 스프레이와 함께 사용했을 때는 CA 안개/포깅 문제가 한 번도 없었습니다! ([제휴 링크](https://amzn.to/3REVhEM), 또는 [비제휴 링크](https://a.co/d/05jtD1j4))


촉진된 CA 글루가 경화되도록 몇 분 기다린 후, 육각 렌치를 사용해 내부의 M4 볼트를 조여 단단히 고정합니다.

![](https://github.com/user-attachments/assets/f8bb0357-8065-4b66-9b64-a7e8ee6cf0b6)



## 모터 + 센서 + 좌측 인클로저

가운데에 둥근 사각형 구멍이 뚫려 있는, 더 넓은 사이드 인클로저 부품을 가져와 아래 그림과 같은 방향으로 모터 케이블을 구멍에 통과시킵니다.

![](https://github.com/user-attachments/assets/144d1159-13ce-48f2-86d8-3efec033a412)
![](https://github.com/user-attachments/assets/e3d7fa5d-a40b-49e1-a414-b9a280abca51)


그런 다음 모터 위에 센서 PCB를 올리고, M4x10 볼트 2개를 모터 마운트 구멍에 삽입합니다.

![](https://github.com/user-attachments/assets/587dc552-79e4-4975-9429-f4506a779b25)
![](https://github.com/user-attachments/assets/dde753a1-1041-410c-a4b9-fa8bd5addea8)


조립체를 뒤집어 각 볼트에 너트를 끼운 뒤, 육각 렌치로 너트를 단단히 조입니다.
![](https://github.com/user-attachments/assets/1fbec3b4-64bb-4268-ae60-594752cdfd14)
![](https://github.com/user-attachments/assets/5a0c872e-00eb-49ec-969f-a85f7dcb1061)

![](https://github.com/user-attachments/assets/a70ff55a-27eb-4ce8-9be8-03ba09edd3a4)

## 자석

이제 자석을 플랩 드럼에 설치합니다. 센서는 자석의 한쪽 극에서만 동작하고 반대쪽에서는 동작하지 않으므로, 자석의 방향이 매우 중요합니다!

다행히 센서 PCB의 LED를 사용하면 올바른 설치 방향을 쉽게 판별할 수 있습니다.

센서를 Chainlink Driver에 꽂고, Chainlink Driver를 ESP32/Chainlink Buddy에 연결한 뒤, 3.3V 로직 전원 스크류 터미널이 연결되어 있는지 확인합니다.

![](https://github.com/user-attachments/assets/2802c27b-cd9c-459d-93fd-7bd0f1095242)


자석을 가까이 댔을 때, 한쪽 면에서는 LED가 켜지고 다른 면에서는 켜지지 않을 것입니다.

![자석이 올바른 방향일 때 센서 PCB의 LED가 켜집니다](https://github.com/user-attachments/assets/a9dca1d9-0d0e-4b3e-807e-55e92aefe5ef)
> 자석이 올바른 방향일 때 센서 PCB의 LED가 켜집니다

![이것은 잘못된 방향입니다 - LED가 켜지지 않습니다](https://github.com/user-attachments/assets/9c89b987-2ebd-4904-8152-f4ea99b88fc0)
> 이것은 잘못된 방향입니다 - LED가 켜지지 않습니다


LED가 켜졌던 방향으로 자석을 플랩 드럼에 설치합니다.

펜치의 한쪽 턱에 자석을 붙인 뒤 **부드럽게** 플랩 드럼에 눌러 넣는 방법이 잘 통합니다 — 살짝 이상의 힘이 필요하다면 절대 무리하게 누르지 마세요. 아크릴이 깨질 수 있습니다. 줄로 구멍을 살짝 넓힌 뒤 다시 시도하세요.

![올바른 방향으로 펜치에 붙은 자석](https://github.com/user-attachments/assets/940501ef-9e59-4789-87be-1ad323f771f9)
![면이 맞도록 부드럽게 눌러 넣기](https://github.com/user-attachments/assets/fed6cdb1-7a86-4679-85a3-1ba4b206bc51)

![설치된 자석](https://github.com/user-attachments/assets/a1896f2b-16a1-49f2-847b-af04b27345c7)


플랩 드럼을 모터에 결합할 때 자석 방향이 올바른지 다시 확인하세요. 마찬가지로 모터 샤프트에 부드럽게 압입되어야 합니다. 너무 큰 힘이 필요하면 줄로 구멍을 넓힌 뒤 끼우세요.

![](https://github.com/user-attachments/assets/5743c10b-63c1-45f6-89cc-bb294c631519)


자석이 약간 헐겁다면, 드럼 안쪽의 뒷면에 CA 글루를 한 방울 떨어뜨려 고정할 수 있습니다.


## 상/하/우측 인클로저 부품

상단과 하단 부품은 서로 호환됩니다. 상단 부품과 (모터가 장착된) 좌측 부품의 맞물리는 탭과 슬롯을 찾습니다…

![](https://github.com/user-attachments/assets/d62908ee-4559-40ad-9908-14d165833c11)


… 상단 부품의 노치에 너트를 끼우고(아래처럼 손가락으로 뒤에서 받쳐 주는 방식이 편리합니다) M4x10 볼트를 조여 부품을 결합합니다.

![](https://github.com/user-attachments/assets/0bdd09cc-ffc7-4987-9717-bf83afc7f62c)


하단 부품에서도 같은 과정을 반복한 뒤, 우측 부품도 결합합니다.

전면 페이스를 설치하기 전에, 우측 부품의 슬롯 가운데에 M4x10 플랩 백스톱 볼트를 삽입하고 너트로 고정합니다. 위치는 나중에 미세 조정할 수 있지만, 보통 슬롯의 중앙에서 시작하는 것이 좋습니다.

![백스톱 볼트를 슬롯 중앙에 두고 시작합니다](https://github.com/user-attachments/assets/ff1fa112-db3c-42f6-8aad-2a73d22f0481)
백스톱 볼트를 슬롯 중앙에 두고 시작합니다

![플랩 백스톱 볼트가 모듈 안쪽 중앙으로 돌출되어 있습니다](https://github.com/user-attachments/assets/05b6a470-f6fd-4594-9c1b-445c6fbd735d)
플랩 백스톱 볼트가 모듈 안쪽 중앙으로 돌출되어 있습니다


이제 M4 볼트/너트를 사용해 전면 페이스를 상단과 하단 부품에 고정합니다.

![](https://github.com/user-attachments/assets/ffa5ab54-01f5-47f9-bc1a-7660309deaa5)



## 플랩 설치

이제 플랩을 설치할 수 있습니다. 가장 먼저 설치할 플랩은 빈 칸과 글자 “A”의 아래쪽 절반이 그려진 플랩이어야 합니다.

![](https://github.com/user-attachments/assets/64c6464c-8fd1-401d-98f0-33bb0e2f26b1)


첫 번째 플랩은 아래 그림과 같은 위치 — 플랩 드럼의 자석으로부터 90도 “앞” — 에 설치합니다. (홈 위치는 나중에 소프트웨어로 보정되므로 이 위치 자체가 기술적으로 결정적인 것은 아니지만, 모듈들 간의 일관성을 유지하기 위한 좋은 관례입니다.)

![](https://github.com/user-attachments/assets/f07657e3-4ea5-4ef0-93bb-16fd3e7befe7)


플랩을 설치하려면, 플랩을 검지와 중지 사이에 두고 엄지로 가운데를 눌러 살짝 휘게 합니다. 플랩의 한쪽 핀을 플랩 드럼에 넣은 뒤, 다른 쪽 핀을 조심스럽게 정렬하고 엄지의 압력을 천천히 풀어 플랩이 펴지면서 두 번째 핀이 들어가도록 합니다.

![플랩을 부드럽게 휘어 넣기](https://github.com/user-attachments/assets/1f73f79f-cba4-466a-91da-10aa7d61e9e3)
> 플랩을 부드럽게 휘어 넣기

다음 51개의 플랩에 대해서도 같은 작업을 반복하며, 진행 중에 순서가 맞는지 반드시 확인하세요.

![](https://github.com/user-attachments/assets/93e0a8a1-47ae-461b-961b-c38ece7434bc)



# 펌웨어
- [Microsoft Visual Studio Code](https://code.visualstudio.com/)를 다운로드하고 설치합니다.
- 다음 단계에 따라 Platform IO와 splitflap 코드를 설정합니다:
    - Platform IO 확장 프로그램을 설치합니다.
    - 탐색기 사이드바에서 “Clone Repository”를 선택하고 git 저장소 URL `https://github.com/scottbez1/splitflap.git`을 입력합니다.
    - 클론이 완료되면 폴더를 여는 옵션을 선택합니다.
    - Platform IO 확장 프로그램이 정상적으로 동작하도록 폴더를 “Trust”해야 할 수도 있습니다.

연결한 Chainlink Driver가 지원하는 모듈 수와 일치하도록 `platformio.ini`의 NUM_MODULES를 설정해야 합니다. Chainlink Driver가 1개라면 6으로 설정하면 됩니다.


    [env:chainlink]
    extends=esp32base
    build_flags =
        ${esp32base.build_flags}
        -DCHAINLINK
        -DNUM_MODULES=6


- Mac 사용자: 최신 버전의 ESP32 T-Display에 사용되는 CH9102 USB-시리얼 어댑터용 최신 드라이버를 설치해야 할 가능성이 큽니다: https://learn.adafruit.com/how-to-install-drivers-for-wch-usb-to-serial-chips-ch9102f-ch9102/mac-driver-installation
- VS Code에서 ESP32 T-Display로 코드를 업로드하려면 다음을 수행해야 합니다(아래 스크린샷 참조):
> 1) Platform IO 사이드바를 엽니다(왼쪽의 외계인 아이콘 클릭).
> 2) 화면 하단의 “env” 버튼을 클릭한 뒤 화면 상단의 드롭다운에서…
> 3) …환경으로 “env:chainlink”를 선택합니다 — 이렇게 하면 ESP32에 맞는 코드 자동 완성과 구문 강조가 설정됩니다.
> 4) Platform IO 사이드바의 “General” 섹션을 펼치고 `Upload and Monitor`를 클릭합니다.

![](https://github.com/user-attachments/assets/a05ff348-9ac6-4e99-9ea6-8f27750397d9)

- ESP32를 리셋하면 Chainlink Driver의 LED가 빠르게 깜빡이고 시리얼 모니터에 루프백이 정상이라는 메시지가 표시되어야 합니다. 루프백 오류 메시지가 보이면 계속 진행하기 전에 문제를 먼저 해결하세요.



## 모듈 및 전원 연결

**모터**

- 흰색 커넥터에 꽂습니다. Chainlink Driver PCB는 모듈 *뒤*에 위치하도록 설계되어 있기 때문에, 모듈 연결은 *오른쪽에서 왼쪽* 순서로 배치되어 있습니다. 따라서 첫 번째 모듈은 PCB의 **오른쪽** “A” 위치에 꽂힙니다.

**센서**

![](https://github.com/user-attachments/assets/fe742b01-ac38-499c-9a66-9c0df9da36a6)

- 센서 케이블을 해당하는 3핀 헤더에 꽂습니다.
- Ground(검정)는 왼쪽, “-” 라벨이 붙은 쪽이어야 합니다.
- Signal(보통 흰색 또는 노란색)은 오른쪽(“Input” 쪽), “S” 라벨이 붙은 쪽이어야 합니다.
##



**전원**
Chainlink Driver의 ESP32와 3.3V 전자장치는 일반적으로 컴퓨터의 USB 연결로 전원을 공급받습니다. 모터용 12V 전원은 별도의 전원 공급 장치를 통해 공급됩니다.


> 참고: ESP32가 동작하지 않는 상태에서 12V 전원을 켜는 것은 피해야 합니다! ESP32가 동작하지 않으면 모터 코일이 “고정된 채” 켜질 수 있어 모터가 손상되거나 더 큰 문제가 발생할 수 있습니다.

**T-Display**

- Chainlink Driver를 1~2개 사용하여 최대 12개의 모듈을 구동할 때는 T-Display Buddy의 DC 12V 배럴 잭에 전원을 연결할 수 있습니다.
- ⚠️ Chainlink Driver가 2개를 초과한다면, 배럴 잭이 **충분한 전류를 감당할 수 없으므로**, 대신 첫 번째 Chainlink Driver의 Motor Power 터미널에 전원 공급 장치를 직접 연결해야 합니다.
[적절한 전선 굵기](../ElectronicsGuide.ko.md#power-supply-tips)를 사용하고 있는지 확인하고, [6개를 초과한 Chainlink Driver에 전원을 데이지체인으로 연결하지 마세요](../ElectronicsGuide.ko.md#large-displays).
https://www.dropbox.com/s/4xpvtycwrw21g0e/chainlinkBuddyWiringv1.1.pdf?dl=0


**Breadboard**

- 첫 번째 Chainlink Driver의 Motor Power 터미널에 전원 공급 장치를 직접 연결합니다. [적절한 전선 굵기](../ElectronicsGuide.ko.md#power-supply-tips)를 사용하고 있는지 확인하고, [6개를 초과한 Chainlink Driver에 전원을 데이지체인으로 연결하지 마세요](../ElectronicsGuide.ko.md#large-displays).


자세한 배선 정보는 전체 [Chainlink User Guide](../ElectronicsGuide.ko.md)를 참조하세요.


# 초기 설정 및 보정
- 12V 전원을 켜고 ESP32를 컴퓨터에 연결합니다.
- 모듈들이 홈 위치를 찾기 시작하는 모습이 보여야 합니다.
    - 어떤 모듈도 움직이지 않으면 ESP32를 다시 시작해 보세요. 그래도 움직이지 않으면 12V 전원을 끄고 [문제 해결 섹션](#troubleshooting)을 참조하세요.
- Chrome 또는 Edge에서(2024-10-05 기준 Firefox는 작동하지 않습니다) https://scottbez1.github.io/splitflap/ 에 접속하고 Web Serial로 디스플레이에 연결합니다.
- 어떤 모듈이 주황색 사각형으로 표시되면 먼저 모듈을 좌클릭하여 다시 호밍해 보세요. 모듈이 회전하며 홈 위치를 찾는 모습이 보여야 합니다. 그래도 센서 오류가 해결되지 않으면 [문제 해결 섹션](#troubleshooting)을 참조하세요.
- 모듈을 우클릭하여 보정 흐름을 열고, 안내에 따라 보정을 완료합니다. 다른 모듈 보정을 계속하기 전에 보정 결과를 저장하세요.
    - 보정 저장에 실패하면 [문제 해결 섹션](#troubleshooting)을 참조하세요.



https://www.dropbox.com/scl/fi/aqilx2zk5q8ic1kwi2ki7/PXL_20240330_182017129.TS.mp4?rlkey=im0qr2vuhdlxhmnnzx7f57r09&dl=0



# 문제 해결
- ESP32와 12V 전원을 켰을 때 모듈이 전혀 움직이지 않음
    - 문제 해결 단계:
        - VSCode에서 PlatformIO의 “Monitor” 액션을 실행한 뒤 ESP32의 리셋 버튼을 눌러 보세요. `{"type":"init", "num_modules":6}`과 같은 메시지가 보여야 하며, 루프백 오류 메시지가 보이지 않아야 합니다(`Loopback ERROR`가 보인다면 아래 섹션을 참조하세요).
        - 스크류 터미널이 해당 와이어에 단단히 고정되어 있는지 확인하세요.
        - 전압계로 각 Chainlink Driver 보드의 Motor와 GND 스크류 터미널 사이가 11~13V로 측정되는지 확인하세요.
- 모듈 보정 저장 실패
    - 증상: 보정 저장 시 `Failed to open config file` 또는 `Failed to mount FFat` 메시지가 나타남
    - 문제 해결 단계:
        - VSCode에서 PlatformIO 액션을 사용해 ESP32의 플래시를 지운 뒤, 펌웨어를 다시 업로드하고 보정을 재시도하세요.
- 잘못된 chainlink 데이터 신호 - `Loopback ERROR`
    - 증상: `Loopback ERROR` 로그 메시지. 이는 Chainlink Driver 보드 체인을 따라 모터로 가는 또는 센서로부터 오는 제어 신호가 동작하지 않음을 의미합니다.
    - 문제 해결 단계:
        - 모든 납땜 부위, 특히 IDC 커넥터의 납땜이 견고하고 단락되지 않았는지 확인하세요.
        - IDC 리본 케이블 커넥터가 리본 케이블에 완전히 고정되어 있는지 확인하세요.
        - 모든 스크류 터미널이 해당 와이어에 단단히 고정되어 있는지 확인하세요.
        - platformio.ini의 (`env:chainlink` 섹션 아래에 있는) NUM_MODULES 변수가 연결된 Chainlink Driver 수의 6배로 설정되어 있는지 확인하세요.
        - ESP32의 리셋 버튼을 누르고, 각 Chainlink Driver의 빨간 LED가 순차적으로 한 번씩 깜빡이는지 확인하세요.


여기서 다루지 않은 질문이 있다면 [splitflap Discord 서버](#troubleshootings)를 통해 문의해 주세요.



----------

링크 고지: Amazon Associate 자격으로 적격 구매에 대해 별도 비용 없이 수수료를 받습니다.
(제휴 링크 사용을 피하고 싶을 분들을 위해 모든 제휴 링크 옆에 비제휴 링크도 함께 제공하고 있습니다)

