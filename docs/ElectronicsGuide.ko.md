# Chainlink Driver 전자장치 사용자 가이드
[<< 문서 인덱스로 돌아가기](DocumentationIndex.ko.md)

# 소개

이제 막 시작하시는 분이고 Chainlink Driver에 대해 더 자세히 알고 싶으시다면, 추가 배경 및 일반 정보가 포함된 [이 문서의 하단](#chainlink-driver란-무엇입니까)으로 이동하시기 바랍니다.

이 안내를 개선할 수 있는 질문이나 제안이 있으시면 알려주십시오. 풀 리퀘스트를 자유롭게 열거나 [커뮤니티 Discord 서버](https://discord.gg/wgehm3PcrC)에 참여해 주세요.

split-flap 디스플레이를 만들고 계십니까? 진행 중이거나 완성된 프로젝트의 사진/영상을 받아보고 이야기 나누고 싶습니다! 이 프로젝트는 몇 년 동안 저의 취미였으며, 가장 멋진 부분은 단연 다른 분들이 직접 만들고 작동시키는 모습을 보는 것입니다. scott@bezeklabs.com 으로 자유롭게 메일을 보내주시거나 🙂, [Discord 서버에 참여](https://discord.gg/wgehm3PcrC)하셔서 더 넓은 split-flap 커뮤니티와 공유하고 토론해 주십시오!


# 1. 부품 준비
- Chainlink Driver PCB 어셈블리 (주문 정보는 [부록](#부록) 참조)
- 커넥터 (제가 Etsy에서 판매하는 Chainlink Driver 보드에는 모두 포함되어 있습니다)
    - JST XH 5핀 6개
    - 3핀 male 헤더 6개
    - 8핀 2열 슈라우드 IDC 커넥터 2개
- 와이어
    - 8핀 1.27mm 리본 케이블 및 양 끝의 IDC 커넥터 (제가 Etsy에서 판매하는 Chainlink Driver 보드에 포함됨)
    - 3.3v 전원 와이어
        - 예: 22AWG 단선 hookup wire
    - 12v 전원/접지 와이어
        - 모듈 개수에 따라 20AWG에서 14AWG까지
- 12V 전원 공급 장치 (자세한 정보는 [부록](#부록) 참조)
- ESP32
![Chainlink Buddy [T-Display]](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637360060741_DSC_5014_s.jpg)

    - [TTGO T-Display](https://amzn.to/3kHwhMm) [어필리에이트 링크는 추가 비용 없이 이 프로젝트를 지원하는 데 도움이 됩니다. 또는 원하시면 [비어필리에이트 링크](https://www.amazon.com/LILYGO-T-Display-Arduino-Development-CH9102F/dp/B099MPFJ9M)를 사용하셔도 됩니다]는 권장 ESP32 보드이며, 240x135 LCD가 포함되어 있어 splitflap 펌웨어가 기본적으로 지원합니다. ([aliexpress](https://www.aliexpress.com/item/33048962331.html)에서도 구입 가능하며, 더 저렴할 수 있습니다)
    - 대부분의 사용자에게는 선택 사항인 [Chainlink Buddy [T-Display]](https://bezeklabs.etsy.com/listing/1109357786/splitflap-chainlink-buddy-t-display)도 강력히 권장됩니다. 이는 T-Display를 Chainlink Driver에 쉽고 깔끔하게 연결할 수 있도록 해줍니다.
    - T-Display가 아닌 다른 ESP32 모듈을 사용하려는 경우, T-Display Buddy 대신 [Chainlink Buddy [Breadboard]](https://bezeklabs.etsy.com/listing/1123863267/splitflap-chainlink-buddy-breadboard)가 도움이 될 수 있습니다. 다른 ESP32 모듈 사용에 대한 자세한 정보는 [부록](#부록)을 참조하십시오.



# 2. PCB 조립 마무리
- 그림과 같이 커넥터를 삽입하고 납땜하십시오. 양쪽 끝에 있는 두 개의 IDC 커넥터는 모두 같은 방향(노치가 왼쪽을 향함)을 향해야 한다는 점에 유의하십시오.
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637363719721_chainlinkDrawing.png)

- 그림과 같이 리본 케이블을 커넥터에 삽입하고, 바이스나 펜치로 *부드럽게* 눌러 닫습니다. 반대쪽 끝의 다른 커넥터로도 반복하되, 두 커넥터가 **같은** 방향(노치가 왼쪽을 향함)을 향하도록 하십시오.
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637363943974_ChainlinkCableIDCAssembly.png)

- 권장하지는 않지만, 선택적으로 커넥터에 strain relief를 설치할 수 있습니다 (Bezek Labs Chainlink Driver 보드에 포함됨): 리본 케이블을 커넥터 위로 다시 접고 플라스틱 조각을 설치하여 딸깍 소리가 날 때까지 클램핑합니다. 케이블 길이가 일부 희생되고 부피가 더 크고 키가 큰 커넥터가 되므로, 어차피 케이블이 많이 움직이지 않을 것이기 때문에 그만한 가치가 있다고 생각하지 않습니다.


# 3. Chainlink Buddy 조립
- 커넥터를 제자리에 납땜하십시오 (PCB에 표시된 대로 IDC 커넥터 노치가 왼쪽을 향하도록 하십시오)


## T-Display Buddy
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637364807000_DSC_5003_s.jpg)
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637364821133_DSC_5014_s.jpg)


T-Display 자체에는 (상자에 포함된) male 헤더 2열을 T-Display에 납땜한 다음, 전체 모듈을 Buddy 보드에 납땜한 일치하는 female 헤더에 꽂습니다.

T-Display Buddy PCB의 왼쪽 아래에 C1 및 C2로 표시된 빈 공간과 3개의 관통 구멍이 있는 것을 알 수 있습니다. 걱정하지 마십시오. 이는 선택적 구성 요소이며 기본 설정에는 필요하지 않습니다. 자세한 내용은 [독립형 T-Display 작동](#8-선택사항-독립형-t-display-작동)을 참조하십시오.


![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1647556549613_PXL_20220317_223022886.jpg)


참고: T-Display에는 종종 작은 빨강/검정 와이어 하니스와 커넥터도 함께 제공됩니다. 이는 Chainlink Buddy와 함께 사용되지 않으므로 폐기해도 됩니다.






## Breadboard Buddy (T-Display Buddy의 대안)

다른 ESP32 모듈을 사용하고 싶으시다면, Breadboard Buddy PCB를 사용하여 IDC 케이블을 브레드보드에 쉽게 연결할 수 있습니다.

![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637364835081_DSC_5006.jpg)
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637364842028_DSC_5009_s.jpg)



# 4. Chainlink Driver를 Chainlink Buddy에 연결

먼저 전원 공급 장치나 모듈의 모터 또는 센서를 연결하지 않고 Chainlink Driver만 연결하고 테스트하는 것부터 시작하겠습니다. 기본 전자장치가 작동하는지 확인한 후 나중에 추가하겠습니다.


## T-Display
- Chainlink Buddy의 **Output**에서 Chainlink Driver의 **Input**으로 리본 케이블을 연결합니다
- Chainlink Driver의 “Logic 3.3-5V” 스크류 터미널에서 Chainlink Buddy의 “3.3V” 스크류 터미널로 와이어를 연결합니다
- Chainlink Driver의 “GND” 스크류 터미널에서 Chainlink Buddy의 “GND” 스크류 터미널로 와이어를 연결합니다
- Chainlink Driver의 “Motor 5-12v” 스크류 터미널에서 Chainlink Buddy의 “12V” 스크류 터미널로 와이어를 연결합니다
- ⚠️  Chainlink Buddy를 사용할 때는 절대 T-Display의 배터리 커넥터(TTGO T-Display 모듈 하단의 작은 흰색 커넥터)에 배터리를 연결하지 마십시오!
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637365064613_PXL_20211118_023418663.jpg)

## Breadboard (T-Display Buddy를 사용하지 않는 경우)
- Chainlink Buddy의 **Output**에서 Chainlink Driver의 **Input**으로 리본 케이블을 연결합니다
- Chainlink Driver의 “Logic 3.3-5V” 스크류 터미널에서 브레드보드의 3.3v 공급원으로 와이어를 연결합니다
- Chainlink Driver의 “GND” 스크류 터미널에서 브레드보드의 접지 레일로 와이어를 연결합니다
- 5개의 핀을 ESP32에 연결합니다. 자세한 내용은 [부록](#부록)을 참조하십시오. 기본 핀 할당은 다음과 같습니다:
    - Clock: 33
    - Motor Data: 32
    - Sensor Data: 39
    - Latch: 25
    - GND: ground
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637364110536_DSC_5010.jpg)



# 5. 펌웨어 설치

[**Microsoft Visual Studio Code**](https://code.visualstudio.com/) **를 다운로드하여 설치하십시오**

**Platform IO 확장을 설치하십시오**

**저장소를 복제하십시오**
VS Code 환영 페이지에서 "Clone Git Respository"를 선택한 다음 git 저장소 URL을 붙여넣습니다: `https://github.com/scottbez1/splitflap.git`


![](https://paper-attachments.dropboxusercontent.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1728232383342_Screenshot+from+2024-10-06+09-29-20.png)
![](https://paper-attachments.dropboxusercontent.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1728232480075_image.png)


메시지가 표시되면 복제된 저장소를 열기로 선택합니다.

Platform IO 확장이 실행되도록 폴더를 "Trust"로 설정해야 할 수도 있습니다.

![](https://paper-attachments.dropboxusercontent.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1728245389499_image.png)


platformio.ini의 NUM_MODULES를 연결한 Chainlink Drivers가 지원하는 모듈 수와 일치하도록 구성해야 합니다. 따라서 단일 Chainlink Driver의 경우 6으로 설정합니다.


    [env:chainlink]
    extends=esp32base
    build_flags =
        ${esp32base.build_flags}
        -DCHAINLINK
        -DNUM_MODULES=6


- (T-Display를 *사용하지 않는* 경우, 이 시점에서 추가로 변경해야 할 사항에 대해서는 [부록](#부록)을 참조하십시오)
- Mac 사용자: 최신 버전의 ESP32 T-Display에서 사용되는 CH9102 USB-시리얼 어댑터용 업데이트된 드라이버를 설치해야 할 가능성이 높습니다: https://learn.adafruit.com/how-to-install-drivers-for-wch-usb-to-serial-chips-ch9102f-ch9102/mac-driver-installation


VS Code에서 ESP32 T-Display로 코드를 업로드하려면 다음을 수행해야 합니다 (아래 스크린샷 참조):

> 1) Platform IO 사이드바를 엽니다 (왼쪽의 외계인 아이콘 클릭)
> 2) 창 하단의 "env" 버튼을 클릭한 다음 화면 상단의 드롭다운에서…
> 3) …환경으로 "env:chainlink"를 선택합니다 - 이렇게 하면 ESP32에 대한 코드 자동 완성 및 구문 강조가 설정됩니다
> 4) Platform IO 사이드바에서 "General" 섹션을 확장하고 `Upload and Monitor`를 클릭합니다
![](https://paper-attachments.dropboxusercontent.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1693886806926_image.png)

- ESP32를 재설정하면 Chainlink Drivers의 LED가 빠르게 깜박이고 시리얼 모니터에 loopback이 정상이라는 메시지가 표시되어야 합니다. loopback 오류 메시지가 표시되면 계속하기 전에 문제를 해결하십시오.

*참고*: 캘리브레이션을 시작하기 전에 터미널 창을 종료해야 합니다. 그렇지 않으면 두 창이 동시에 실행되어서는 안 되므로 오류가 발생할 수 있습니다.


# 6. 모듈 및 전원 연결
## 모터
- 흰색 커넥터에 꽂습니다. Chainlink Driver PCB가 모듈 *뒤에* 위치하도록 의도되었기 때문에 모듈 연결은 *오른쪽에서 왼쪽으로* 배치되어 있다는 점에 유의하십시오. 따라서 첫 번째 모듈은 PCB의 **오른쪽** 위치 "A"에 꽂힙니다
## 센서
![](https://paper-attachments.dropbox.com/s_0012998176B94D187A680336F96A7737F168EF4FF12A85A15DE924A7E7D3E44B_1627605534995_Screenshot+from+2021-07-29+17-38-43.png)

- 센서 케이블을 해당 3핀 헤더에 꽂습니다
- Ground (검정)는 왼쪽 ("Output" 측)에 있어야 하며 "-"로 표시되어 있습니다
- Signal (보통 흰색)은 오른쪽 ("Input" 측)에 있어야 하며 "S"로 표시되어 있습니다
##




## 전원

Chainlink Drivers의 ESP32 및 3.3v 전자장치는 일반적으로 컴퓨터에 대한 USB 연결로 전원이 공급됩니다. 모터용 12V 전원은 별도의 전원 공급 장치로 공급됩니다.


> 참고: ESP32가 실행 중이지 않을 때 12V 전원을 켜둔 채로 두지 마십시오! ESP32가 실행 중이지 않으면 모터 코일이 "고정 켜짐" 상태가 될 수 있어 모터를 손상시키거나 더 나쁜 결과를 초래할 수 있습니다.

**T-Display**

- 1개 또는 2개의 Chainlink Drivers를 사용할 때 DC 12v barrel jack을 T-Display Buddy에 꽂을 수 있습니다
- ⚠️ 2개를 초과하는 Chainlink Drivers의 경우 barrel jack이 충분한 전류를 처리할 수 없으므로, 대신 전원 공급 장치를 첫 번째 Chainlink Driver의 Motor Power 터미널에 직접 연결해야 합니다. [적절한 와이어 게이지](#전원-공급-장치-팁)를 사용하고 있는지 확인하고, [절대로 6개를 초과하는 Chainlink Drivers에 전원을 체인 연결하지 마십시오](#대형-디스플레이)

[배선 다이어그램](img/chainlinkWiringv1.1.pdf)


**Breadboard**

- 전원 공급 장치를 첫 번째 Chainlink Driver의 Motor Power 터미널에 직접 연결합니다. [적절한 와이어 게이지](#전원-공급-장치-팁)를 사용하고 있는지 확인하고, [절대로 6개를 초과하는 Chainlink Drivers에 전원을 체인 연결하지 마십시오](#대형-디스플레이)


[배선 다이어그램](img/chainlinkWiringv1.1.pdf)



# 7. (선택사항) 추가 Driver 추가

리본 케이블을 연결하고 두 번째 전원 스크류 터미널 세트(3.3v, ground 및 12v 전원에 대해 각각 2개의 터미널이 있음)를 사용하여 추가 전원 와이어를 추가하면 여러 Chainlink Drivers를 쉽게 체인 연결할 수 있지만, 다음 규칙을 반드시 따라야 합니다:


    ⚠️ 절대로 6개를 초과하는 Chainlink Drivers에 연속해서 전원을 체인 연결하지 마십시오 ⚠️

스크류 터미널은 제한된 전류 정격(Bezek Labs에서 판매하는 것은 10A)이 있으므로, **6개를 초과하는 Chainlink Drivers를 사용하려면 전원을 다르게 배선해야 합니다**. 대형 디스플레이 배선에 대한 자세한 내용은 아래의 [+Chainlink Driver v1.1 전자장치 사용자 가이드: 대형 디스플레이](#대형-디스플레이)를 참조하십시오.


# 8. (선택사항) 독립형 T-Display 작동

일반적인 구성에서는 12V 공급으로 모터에 전원을 공급하고, 별도로 T-Display는 컴퓨터에 대한 5V USB 연결을 통해 전원이 공급됩니다.

그러나 USB 연결을 생략하고 12V 모터 공급으로 전원을 공급받는 완전 독립형 설정도 가능합니다. 이는 T-Display의 WiFi 기능을 사용하여 예를 들어 HTTP(s) API를 폴링하거나 MQTT 토픽을 수신할 때 잘 작동합니다.

이를 위해서는 Chainlink Buddy [T-Display]에 3개의 구성 요소를 추가해야 합니다 (별도 구매 필요):

- 5V 스위칭 레귤레이터
    - [Mornsun K7805-500R3](https://www.digikey.com/en/products/detail/mornsun-america-llc/K7805-500R3/13168189)는 권장 옵션 중 하나이지만, 7805 폼 팩터로 500mA+ 정격의 모든 **스위칭** 레귤레이터 모듈이 작동해야 합니다 - 데이터시트에서 입력(C1) 및 출력(C2)에 대한 커패시터 요구 사항을 다시 확인하십시오. 클래식 7805 선형 레귤레이터는 권장되지 않습니다.
- 22uF 1206 세라믹 커패시터 - 16V - C2에 설치
    - 예: [CL31A226MOCLNNC](http://)
- 10uF 1206 세라믹 커패시터 - 50V - C1에 설치
    - 예: [CL31A106MBHNNNE](https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL31A106MBHNNNE/5961220)
    - 또는 22uF 커패시터 2개를 구입하여 C1과 C2 모두에 사용하되, 25V+ 정격으로 선택해야 합니다. 예: [CL31A226KAHNNNE](https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL31A226KAHNNNE/3888705)
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1639184673383_2021-12-10+16.26.37.jpg)
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1639184679625_2021-12-10+16.28.06.jpg)

----------
# 부록
## Chainlink Driver란 무엇입니까?
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637357775368_DSC_4991_s.jpg)


Chainlink Driver는 Classic Controller에서 얻은 교훈을 바탕으로 한 splitflap 디스플레이용 업데이트된 컨트롤 보드입니다.

이를 설계하는 데에는 두 가지 주요 목표가 있었습니다:

- *많은* 수의 splitflap 제어 지원
- 저비용 및 사전 조립된 보드 구매의 용이성 - 관통 구멍 방식이 아닌 대부분 SMD 방식

각 Chainlink Driver PCBA에는 stepper 모터를 구동하고 **최대 6개** 모듈의 home position 센서를 읽기 위한 모든 전원 및 신호 전자장치가 포함되어 있으며, 사소하게 체인으로 연결하여 ESP32의 4개 핀만 사용하여 100개 이상의 splitflap 모듈을 제어할 수 있습니다.


https://www.youtube.com/watch?v=g9EPabcxBsM&



## Chainlink Driver는 어디서 구입합니까?
![](https://paper-attachments.dropbox.com/s_BBABC117AF455DD9F0525297940CD25AF9A358008ED7FF73463824486BCF5E62_1637358766420_DSC_4994_s.jpg)


이 디자인은 오픈 소스이므로 제공된 디자인 파일을 사용하여 PCB 제조업체로부터 직접 주문할 수 있지만, 미국 내에서는 [Bezek Labs Etsy 스토어에서도 판매](https://bezeklabs.etsy.com/listing/1123280069/splitflap-chainlink-driver-v11)하고 있습니다.

제 스토어에서 구매하는 것의 장점은 [조립 후 맞춤 테스트 베드를 사용하여 100% 기능 테스트가 이루어지며](https://twitter.com/scottbez1/status/1414986069586575360), 이 프로젝트의 추가 개발 및 프로토타이핑을 지원하는 데 도움이 됩니다. 또한 편의를 위해 모든 커넥터와 리본 케이블을 포함하고 있습니다.

PCB 제조업체로부터 직접 주문하고 싶으시다면, 디자인은 JLCPCB의 어셈블리 서비스에 최적화되어 있습니다 (스폰서십이나 제휴 관계는 없지만, 그들의 부품 라이브러리에서 제공되는 제한된 부품 세트를 고수하는 한 매우 저렴한 어셈블리를 제공합니다). BOM에는 많은 커넥터가 *포함되지 않은* 점을 유의하십시오. 고유 부품당 $3 수수료가 있고, 어차피 리본 케이블을 별도로 주문해야 하기 때문에 소량 주문 시 비용을 더 낮게 유지할 수 있습니다.


## 전원 공급 장치 팁

제어할 모듈의 수에 따라 (그리고 모든 28BYJ-48 모터가 동일한 코일 저항을 갖는 것은 아니므로 사용하는 특정 모터에 따라) 결정되는 전류 정격을 가진 12V 공급 장치가 필요합니다.

좋은 시작 가정은 각 모터가 0.25A씩 끌어온다는 것입니다 (100옴 half-winding 저항을 가진 모터에 대한 일반적인 추정치). 그러나 항상 모터를 테스트하고 안전 마진을 포함시켜야 합니다.

따라서 사용하는 각 Chainlink Driver당 최소 1.5A 용량을 계획해야 하지만, 많은 저렴한 전원 공급 장치는 의심스럽거나 과장된 정격을 가지고 있으므로 최소 2A는 원하실 것입니다.

대형 디스플레이의 경우, [Mean Well LRS-350-12](https://amzn.to/3cdjuwD) [어필리에이트 링크는 추가 비용 없이 이 프로젝트를 지원하는 데 도움이 됩니다. 또는 원하시면 [비어필리에이트 링크](https://www.amazon.com/MEAN-WELL-LRS-350-12-Computer-Project/dp/B07VTLJS18)를 사용하셔도 됩니다]를 사용했으며, 매우 적은 전압 리플로 22A 이상을 쉽게 공급한다는 것을 발견했습니다.

전원용으로 적절한 게이지의 구리 와이어를 선택해야 합니다 (이는 GND 와이어도 포함합니다!). Chainlink Driver 보드 체인을 따라 흐르는 전류는 빠르게 누적됩니다!

특히 대형 디스플레이의 경우 추가 보호 계층으로 전원 공급 장치 근처에 퓨즈를 추가하는 것을 권장합니다. 위에서 언급한 LRS-350-12는 *연속적으로* 29A를 공급할 수 있으며, 이는 결함 발생 시 잠재적으로 파괴적일 수 있는 많은 전류입니다. 각 전원 분기(고급 배선 다이어그램 참조)는 이보다 적게 사용하므로, 각 분기를 적절한 크기의 자체 퓨즈로 보호해야 합니다.

평판이 좋고 신뢰할 수 있는 공급망을 가진 판매자(예: AliExpress나 Amazon이 아닌 전자 부품 공급업체나 대형 철물점)로부터 전원 배선을 구입하시기 바랍니다.
불행히도, 구리 가격이 상승함에 따라 [광고된 사양을 충족하지 않을 수 있는 다른 금속을 사용하는 와이어를 발견하는 경우가 더 일반적이 되었습니다](https://www.youtube.com/watch?v=15sMogK3vTI).


## 다른 ESP32 모듈 사용

이론적으로 *2개의 코어를 가진* ESP32 모듈(즉, ESP32-**S2** 기반이 *아닌*)이라면 작동해야 합니다. 가장 일반적인 WROOM 또는 WROVER 기반 모듈이 작동할 수 있습니다.

그러나 모든 저렴한 모듈이 잘 설계된 것은 아니므로(브레드보드 친화적이지 않은 것, WiFi/ble 동안 brownout을 일으키는 부실한 전원 설계 등), T-Display가 훌륭한 기본값임을 발견했습니다. LCD에 몇 개의 IO 핀을 잃지만, Chainlink 펌웨어는 LCD를 기본적으로 지원하며 디버깅에 유용하다는 것을 알게 되실 것입니다.

그렇긴 하지만, 다른 모듈을 사용하는 경우 알아야 할 사항은 다음과 같습니다:


1. 해당 핀을 해제하고 CPU 사이클 낭비를 피하기 위해 디스플레이 코드를 비활성화하고 싶을 것입니다. platformio.ini에서 `-DENABLE_DISPLAY=1`을 `-DENABLE_DISPLAY=0`으로 변경하여 이를 수행하십시오
2. ESP32에는 GPIO 매트릭스가 있으므로 핀 할당을 쉽게 변경할 수 있지만(spi_io_config.h 참조), [특정 예약된 기능을 피해야](https://www.youtube.com/watch?v=LY-1DHTxRAk) 하므로 그렇게 하지 않을 충분한 이유가 없는 한 기본값을 사용하는 것을 권장합니다.


## 대형 디스플레이

Chainlink 시스템은 대형 디스플레이를 지원할 수 있지만, 디스플레이의 크기가 (그리고 따라서 관련된 전원 공급 장치 및 전자장치가) 증가함에 따라 더 많은 주의가 필요하다는 점을 인지하시기 바랍니다.

6개 이상의 Chainlink Driver 보드를 배선하는 경우, **데이터 연결만 연속적인 체인을 형성해야 합니다**! 이는 아래 다이어그램에 파란색으로 표시되어 있습니다.

전원은 **최대 6개의 Drivers로 구성된 별도의 체인으로 분기**되어야 합니다 (모터에 더 많은 전류가 필요한 경우 더 적게).

데이터처럼 전원을 연속적으로 체인 연결하면 체인 시작 부분의 스크류 터미널과 와이어에 과부하가 걸려 손상/화재를 일으킬 수 있습니다. 아래 다이어그램에서 노란색과 검정색 와이어가 *전원 공급 장치에서* 분기되어 6개 Drivers의 각 하위 체인을 넘어 계속되지 않는 방식에 유의하십시오.

[고급 배선 다이어그램](img/chainlinkWiringAdvanced.pdf)

이 크기의 디스플레이의 경우, 관련된 총 전력을 고려할 때 추가 안전 조치를 추가할 것을 강력히 권장합니다. 예를 들어:

- 각 전원 분기에 대한 퓨즈
- 실시간 전압 및 전류 모니터링, 그리고 결함을 감지하고 대응하기 위한 각 "분기"용 개별 부하 스위치
- 12V 전원 공급 장치로의 mains 입력을 제어하는 릴레이 (12V 분기 부하 스위치와 의도적으로 중복)

Chainlink Base (시스템에서 Chainlink Buddy를 대체)는 이러한 조치 중 일부에 대한 한 가지 가능한 접근 방식이지만, 공식적으로 지원/권장되지는 않습니다.

자격을 갖춘 전기 기술자/엔지니어와 상담하여 모든 디자인(splitflap 프로젝트 회로도 및 PCB 포함)을 검토하시고, 해당 규제 코드를 반드시 따르도록 하십시오.




----------

링크 공개: Amazon Associate로서 자격을 갖춘 구매로부터 수익을 얻습니다.
(어필리에이트 링크 사용을 피하고 싶으신 경우를 위해 모든 어필리에이트 링크 옆에 비어필리에이트 링크도 포함하기로 결정했습니다)

