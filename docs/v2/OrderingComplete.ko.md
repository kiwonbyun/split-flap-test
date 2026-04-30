# Splitflap v2 종합 주문 가이드
[<< 문서 인덱스로 돌아가기](../DocumentationIndex.ko.md)

아래 안내는 최신 Chainlink 전자 부품을 사용하여 **6개 모듈**로 구성된 splitflap v2 디스플레이를 제작하는 데 필요한 모든 부품(일반 공구 제외)을 주문하는 과정을 안내합니다.

조립할 준비가 되셨나요? [조립 가이드](Assembly.ko.md)로 바로 이동하세요.

질문이 있으시면 언제든지 저(scott@bezeklabs.com)에게 연락해 주세요. 또는 [Discord 서버](https://discord.gg/wgehm3PcrC)에 참여하여 split-flap 커뮤니티와 토론하거나 질문해 보세요!


😩 이 문서가 부담스럽게 느껴지시나요? 충분히 그럴 만합니다, 정말 많은 내용이 담겨 있으니까요… 그래서 미국에 계신 분들을 위해 포괄성/최저 비용보다는 단순함을 우선시한 훨씬 더 짧은 문서를 준비했습니다: [+Splitflap 주문 (“쉬운” 경로)](OrderingEasy.ko.md)


1. [레이저 컷 부품 주문](#레이저-컷-부품-주문)
3. [전자 부품 주문](#전자-부품-주문)
2. [기타 하드웨어 주문](#기타-하드웨어-주문)

----------
# 레이저 컷 부품 주문

레이저 컷 부품을 주문할 수 있는 곳은 많지만, 저는 미국으로 배송되는 간편한 온라인 전용 프로세스를 제공하는 Ponoko와 Elecrow를 직접 사용해 보았습니다. 이전에는 Ponoko를 추천드렸으며, 여전히 품질과 고객 서비스가 훌륭하여 좋은 제품을 받으실 수 있다고 생각합니다. 다만 가격이 너무 비싸져서 더 이상 기본 추천으로는 권하기 어렵게 되었습니다 😞

상급자 메이커를 위한 안내: 모듈 한 행(또는 그리드) 전체가 공유할 단일 전면 패널을 절단하고 싶다면, 간격, 행/열과 같은 다양한 구성 옵션을 제공하는 스크립트가 있습니다. 심지어 내부 모서리에 필요한 “도그본(dog-bones)”이 적용된 CNC 라우팅용 지오메트리를 생성하는 모드도 있습니다. `generate_combined_front_panel.py`를 참고하세요.

💡 참고: v2 레이저 컷 부품은 이전 v0 모듈과 치수가 호환되지 않습니다! 기존 디스플레이를 확장하시는 경우 이전 파일을 사용하셔야 합니다 (v0 [주문 안내](../v0/OrderingComplete.ko.md) 참조).


## Elecrow (추천)

- 적절한 파일을 다운로드하세요:
  - 52-flap 디자인
    - 3mm 아크릴
      - [zip](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-elecrow-3mm-acrylic_1x.zip) 다운로드
      - [Elecrow 아크릴 레이저 커팅](https://www.elecrow.com/acrylic-cutting.html)으로 이동하여 zip 파일 업로드
      - 치수 입력: <img height="18" src="https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-elecrow-3mm-acrylic_1x_dimensions.svg" />
      - 두께 선택: 3mm
      - 인그레이브: No
      - 아크릴 색상: Matte Black (P502) 권장
    - 3mm 목재
      - [zip](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-elecrow-3mm-wood_1x.zip) 다운로드
      - [Elecrow 목재 레이저 커팅](https://www.elecrow.com/5pcs-wood-laser-cutting-service.html)으로 이동
      - 치수: 20cm Max * 20cm Max (두께: 3mm)
  - 40-flap 디자인
    - 3mm 아크릴
      - [zip](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-40-elecrow-3mm-acrylic_1x.zip) 다운로드
      - [Elecrow 아크릴 레이저 커팅](https://www.elecrow.com/acrylic-cutting.html)으로 이동하여 zip 파일 업로드
      - 치수 입력: <img height="18" src="https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-40-elecrow-3mm-acrylic_1x_dimensions.svg" />
      - 두께 선택: 3mm
      - 인그레이브: No
      - 아크릴 색상: Matte Black (P502) 권장
    - 3mm 목재
      - [zip](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-40-elecrow-3mm-wood_1x.zip) 다운로드
      - [Elecrow 목재 레이저 커팅](https://www.elecrow.com/5pcs-wood-laser-cutting-service.html)으로 이동
      - 치수: 20cm Max * 20cm Max (두께: 3mm)

![](img/elecrow_acrylic.png)
![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1592618387746_Screenshot+from+2020-06-19+18-59-27.png)

## Ponoko (추천하지만 가격이 비쌈)
- 적절한 파일을 다운로드하세요
    - 52-flap 디자인
        - 3mm 아크릴: [svg](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-ponoko-3mm-acrylic_1x.svg) <img height="18" src="https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-ponoko-3mm-acrylic_1x_dimensions.svg" />
        - 3mm MDF: [svg](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-ponoko-3mm-mdf_1x.svg) <img height="18" src="https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-ponoko-3mm-mdf_1x_dimensions.svg" />
    - 40-flap 디자인
        - 3mm 아크릴: [svg](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-40-ponoko-3mm-acrylic_1x.svg) <img height="18" src="https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-40-ponoko-3mm-acrylic_1x_dimensions.svg" />
        - 3mm MDF: [svg](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-40-ponoko-3mm-mdf_1x.svg) <img height="18" src="https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-40-ponoko-3mm-mdf_1x_dimensions.svg" />


- [Ponoko](https://www.ponoko.com/)로 이동하여 계정에 가입하세요.
- 위에서 다운로드한 SVG 파일을 [업로드](https://www.ponoko.com/designs)하세요. 치수가 위의 값과 일치하는지 확인하고, 파란색 선이 “Cutting”으로 설정되어 있고 검정색 채우기가 “Area Engraving”으로 설정되어 있는지 확인하세요 (또는 인그레이브된 기능을 건너뛰려면 이 옵션을 끄세요).
![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1590128918128_Screenshot+from+2020-05-21+23-28-11.png)

- 재료를 선택하세요. [MDF](https://www.ponoko.com/materials/mdf-fiberboard)나 [아크릴](https://www.ponoko.com/materials/black-matte-acrylic)을 추천드리며, 3.0mm (0.12 inches) 두께를 선택하세요. 위의 파일 링크 옆에 제공된 치수와 재료의 최대 크기를 비교하여 확인하세요. 일부 재료는 너무 작아서 4x 버전을 주문할 수 없을 수도 있습니다.

💡 **Ponoko에서 Matte 1-Side 아크릴을 주문하실 때 중요한 참고사항:** 주문을 한 직후 Ponoko에 ***반드시*** 특별 지시사항을 보내어 *광택(glossy)* 면에 디자인을 인그레이브해 달라고 요청해야 합니다. 그래야 디자인이 올바르게 절단되어 조립 시 매트면이 디스플레이의 외부에 오게 됩니다. Ponoko 지원팀의 안내 (2021-05-13 기준):

> 매트 [기본값] 절단은 매트면을 위로 향하게 하여 절단됩니다 (따라서 인그레이빙도 이 면에 진행됩니다).
>
> 광택면에 인그레이빙하기를 원하시면, **주문 확인 페이지에 답글**로 요청을 남겨 주시면 주문 세부 정보에 메모하도록 하겠습니다.

----------
# 전자 부품 주문

Chainlink 시스템은 더 강력한 ESP32 마이크로컨트롤러(wifi 지원과 같은 기능을 추가함)를 기반으로 하는 새로운 전자 시스템이며, 이전 Classic Controller에서 얻은 학습 내용을 통합한 것입니다. 새로운 개발은 Chainlink 시스템에 집중되고 있습니다.

Chainlink 시스템에 필요한 기본 부품:

- **Chainlink Driver 보드** (제어하려는 split-flap 모듈 6개당 1개)
- **Chainlink Buddy** + **ESP32** (디스플레이 크기에 관계없이 전체 디스플레이당 1개)
- **Sensors** (split-flap 모듈당 1개)

가장 쉽고 가장 잘 지원되는 방법은 Bezek Labs Etsy 스토어(미국 한정)에서 각 항목을 구매하는 것입니다. 각 항목이 필요한 액세서리와 함께 제공되도록 스토어를 설정해 두었기 때문에, 다른 공급업체에서 따로 찾아 구매해야 할 항목이 줄어듭니다. 수익금은 또한 프로젝트의 지속적인 개발 자금으로 사용됩니다!

💡 다양한 구성에 대한 자세한 정보는 [Chainlink 사용자 가이드](../ElectronicsGuide.ko.md)를 참조하세요.

## Chainlink Driver 주문
![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639441358230_DSC_4991_s.jpg)


Chainlink Driver는 최대 6개의 split-flap 모듈을 구동하는 부품입니다. 여러 개의 Chainlink Driver를 체인처럼 연결하여 (그래서 이름이 그렇습니다!) 훨씬 더 큰 디스플레이를 만들 수 있습니다 (저는 18개의 Chainlink Driver 보드를 사용하여 108-모듈 디스플레이를 만든 적이 있습니다).

Chainlink Driver는 대부분 표면 실장(SMD) 부품을 사용하므로 손납땜보다는 공장 생산에 더 최적화되어 있습니다 (물론 원하시면 직접 손납땜하실 수도 있습니다).

[**추천] 옵션 1: Etsy에서 완전히 테스트된 PCBA 구매 (미국 배송만 가능)**
저는 [Bezek Labs Etsy 스토어에서 대부분 사전 조립된 Chainlink Driver 보드](https://bezeklabs.etsy.com/listing/1123280069/splitflap-chainlink-driver-v11)를 판매합니다 (액세서리 포함: 커넥터, 리본 케이블).

이 보드들에는 까다로운 표면 실장 부품들이 모두 미리 납땜되어 있습니다. 비교적 쉬운 스루홀 커넥터만 직접 납땜하시면 됩니다.

제가 판매하는 모든 보드는 제가 직접 개발한 맞춤형 테스트 지그를 사용하여, 모든 모터 출력, 센서 입력, LED, 데이터 라인이 예상대로 작동하는지 검증하는 100% 엄격한 기능 테스트를 거칩니다.

이 옵션에는 또한 필요한 모든 커넥터와 리본 케이블이 포함되어 있어 별도로 주문하실 필요가 없습니다!

그리고 AliExpress에서 주문하고 운에 맡기는 대신 올바른 28byj-48 모터를 받고 싶으시다면, Chainlink Driver 주문 시 6x 모터를 포함하는 옵션을 Etsy에 추가해 두었습니다! 네, AliExpress에서 직접 주문하는 것보다 비싸지만 빠르게 배송되며 좋은 모터를 받으실 수 있다는 것을 보장합니다.

**옵션 2: JLCPCB에서 조립된 Chainlink Driver를 구매하고, 커넥터와 리본 케이블은 별도로 구매**
Chainlink Driver 디자인은 JLCPCB 조립에 최적화되어 있어 대부분 드래그 앤 드롭 프로세스이지만, 선택하는 옵션을 신중하게 이해하셔야 합니다. 가장 중요한 것은, JLCPCB에서 부품 재고가 없는 경우 *해당 부품을 단순히 누락한 채로 주문을 계속 진행한다는 것입니다!* 따라서 주문 시 표시되는 모든 경고나 알림을 주의 깊게 확인하세요.

JLCPCB 조립에는 여러 가지 고정 비용 (예: 고유 부품당 $3, 배송비 등)이 포함되므로 수량이 많을수록 더 좋은 가치를 얻을 수 있습니다.

최신 Chainlink Driver 릴리스(v1.1)에서 다음 3개 항목을 다운로드하세요:

- gerber 파일 (PCB용)
- BOM (조립에 필요한 부품을 명시)
- CPL (부품의 배치 위치를 명시)

주문하기:

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444226661_image.png)

- JLCPCB https://cart.jlcpcb.com/quote 로 이동
- gerber zip 업로드
- 수량과 PCB 색상 선택
- 다른 매개변수 확인:
    - 치수: (자동 생성된 치수 수락, 아마도 30.48 x 198.12)
    - PCB 두께: 1.6
    - 외부 동박 두께: 1oz




![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444258704_image.png)

- SMT Assembly 선택
    - 윗면 조립
    - 조립할 수량 선택
    - Tooling holes: **Added by Customer** 선택 (디자인에 이미 포함되어 있으므로 JLC가 추가할 필요 없음)
    - 확인




![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444326379_image.png)

- BOM 파일 업로드
- CPL (csv) 파일 업로드






![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444544494_image.png)

- 부품 검토
    - ⚠️ 재고가 없는 부품은 그냥 누락되므로 이 단계를 신중하게 확인하세요! ⚠️
    - “No part selected”는 JLCPCB에서 조립하지 않을 여러 커넥터에 대해 *정상*입니다 (아래 참조). 이는 “Motor A”, “Sensor C”, “Input” 또는 “Output”과 같은 “J”로 시작하는 지정자입니다.


- 부품 배치 검토
- 장바구니에 저장
- 결제 (참고: JLC는 결제를 완료하기 전까지 부품을 예약하지 않으므로, 재고가 적을 때 결제를 미루면 부품이 누락될 가능성이 있습니다!)

JLCPCB가 조립하는 대신 일부 스루홀 커넥터를 직접 손으로 조립하고 싶으시다면, 주문 시 해당 부품의 선택을 해제한 다음 직접 주문하여 조립할 수 있습니다:

- 2x IDC shrouded 커넥터, 2x4, 2.54mm 간격, 예: JLC/LCSC [C601937](https://lcsc.com/product-detail/IDC-Connectors_JILN-321008SG0ABK00A01_C601937.html), 또는 [Digi-Key](https://www.digikey.com/en/products/detail/adam-tech/BHR-08-VUA/9832409)
- 6x JST XH 5 pin 커넥터, 예: JLC/LCSC [C161872](https://lcsc.com/product-detail/Wire-To-Board-Wire-To-Wire-Connector_JST-Sales-America-B5B-XH-AM-LF-SN_C161872.html), 또는 [C378947](https://lcsc.com/product-detail/Wire-To-Board-Wire-To-Wire-Connector_JST-Sales-America-B5B-XH-A-BK-LF-SN_C378947.html), 또는 LCSC [C157991](https://lcsc.com/product-detail/Wire-To-Board-Wire-To-Wire-Connector_JST-Sales-America-B5B-XH-A-LF-SN_C157991.html), 또는 [Digi-Key](https://www.digikey.com/en/products/detail/jst-sales-america-inc/B5B-XH-AM-LF-SN/1651037)
- 6x 3-pin male headers, 2.54mm 간격, 예: JLC/LCSC [C49257](http://), 또는 Digi-Key [3-pin](https://www.digikey.com/en/products/detail/sullins-connector-solutions/PREC003SAAN-RC/2774851) 또는 [40-pin](https://www.digikey.com/en/products/detail/sullins-connector-solutions/PREC040SAAN-RC/2774814)을 구매하여 분리하기 (또는 Amazon 등에서 대량으로 쉽게 구할 수 있음)

Chainlink Driver를 마이크로컨트롤러에 (또는 체인의 다른 Chainlink Driver에) 연결하려면 IDC 리본 케이블 + 커넥터도 필요합니다:

- 1x 8 컨덕터 1.27mm 간격 리본 케이블 (체이닝의 경우 최소 45cm 길이 권장), [예: Digi-Key](https://www.digikey.com/en/products/detail/w%C3%BCrth-elektronik/63910815521CAB/8324550)
- 2x IDC 케이블 커넥터, 예: LCSC [C601910](https://lcsc.com/product-detail/IDC-Connectors_JILN-531408YBS0BW01_C601910.html), 또는 [Digi-Key](https://www.digikey.com/en/products/detail/adam-tech/FCS-08-SG/9832361)
- 또는 Amazon 등에서 조립된 8P IDC 케이블을 찾을 수도 있지만, 스트레이트 스루(즉, 커넥터의 노치가 같은 방향을 향하는) 케이블인지 확인하세요.

주문 후 JLCPCB로부터 스크류 터미널의 방향을 다시 확인해 달라는 이메일을 받을 수도 있습니다. 올바른 방향에 대해서는 아래 이미지를 참조하세요: 와이어가 PCB의 Power 라벨 *위*로 지나가서 스크류 터미널의 앞쪽으로 삽입되어야 합니다.

![✅ 올바른 스크류 터미널 방향의 디자인 3D 모델](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639550660519_image.png)
![✅ JLCPCB의 확인 이메일, 올바른 스크류 터미널 방향을 보여줍니다. 이렇게 보이는 이미지가 오면 그대로 확인하세요!](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639550557063_image.png)
![🚫 잘못됨: 이렇게 보이면 방향이 잘못된 것입니다!](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639551191137_chainlinkBadScrewTerminalOrientation.png)


**옵션 3: 빈 PCB와 부품을 구매하여 직접 손으로 조립**
이는 표면 실장 부품을 손납땜해야 하는 고급 옵션입니다. 부품이 아주 작지는 않지만 (IC는 SOIC 패키지이고 수동 부품은 0603), 어느 정도의 기술과 인내심이 필요합니다.

스텐실을 주문하고 부품을 직접 리플로우 솔더링하는 것도 고려해 볼 수 있습니다. 다만 PCB가 길고 얇기 때문에 가열될 때 휘어지기 쉬우므로, 오븐 대신 핫 플레이트를 사용할 계획이라면 어려움이 있을 수 있다는 점을 유의하세요.

PCB 주문은 위의 옵션 2 지침을 따르되, 조립을 선택하는 대신 BOM 파일을 사용하여 모든 부품을 직접 주문할 수 있습니다. BOM 파일은 LCSC 부품 번호를 사용합니다.


## Chainlink Buddy와 ESP32 주문

ESP32 마이크로컨트롤러를 체인의 첫 번째 Chainlink Driver에 연결하게 됩니다. 이를 위한 가장 좋은 방법은 IDC/리본 케이블을 직접 꽂을 수 있는 사용 가능한 Chainlink “Buddy” 보드 중 하나를 사용하는 것입니다.

다양한 ESP32 모듈이 존재하며, 대부분은 호환되어야 하지만 (듀얼 코어인 한), 저는 TTGO T-Display를 강력히 추천드립니다 ([Amazon](https://amzn.to/3kHwhMm)에서 빠른 배송 [제휴 링크는 추가 비용 없이 이 프로젝트를 지원하는 데 도움이 됩니다. 원치 않으시면 [비제휴 링크](https://www.amazon.com/LILYGO-T-Display-Arduino-Development-CH9102F/dp/B099MPFJ9M)를 사용하세요], 또는 기다리는 것이 괜찮으시면 [AliExpress](http://)). 여기에는 splitflap 펌웨어가 기본적으로 지원하는 240x135 LCD가 포함되어 있어 디버깅에 매우 유용합니다.

**Chainlink Buddy [T-Display]**

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639445752808_DSC_5014_s.jpg)


Chainlink Buddy [T-Display]는 대부분의 사람들에게 권장되는 방법이며, 리본 케이블 커넥터, 전원용 스크류 터미널, 그리고 편리한 12v 전원 입력을 위한 배럴 잭을 갖추고 있어 TTGO T-Display 마이크로컨트롤러를 Chainlink 시스템에 매우 쉽게 연결할 수 있습니다.



[추천] [Bezek Labs Etsy 스토어 (미국 한정)](https://bezeklabs.etsy.com/listing/1109357786/splitflap-chainlink-buddy-t-display)에서 구매 가능 (액세서리 포함: IDC 커넥터, 스크류 터미널, 배럴 잭, 암 헤더).
또한 올바른 부품을 받기 위해 T-Display ESP32 모듈을 함께 포함하는 옵션도 있습니다.


또는 gerber를 사용하여 PCB를 직접 주문할 수 있으며, 이 경우 함께 사용할 다음 항목들도 주문해야 합니다:

- 1x IDC shrouded 커넥터, 2x4, 2.54mm 간격, 예: LCSC [C601937](https://lcsc.com/product-detail/IDC-Connectors_JILN-321008SG0ABK00A01_C601937.html)
- 1x 3-pin 5.08mm 간격 스크류 터미널, 예: LCSC [C72334](https://lcsc.com/product-detail/Screw-terminal_Ningbo-Kangnex-Elec-WJ500V-5-08-3P_C72334.html)
- 1x 2.1mm 배럴 잭, 예: LCSC [C381116](https://lcsc.com/product-detail/AC-DC-Power-Connectors_XKB-Connectivity-DC-005-5A-2-0_C381116.html)
- 2x 12-pin 2.54mm 간격 암 헤더, 예: LCSC [C350303](https://lcsc.com/product-detail/Female-Headers_HOAUC-2685Y-112CNG1SNA01_C350303.html)




**Chainlink Buddy [Breadboard] (T-Display Buddy의 대안)**

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639446207182_DSC_5009_s.jpg)


T-Display 외의 다른 ESP32 모듈을 사용하고 싶으시다면, Breadboard Buddy는 프로토타이핑을 위해 Chainlink 리본 케이블을 브레드보드에 깔끔하게 연결하는 간단한 방법의 대안입니다. 일반적으로 권장되지는 않지만 고급 사용자를 위해 제공됩니다.




[Bezek Labs Etsy 스토어 (미국 한정)](https://bezeklabs.etsy.com/listing/1123863267/splitflap-chainlink-buddy-breadboard)에서 구매 가능 (액세서리 포함: IDC 커넥터, 수 핀 헤더)

또는 gerber를 사용하여 PCB를 직접 주문할 수 있으며, 이 경우 함께 사용할 다음 항목들도 주문해야 합니다:

- 1x IDC shrouded 커넥터, 2x4, 2.54mm 간격, 예: LCSC [C601937](https://lcsc.com/product-detail/IDC-Connectors_JILN-321008SG0ABK00A01_C601937.html)
- 1x 5-pin 2.54mm 간격 수 핀 헤더


## Sensors 주문

각 split-flap 모듈은 홈 위치를 감지하기 위해 Hall sensor가 필요합니다. 이를 장착하는 가장 좋은 방법은 작은 센서 PCB를 사용하는 것입니다.

[**추천] 옵션 1: Etsy에서 Sensor kit v2 (미국 한정)**
일을 단순하게 만들기 위해, 이 키트에는 센서 6개를 조립하는 데 필요한 모든 부품 6세트가 포함되어 있습니다:

- 6x Sensor PCB
- 6x 3-pin 직각 헤더
- 6x 4mm 자석 (스풀에 장착)
- (선택사항) 6x 센서 케이블

https://bezeklabs.etsy.com/listing/1696745674


**옵션 2: 부분 조립된 PCB를 직접 주문하고, 다른 부품은 별도로 주문**
v2 센서 디자인은 JLCPCB 조립에 최적화되어 있어 대부분 드래그 앤 드롭 프로세스이지만, 선택하는 옵션을 신중하게 이해하셔야 합니다. 가장 중요한 것은, JLCPCB에서 부품 재고가 없는 경우 *해당 부품을 단순히 누락한 채로 주문을 계속 진행한다는 것입니다!* 따라서 주문 시 표시되는 모든 경고나 알림을 주의 깊게 확인하세요.

JLCPCB 조립에는 여러 가지 고정 비용 (예: 고유 부품당 $3, 배송비 등)이 포함되므로 수량이 많을수록 더 좋은 가치를 얻을 수 있습니다.

센서 PCB는 충분히 단순해서 손납땜이 쉬우므로, 더 큰 디스플레이를 만드는 경우가 아니라면 실제로 아래 옵션 3 (빈 PCB와 부품을 주문하여 직접 조립)을 추천드립니다.

조립된 sensor v2 PCB를 주문하려면 최신 v2 센서 릴리스에서 다음 3개 항목을 다운로드하세요:

- [패널화된 gerber 파일](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/sensor-smd/v2/electronics-v2/sensor_smd-panelized-jlc/gerbers.zip) (PCB용)
- [패널화된 BOM](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/sensor-smd/v2/electronics-v2/sensor_smd-panelized-jlc/bom.csv) (조립에 필요한 부품 명시)
- [패널화된 CPL](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/sensor-smd/v2/electronics-v2/sensor_smd-panelized-jlc/pos.csv) (부품의 배치 위치 명시)

주문하기:

- JLCPCB https://cart.jlcpcb.com/quote 로 이동
- gerber zip 업로드
  - 매개변수 설정:
      - Layers: 2
      - 치수: (자동 생성된 치수 수락)
      - PCB Qty: 5 (참고로, 주문하는 "패널"에는 패널당 6x 센서가 포함되어 있으므로, 총 센서 수는 여기서 입력하는 PCB Quantity의 6배입니다! 즉, PCB 5개 주문 시 30개의 센서 PCB를 받게 됩니다. 이 수량보다 적게 조립할 수 있습니다)
      - Product Type: Industrial/Consumer electronics
  - PCB 사양
      - Different design: 1
      - Delivery format: Panel by Customer
      - Panel Format:
          - Column: 2
          - Row: 3
      - PCB 두께: 0.8mm ⚠️ 이는 기본 PCB 두께가 아닙니다 - 0.8mm를 반드시 선택하세요!
      - PCB 색상: 덜 일반적인 0.8mm 두께를 고려할 때 녹색이 가장 저렴합니다
      - LeadFree HASL
  - 기타 옵션 - 모두 기본값으로 두세요<br><a href="https://github.com/user-attachments/assets/5bc0a67e-3750-40d8-8386-1222e3ebc33c"><img src="https://github.com/user-attachments/assets/5bc0a67e-3750-40d8-8386-1222e3ebc33c" width="500" /></a>


- PCB Assembly 선택
    - 참고: JLCPCB는 주문한 PCB의 일부만 조립하도록 선택할 수 있게 해 줍니다. 이 예에서는 5개의 PCB(최소 수량)를 주문하고 그 중 2개만 조립하는 것(최소 조립 수량)을 보여드립니다.
    - 윗면 조립
    - PCBA Type: Economic
    - PCBA Qty: 2 (이는 6x _패널_ 중 2개로, 총 12x 센서 PCB입니다. 이 옵션이 나타나지 않으면 PCBA type을 Standard로 변경한 다음 다시 Economic으로 돌리세요!)
    - Tooling holes: Added by JLCPCB
    - Confirm Parts Placement: No (추가적인 보장을 원하시고 그들이 제공하는 production gerber 파일을 검토할 줄 안다면 Yes 선택)
    - Parts Selection: By Customer
    - Advanced Options: 모두 기본값으로 두세요<br><a href="https://github.com/user-attachments/assets/b4becb1c-d82d-4de8-8d68-b9cb381e58a8"><img src="https://github.com/user-attachments/assets/b4becb1c-d82d-4de8-8d68-b9cb381e58a8" width="500" /></a>


- BOM 파일 업로드
- CPL (csv) 파일 업로드
- File provided as: "Complete File, just proceed with my own files"를 반드시 선택하세요
  ![Screenshot from 2025-03-04 22-32-38](https://github.com/user-attachments/assets/998ad9c8-3e1f-44dc-a046-e0e210b1d497)


- 부품 검토
    - ⚠️ 재고가 없는 부품은 그냥 누락되므로 이 단계를 신중하게 확인하세요! ⚠️
  ![Screenshot from 2025-03-04 22-33-01](https://github.com/user-attachments/assets/62233f7d-e47d-4606-b3fb-e72767408937)


- 부품 배치 검토
  ![Screenshot from 2025-01-19 23-50-15](https://github.com/user-attachments/assets/6bd5e016-f792-46d8-ace7-8fe11aba9cfb)

- 장바구니에 저장
- 결제 (참고: JLC는 결제를 완료하기 전까지 부품을 예약하지 않으므로, 재고가 적을 때 결제를 미루면 부품이 누락될 가능성이 있습니다!)



또한 다음 항목들을 별도로 구매하셔야 합니다:
- 6x 4mm 원형 자석 (예: [Digi-Key](https://www.digikey.com/en/products/detail/radial-magnets-inc/9027/5218822))
- 6x 3-pin 직각 핀 헤더 (예: [Digi-Key](https://www.digikey.com/en/products/detail/sullins-connector-solutions/PREC003SBAN-M71RC/2774931))
- 6x 300mm 3-pin “servo” 수-수 케이블 (예: [Amazon](https://amzn.to/3FdxP8K) (10팩) [또는 [비제휴 링크](https://www.amazon.com/VIMVIP-10pcs-300mm-Extension-Futaba/dp/B00N8OX7VO)], 또는 [AliExpress](https://www.aliexpress.com/item/32800106648.html) (10팩))
https://bezeklabs.etsy.com/listing/966380990/splitflap-sensor-pcb-set-bare


**옵션 3: 빈 PCB를 직접 주문하고, 모든 부품은 별도로 주문**
PCB 주문은 위의 지침을 따르되 조립 부분은 건너뛰세요.

위에서 언급된 부품 (자석, 커넥터, 케이블) 외에도 PCB 자체를 위한 부품도 주문해야 합니다:
- 6x Hall sensor (예: HX6286, LCSC [C495736](https://www.lcsc.com/product-detail/Hall-Switches_HUAXIN-HX6286ESO_C495736.html?s_z=n_C495736))
- (선택사항) 6x 0603 빨간색 LED (예: LCSC [C2286](https://www.lcsc.com/product-detail/LED-Indication-Discrete_Hubei-KENTO-Elec-KT-0603R_C2286.html?s_z=n_C2286))
- (LED용 선택사항) 6x 0603 1k 저항 (예: LCSC [C21190](https://www.lcsc.com/product-detail/Chip-Resistor-Surface-Mount_UNI-ROYAL-Uniroyal-Elec-0603WAF1001T5E_C21190.html?s_z=n_C21190))

# 기타 하드웨어 주문

**참고:** AliExpress 리스팅은 변경되거나 사라지는 경향이 있으며, 이전에 잘 작동했던 동일한 제품 리스팅을 사용하더라도 다른 또는 품질이 더 낮은 제품을 받게 될 수도 있습니다 (제가 어떻게 아는지 묻지 마세요 🙁). 이 항목들은 *제안일 뿐*이며, 한때는 잘 작동했지만 다시 주문할 때 동일한 품질의 제품을 받는다는 **보장은 없습니다**! 또한 AliExpress에서 한 번도 주문해 본 적이 없다면, 대부분의 항목이 도착하는 데 2-4주가 걸린다는 점을 명심하세요. 더 빠른 배송을 원하신다면 Amazon이나 ebay에서 더 비싼 가격에 비슷한 부품을 찾는 경우가 많습니다.

Amazon 링크는 제휴 링크이며, 추가 비용 없이 프로젝트를 지원하는 데 도움이 됩니다. 다만 제휴 링크 사용을 피하고 싶으시다면 비제휴 직접 링크도 함께 포함했습니다. 모든 항목은 제휴 프로그램과 완전히 독립적으로 선정되었으며, 특정 제품을 추천하기 위한 후원이나 결제는 일절 받지 않습니다.

| 항목                                                                        | 6개 모듈 제작에 필요한 수량 | 링크                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | BezekLabs에서 구매 가능 (미국 한정)                 | 비고                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------------------------------------------------------------------------- | ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 12V 28BYJ-48 스테퍼 모터                                                  | 6                             | [+28BYJ-48 모터 구매 가이드](../MotorGuide.ko.md) 참조                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 예 (Chainlink Driver 주문에 선택적으로 추가 가능) | 안타깝게도 같은 이름으로 다양한 모터가 판매되고 있어 올바른 모터를 찾기 어려울 수 있습니다. 자세한 내용은 [모터 구매 가이드](../MotorGuide.ko.md)를 참조하세요.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| M4 x 10mm **ISO 7380** 볼트                                                 | 60                            | TODO | 아니오                                                 | ![](https://paper-attachments.dropboxusercontent.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1627681268542_image.png)<br><br><br>**ISO 7380** (버튼 헤드) 볼트를 반드시 구매하세요. 다른 볼트 헤드 형태는 디자인에 비해 너무 클 수 있습니다 (오른쪽 사진의 좁은 클리어런스 참조).<br><br>반드시 **10mm 길이**여야 합니다.<br><br><br>----------<br><br>Fastenal은 미국 내 오프라인 매장이 있으므로 직접 픽업하고 싶으시다면 이용하실 수 있습니다.<br><br>심미적 이유로 흑색 산화 처리를 사용하시는 경우, 작업 시 더 기름지고 더러워지는 경향이 있으며 스테인리스와 같은 부식 저항성을 갖지 못한다는 점에 유의하세요. |
| M4 너트 (육각형)                                                          | 60                            | TODO | 아니오                                                 | 모듈당 10개의 너트 필요<br><br>----------<br><br>Fastenal은 미국 내 오프라인 매장이 있으므로 직접 픽업하고 싶으시다면 이용하실 수 있습니다.<br><br>심미적 이유로 흑색 산화 처리를 사용하시는 경우, 작업 시 더 기름지고 더러워지는 경향이 있으며 스테인리스와 같은 부식 저항성을 갖지 못한다는 점에 유의하세요.                                                                                                                                                                                                                                                                     |
| Flap                                                                        | 312 (6x 52-flap 모듈용) <br><br>또는 240 (6x 40-flap 모듈용)                         | 빈 flap: [Etsy](https://bezeklabs.etsy.com/listing/979720975/blank-splitflap-display-flaps) (6 모듈용 6팩 = 312 flaps)<br><br>사전 인쇄된 flap: [Etsy](https://bezeklabs.etsy.com/listing/1685633114) (6 모듈용 6팩) <br><br>또는 [PVC ID 카드](https://www.amazon.com/CR80-Mil-Graphic-Quality-Cards/dp/B0045TD22A)와 [Badge Slot Punch](https://www.amazon.com/Badge-Punch-Puncher-Luggage-Credentials/dp/B0006M648E)를 구매한 다음 [절단 지그를 제작](../Flaps.ko.md#31-build-a-flap-cutting-jig)하고 [직접 flap을 제작](../Flaps.ko.md#32-cut-flaps)하세요                            | 👈 예                                             | 제가 좀 편향적일 수 있지만, 미국에 계신다면 Etsy에서 다이컷된 flap을 구매하는 것을 *강력히* 추천드립니다. 직접 자르는 것보다 훨씬 쉽고 품질도 훨씬 더 좋습니다. 다만 직접 만드는 것보다는 비용이 더 듭니다.<br><br>미국에 계신다면 Etsy에서 메시지를 보내주시면 무료 샘플 몇 개를 보내드리겠습니다.<br><br><br>                                                  |
| 레터 스티커 팩<br>(**빈 flap**을 사용하거나 직접 flap을 자르는 경우) | 3                             | [Amazon](https://amzn.to/3cvqfKB) [또는 [비제휴](https://www.amazon.com/Duro-Decal-Permanent-Adhesive-Letters/dp/B0027601CM?) [링크](https://www.amazon.com/Duro-Decal-Permanent-Adhesive-Letters/dp/B0027601CM)]                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                    | 각 팩에는 모든 글자가 2개씩 들어 있습니다 (그리고 더 일반적인 글자는 여러 개의 여분이 들어 있는데, 여기서는 도움이 되지 않습니다)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 12V 전원 공급 장치                                                            | 1                             | Amazon에 많은 옵션 있음                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                    | 각 모듈은 약 0.25A를 필요로 하므로, **6 모듈 키트의 경우 최소 1.5A 정격의 전원을 구매해야 합니다**. 이는 받으시는 특정 28byj-48 모터에 따라 다릅니다. 모든 모터의 저항이 같지 않으므로 전류 요구량이 다를 수 있습니다.<br><br>"CCTV" 또는 "12V LED"는 2.1mm 배럴 잭 커넥터가 있는 12V 공급 장치를 검색하기 좋은 키워드입니다.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |




----------
# 조립

디스플레이를 조립할 준비가 되셨나요? [전체 조립 안내 문서](Assembly.ko.md)를 참조하세요.
