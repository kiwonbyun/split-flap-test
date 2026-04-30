# Splitflap v0 종합 주문 가이드
[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

아래 안내는 최신 Chainlink 전자 시스템을 사용하여 **6개 모듈** 규모의 splitflap v0.7 디스플레이를 제작하는 데 필요한 모든 부품(일반 공구 제외)을 주문하는 과정을 단계별로 안내합니다.

조립할 준비가 되셨습니까? [Assembly Guide](Assembly.ko.md)로 바로 이동하실 수 있습니다.

질문이 있으시면 언제든지 저(scott@bezeklabs.com)에게 연락해 주십시오. 또는 [Discord 서버](https://discord.gg/wgehm3PcrC)에 참여하셔서 더 넓은 split-flap 커뮤니티와 토론하거나 질문하실 수 있습니다!


😩 이 문서가 부담스럽게 느껴지시나요? 충분히 이해합니다. 내용이 정말 많으니까요... 그래서 미국 거주자를 위해 종합성/최저 비용보다는 단순함을 우선시하는 훨씬 짧은 문서를 따로 준비했습니다: [+Splitflap 주문 ("쉬운" 경로)](OrderingEasy.ko.md)


💡 본 안내서는 "Chainlink" 전자 시스템에 맞춰 업데이트되었습니다. 이 시스템은 조립이 더 쉽고 유연성이 뛰어나기 때문에, 신규 제작 시 기존(2016년경) "Classic Controller" 대신 권장됩니다. 이전 Classic Controller 안내가 필요하시다면 [부록](#부록-c-레거시-classic-controller)으로 옮겨졌습니다.


1. [레이저 컷 부품 주문](#레이저-컷-부품-주문)
3. [전자 부품 주문](#전자-부품-주문-chainlink)
2. [기타 하드웨어 주문](#기타-하드웨어-주문)
4. [부록 A: 구버전 레이저 컷 파일](#부록-a-구버전-레이저-컷-파일)
5. [부록 B: Hall sensor 옵션](#부록-b-hall-sensor-옵션)
6. [부록 C: 레거시 Classic Controller](#부록-c-레거시-classic-controller)
    1. [Classic 전용 하드웨어](#classic-전용-하드웨어)
    2. Classic Controller
        1. [컨트롤러 PCB 주문](#컨트롤러-pcb-주문-classic)
        2. [센서 PCB 주문](#센서-pcb-주문)
        3. [전자 부품 주문](#전자-부품-주문-classic)


----------
# 레이저 컷 부품 주문

레이저 컷 부품을 주문할 수 있는 곳은 많지만, 저는 개인적으로 미국 배송이 가능하고 온라인으로 손쉽게 주문할 수 있는 Ponoko와 Elecrow를 사용해 왔습니다. Ponoko는 수년간 사용해 왔으며 다양한 재료 옵션과 좋은 품질을 제공합니다. 최근에는 Elecrow의 레이저 컷 서비스를 알게 되었는데, **상당히** 저렴하면서도 좋은 품질을 제공합니다(다만 재료 옵션은 매우 제한적입니다).

각 모듈의 전면 면적은 약 **너비 82.6mm**, **높이 147.8mm**입니다.

고급 제작자를 위한 안내: 여러 모듈로 구성된 한 행(또는 격자) 전체를 공유하는 단일 전면 패널을 절단하고 싶다면, 간격, 행/열 수 등 다양한 구성 옵션을 지원하는 스크립트가 있으며, 내부 모서리에 필요한 "dog-bones"가 적용된 CNC 라우팅용 형상을 생성하는 모드도 제공됩니다 — `generate_combined_front_panel.py`를 참조하십시오.

💡 참고: v0.7 레이저 컷 부품은 구버전 v0.6 또는 v0.5 모듈과 치수 호환되지 않습니다! 기존 디스플레이를 확장하시는 경우, 여기에 링크된 새로운 v0.7 파일이 아닌 [본 문서 하단에 보관된](#older-v06-laser-cut-files) 구버전 v0.6 파일을 사용해 주십시오.


## Ponoko
    - 1 모듈
        - 3mm MDF: https://github.com/scottbez1/splitflap/releases/download/v0.7/3d_laser_vector-ponoko-3mm-mdf_1x.svg [177.42mm x 173.37mm]
        - 3mm Acrylic: https://github.com/scottbez1/splitflap/releases/download/v0.7/3d_laser_vector-ponoko-3mm-acrylic_1x.svg [177.26mm x 173.05mm]
    - 4 모듈
        - 3mm MDF: https://github.com/scottbez1/splitflap/releases/download/v0.7/3d_laser_vector-ponoko-3mm-mdf_4x.svg [354.84mm x 346.74mm]
        - 3mm Acrylic: https://github.com/scottbez1/splitflap/releases/download/v0.7/3d_laser_vector-ponoko-3mm-acrylic_4x.svg [354.52mm x 346.10mm]


- [Ponoko](https://www.ponoko.com/)에 접속하여 계정을 만드십시오.
- 위의 SVG 파일을 [업로드](https://www.ponoko.com/designs)하십시오. 치수가 위의 값과 일치하는지 확인하고, 파란 선이 "Cutting"으로, 검은색 채움이 "Area Engraving"으로 설정되어 있는지 확인하십시오(또는 새김 기능을 건너뛰려면 이 옵션을 끄십시오).
![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1590128918128_Screenshot+from+2020-05-21+23-28-11.png)

- 재료를 선택하십시오 - [MDF](https://www.ponoko.com/materials/mdf-fiberboard) 또는 [Acrylic](https://www.ponoko.com/materials/black-matte-acrylic)이 권장됩니다 — 두께는 3.0mm(0.12 인치)를 선택하십시오. 위의 파일 링크 옆에 표시된 치수와 재료의 최대 크기를 반드시 비교하여 확인하십시오. 일부 재료는 4x 버전을 주문하기에 너무 작을 수 있습니다.

💡 **Ponoko에서 Matte 1-Side** ****아크릴을 주문할 때 중요한 안내: 주문 후 ***즉시*** Ponoko에 *광택* 면에 디자인을 새겨 달라는 특별 지시 사항을 보내야 합니다. 그래야 디스플레이를 조립했을 때 무광 표면이 외부에 오도록 올바르게 절단됩니다. Ponoko 지원팀의 안내(2021-05-13 기준):

> 무광 재질은 [기본적으로] 무광 면이 위로 향한 상태로 절단됩니다(따라서 새김도 이 면에 이루어집니다).
>
> 광택 면에 새김을 원하시는 경우, **주문 확인 페이지에 답장**으로 요청해 주시면 주문 세부 사항에 메모해 두겠습니다.


## Elecrow

Elecrow는 주문당 디자인 5장을 "wood"(종류 미명시)로 절단해 주며, 가격은 $14.55 + 배송비입니다. 이보다 저렴한 옵션을 찾기는 어렵지 않을까 싶습니다(혹시 더 저렴한 곳이 있다면 알려 주십시오!).

경험상 앞뒤로 얇은 베니어가 있고 매우 가벼운 목재 코어가 있는 3겹 구조로 보입니다. 두께는 명세된 3mm보다 약간 얇은 ~2.8mm로 측정되었습니다. 마감과 재료의 품질은 Ponoko의 MDF만큼 훌륭하지는 않으며(제 주문에서는 절단부 근처에 눈에 띄는 그을음 자국이 있었음), 결정 시 이 점을 고려해 주십시오.


- 적절한 파일을 다운로드하십시오:
    - 3mm wood: https://github.com/scottbez1/splitflap/releases/download/v0.7/3d_laser_vector-elecrow-3mm-wood_1x.zip
    - 3mm acrylic: [아직 테스트되지 않았습니다. 시도하실 경우 위의 Ponoko 3mm acrylic 파일로 시작하는 것을 권장합니다. 어떤 파일을 사용하셨고 결과가 어땠는지(언더사이즈/오버사이즈 등) 알려 주시면, 그 피드백을 바탕으로 향후 권장 파일을 만들어 두겠습니다.]
- https://www.elecrow.com/5pcs-wood-laser-cutting-service.html 에 접속하십시오.
- 치수로 "20cm Max * 20cm Max(Thickness: 3.0mm)"를 선택하십시오.
- 위에서 다운로드한 .zip 파일을 업로드하십시오.
- 카트에 추가하고 결제하십시오.
![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1592618387746_Screenshot+from+2020-06-19+18-59-27.png)

- 배송 옵션으로 "Registered Airmail"은 피하시기를 권장합니다 - 한 달 넘게 걸렸고 추적도 형편없었습니다. ShenZhenDHL을 이용한 두 번째 주문은 며칠 만에 도착했습니다.
- 2020-06-1 기준 캘리포니아행 배송비 예시는 다음과 같습니다.
![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1592618688522_Screenshot+from+2020-06-19+19-03-30.png)

----------
# 전자 부품 주문 (Chainlink)

Chainlink 시스템은 더 강력한 ESP32 마이크로컨트롤러(Wi-Fi 지원 등 추가 기능 제공)를 기반으로 하는 새로운 전자 시스템이며, 이전 Classic Controller에서 얻은 교훈을 반영하였습니다. 신규 개발은 Chainlink 시스템에 집중되고 있습니다.

Chainlink 시스템에 필요한 기본 구성 요소는 다음과 같습니다:

- **Chainlink Driver 보드** (제어하려는 split-flap 모듈 6개당 1개)
- **Chainlink Buddy** + **ESP32** (디스플레이 크기와 무관하게 전체 디스플레이당 1개)
- **센서** (split-flap 모듈당 1개)

가장 쉽고 잘 지원되는 방법은 Bezek Labs Etsy 스토어(미국 한정)에서 각 항목을 구매하는 것입니다. 필요한 액세서리가 함께 제공되도록 스토어를 구성해 두었기 때문에, 여러 공급업체에서 따로 추적해 구매할 항목이 적어집니다. 수익은 프로젝트의 지속적인 개발에 보탬이 됩니다!

💡 다양한 구성에 대한 자세한 정보는 [Chainlink User Guide](../ElectronicsGuide.ko.md)를 참고해 주십시오.

## Chainlink Driver 주문
![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639441358230_DSC_4991_s.jpg)


Chainlink Driver는 최대 6개의 split-flap 모듈을 구동합니다. 여러 개의 Chainlink Driver를 연결하여(이름의 유래!) 훨씬 더 큰 디스플레이를 만들 수 있습니다(저는 18개의 Chainlink Driver 보드를 사용해 108-모듈 디스플레이를 제작한 바 있습니다).

Chainlink Driver는 대부분 표면 실장 부품을 사용하므로 수작업 납땜보다는 공장 양산에 최적화되어 있습니다(물론 원하시면 직접 납땜하실 수도 있습니다).

[**권장] 옵션 1: Etsy에서 완전히 테스트된 PCBA 구매 (미국 배송 한정)**
저는 거의 조립 완료된 Chainlink Driver 보드를 Bezek Labs Etsy 스토어에서 판매하고 있습니다:

https://bezeklabs.etsy.com/listing/1123280069/splitflap-chainlink-driver-v11


(액세서리 포함: 커넥터, ribbon cable)

까다로운 표면 실장 부품은 모두 미리 납땜되어 있습니다. 비교적 쉬운 through-hole 커넥터만 직접 납땜하시면 됩니다.

제가 판매하는 모든 보드는 제가 개발한 맞춤형 테스트 지그를 사용하여 모든 모터 출력, 센서 입력, LED, 데이터 라인이 예상대로 동작하는지 검증하는 엄격한 100% 기능 테스트를 거칩니다.

이 옵션은 필요한 모든 커넥터와 ribbon cable도 함께 제공하므로 별도로 주문하실 필요가 없습니다!

또한 AliExpress에서 그냥 주문하고 운에 맡기는 대신 올바른 28byj-48 모터를 확실히 받고 싶으시다면, Chainlink Driver 주문에 모터 6개를 함께 포함할 수 있는 옵션을 Etsy에 추가했습니다! 네, AliExpress에서 직접 주문하는 것보다는 비싸지만, 빠르게 배송되며 좋은 모터를 받으시리라는 점을 보장할 수 있습니다.

**옵션 2: JLCPCB에서 조립된 Chainlink Driver를 구매하고, 커넥터와 ribbon cable은 별도로 구매**
Chainlink Driver 설계는 JLCPCB 조립에 최적화되어 있어 대체로 드래그 앤 드롭 방식으로 진행되지만, 선택하는 옵션을 신중하게 이해하셔야 합니다. 가장 중요한 점은, JLCPCB에 어떤 부품의 재고가 없을 경우 *주문을 계속 진행하면서 해당 부품을 그냥 누락시킨다는 점입니다!* 따라서 주문 시 표시되는 모든 경고나 안내를 주의 깊게 확인하셔야 합니다.

JLCPCB 조립에는 부품당 $3 등의 고정 비용이 다수 포함되어 있어 수량이 많을수록 가성비가 좋아진다는 점도 유의해 주십시오.

최신 Chainlink Driver 릴리스(v1.1)에서 다음 3개 항목을 다운로드하십시오:

- gerber files (PCB용)
- BOM (조립에 필요한 부품을 명시)
- CPL (부품 배치 위치를 명시)

주문 절차:

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444226661_image.png)

- JLCPCB https://cart.jlcpcb.com/quote 에 접속하십시오.
- gerber zip 업로드
- 수량과 PCB 색상 선택
- 다른 매개변수 확인:
    - Dimensions: 30.48 x 198.12
    - PCB Thickness: 1.6
    - Outer Copper Weight: 1oz




![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444258704_image.png)

- SMT Assembly 선택
    - Assemble top side
    - 조립 수량 선택
    - Tooling holes: **Added by Customer** 선택 (이미 설계에 포함되어 있으므로 JLC가 추가할 필요 없음)
    - Confirm




![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444326379_image.png)

- BOM 파일 업로드
- CPL (csv) 파일 업로드






![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639444544494_image.png)

- 부품 검토
    - ⚠️ 재고가 없는 부품은 그대로 누락되므로 이 단계를 꼼꼼히 확인하십시오! ⚠️
    - JLCPCB에서 조립하지 않을 일부 커넥터(아래 참조)에 대해 "No part selected"가 표시되는 것은 *정상*입니다 - 이러한 항목은 "Motor A", "Sensor C", "Input", "Output" 등 "J" 접두사가 붙은 지정자를 가집니다.


- 부품 배치 검토
- Save to Cart
- 결제 (JLC는 결제가 완료될 때까지 부품을 예약해 두지 *않으므로*, 재고가 적은 경우 결제를 미루면 부품이 누락될 가능성이 있습니다!)

조립 비용을 낮추고, 다른 곳에서 쉽게 구할 수 있고 수작업 납땜이 용이한 부품의 변동성 있는 재고 문제를 피하기 위해, 조립용 설계 파일에는 *다음 부품이 포함되어 있지 않으므로* 별도로 주문하셔야 합니다(또는 아래 LCSC 부품 번호를 사용해 Review Parts 단계에서 선택하고 추가 조립 비용을 지불하실 수 있습니다):

- 2x IDC shrouded connectors, 2x4, 2.54mm spacing, 예: JLC/LCSC [C601937](https://lcsc.com/product-detail/IDC-Connectors_JILN-321008SG0ABK00A01_C601937.html), 또는 [Digi-Key](https://www.digikey.com/en/products/detail/adam-tech/BHR-08-VUA/9832409)
- 6x JST XH 5 pin connectors, 예: JLC/LCSC [C161872](https://lcsc.com/product-detail/Wire-To-Board-Wire-To-Wire-Connector_JST-Sales-America-B5B-XH-AM-LF-SN_C161872.html), 또는 [C378947](https://lcsc.com/product-detail/Wire-To-Board-Wire-To-Wire-Connector_JST-Sales-America-B5B-XH-A-BK-LF-SN_C378947.html), 또는 LCSC [C157991](https://lcsc.com/product-detail/Wire-To-Board-Wire-To-Wire-Connector_JST-Sales-America-B5B-XH-A-LF-SN_C157991.html), 또는 [Digi-Key](https://www.digikey.com/en/products/detail/jst-sales-america-inc/B5B-XH-AM-LF-SN/1651037)
- 6x 3-pin male headers, 2.54mm spacing, 예: JLC/LCSC [C49257](http://), 또는 Digi-Key [3-pin](https://www.digikey.com/en/products/detail/sullins-connector-solutions/PREC003SAAN-RC/2774851), 또는 [40-pin](https://www.digikey.com/en/products/detail/sullins-connector-solutions/PREC040SAAN-RC/2774814)을 구매하여 분리해 사용 (또는 Amazon 등에서 대량으로 손쉽게 구입 가능)

Chainlink Driver를 마이크로컨트롤러(또는 체인 안의 다른 Chainlink Driver)에 연결하려면 IDC ribbon cable + 커넥터도 필요합니다:

- 1x 8 conductor 1.27mm spacing ribbon cable (체이닝을 위해 권장 최소 길이 45cm), [예: Digi-Key](https://www.digikey.com/en/products/detail/w%C3%BCrth-elektronik/63910815521CAB/8324550)
- 2x IDC connectors, 예: LCSC [C601910](https://lcsc.com/product-detail/IDC-Connectors_JILN-531408YBS0BW01_C601910.html), 또는 [Digi-Key](https://www.digikey.com/en/products/detail/adam-tech/FCS-08-SG/9832361)

주문 후 JLCPCB로부터 screw terminal의 방향을 다시 확인해 달라는 이메일을 받으실 수 있습니다. 올바른 방향은 아래 이미지를 참고해 주십시오: 전선이 PCB의 Power 라벨 *위로* 통과하여 screw terminal의 앞쪽으로 삽입되어야 합니다.

![✅ screw terminal 방향이 올바른 설계의 3D 모델](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639550660519_image.png)
![✅ JLCPCB의 확인 이메일 - 올바른 screw terminal 방향. 보내주는 이미지가 이렇게 보이면 그대로 확인해 주십시오!](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639550557063_image.png)
![🚫 잘못된 예: 이렇게 보이면 방향이 반대로 되어 있는 것입니다!](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639551191137_chainlinkBadScrewTerminalOrientation.png)


**옵션 3: 빈 PCB와 부품을 구매하여 직접 손으로 조립**
이는 표면 실장 부품을 수작업으로 납땜해야 하는 고급 옵션입니다. 부품 자체가 아주 작지는 않지만(IC는 SOIC 패키지이고 수동 부품은 0603), 어느 정도의 숙련도와 인내심이 필요합니다.

스텐실을 주문하여 부품을 직접 reflow 납땜하는 것도 고려해 보실 수 있습니다. 다만 PCB가 길고 얇아서 가열 시 휨이 발생하기 쉬우므로, 오븐 대신 핫 플레이트를 사용할 계획이라면 어려움이 있을 수 있다는 점에 유의해 주십시오.

위 옵션 2의 안내에 따라 PCB를 주문하시되, 조립 옵션은 선택하지 마시고 BOM 파일을 사용해 모든 부품을 직접 주문하시면 됩니다. BOM 파일은 LCSC 부품 번호를 사용합니다.


## Chainlink Buddy와 ESP32 주문

ESP32 마이크로컨트롤러는 체인의 첫 번째 Chainlink Driver에 연결합니다. 이를 가장 쉽게 처리하는 방법은 사용 가능한 Chainlink "Buddy" 보드 중 하나를 사용하는 것이며, IDC/ribbon cable을 직접 꽂을 수 있습니다.

다양한 ESP32 모듈이 존재하며 대부분 호환됩니다(듀얼 코어이기만 하면). 하지만 TTGO T-Display를 강력히 권장합니다([Amazon](https://amzn.to/3kHwhMm)에서 빠르게 배송 가능 [제휴 링크는 추가 비용 없이 본 프로젝트를 후원합니다. 원하지 않으시면 [비제휴 링크](https://www.amazon.com/LILYGO-T-Display-Arduino-Development-CH9102F/dp/B099MPFJ9M)를 사용하셔도 됩니다], 또는 기다리실 수 있다면 [AliExpress](http://)). 240x135 LCD가 포함되어 있으며, splitflap 펌웨어가 기본적으로 지원하므로 디버깅에 매우 유용합니다.

**Chainlink Buddy [T-Display]**

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639445752808_DSC_5014_s.jpg)


Chainlink Buddy [T-Display]는 대부분의 사용자에게 권장되는 방식이며, ribbon cable 커넥터, 전원용 screw terminals, 편리한 12V 전원 입력을 위한 barrel jack과 함께 TTGO T-Display 마이크로컨트롤러를 Chainlink 시스템에 매우 쉽게 연결할 수 있도록 해줍니다.



[권장] Bezek Labs Etsy 스토어(미국 한정)에서 구매 가능:

https://bezeklabs.etsy.com/listing/1109357786/splitflap-chainlink-buddy-t-display


 (액세서리 포함: IDC connector, screw terminals, barrel jack, female headers)

 올바른 제품을 확실하게 받고 싶으시다면 T-Display ESP32 모듈도 함께 포함하는 옵션이 있습니다.


또는 gerber를 사용해 직접 PCB를 주문할 수도 있으며, 이 경우 다음 항목들도 함께 주문해야 합니다:

- 1x IDC shrouded connectors, 2x4, 2.54mm spacing, 예: LCSC [C601937](https://lcsc.com/product-detail/IDC-Connectors_JILN-321008SG0ABK00A01_C601937.html)
- 1x 3-pin 5.08mm spacing screw terminal, 예: LCSC [C72334](https://lcsc.com/product-detail/Screw-terminal_Ningbo-Kangnex-Elec-WJ500V-5-08-3P_C72334.html)
- 1x 2.1mm barrel jack, 예: LCSC [C381116](https://lcsc.com/product-detail/AC-DC-Power-Connectors_XKB-Connectivity-DC-005-5A-2-0_C381116.html)
- 2x 12-pin 2.54mm spacing female headers, 예: LCSC [C350303](https://lcsc.com/product-detail/Female-Headers_HOAUC-2685Y-112CNG1SNA01_C350303.html)




**Chainlink Buddy [Breadboard]**

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639446207182_DSC_5009_s.jpg)


다른 ESP32 모듈을 사용하고 싶으시다면, Breadboard Buddy는 Chainlink ribbon cable을 프로토타이핑용 브레드보드에 깔끔하게 연결하는 간단한 방법입니다. 일반적으로 권장되지는 않지만 고급 사용자를 위해 제공됩니다.




Bezek Labs Etsy 스토어(미국 한정)에서 구매 가능:

https://bezeklabs.etsy.com/listing/1123863267/splitflap-chainlink-buddy-breadboard


(액세서리 포함: IDC connector, male pin headers)

또는 gerber를 사용해 직접 PCB를 주문할 수도 있으며, 이 경우 다음 항목들도 함께 주문해야 합니다:

- 1x IDC shrouded connectors, 2x4, 2.54mm spacing, 예: LCSC [C601937](https://lcsc.com/product-detail/IDC-Connectors_JILN-321008SG0ABK00A01_C601937.html)
- 1x 5-pin 2.54mm spacing male pin headers


## 센서 주문

각 split-flap 모듈에는 홈 위치를 감지하기 위한 Hall sensor가 필요합니다. 이를 가장 잘 장착하는 방법은 작은 센서 PCB를 사용하는 것입니다.

[**권장] 옵션 1: Etsy의 센서 키트 (미국 한정)**
간편함을 위해 이 키트는 센서 6개를 조립하는 데 필요한 모든 부품을 6세트 포함합니다:

- 6x Sensor PCB
- 6x Hall sensor (가용성에 따라 AH3391Q 또는 유사 제품 - 항상 브랜드 정품 고품질 센서)
- 6x 3-pin right angle headers
- 6x 4mm 자석 (스풀에 장착)
- (선택) 6x 센서 케이블
https://bezeklabs.etsy.com/listing/1139795321/splitflap-sensor-kit-6x-with-sensors


**옵션 2: Etsy의 빈 센서 PCB (미국 한정) + 부품 별도 주문**
저는 처음에 Classic Controller를 제작하는 분들을 위해 빈 PCB 세트를 판매하기 시작했지만, Chainlink 시스템에서도 잘 동작합니다. 위의 풀 센서 키트보다 저렴할 수 있는 옵션이지만, 액세서리를 별도로 주문해야 하므로 결과적으로 더 저렴하지 않을 수도 있다는 점을 유념해 주십시오:

- Hall sensor (예: AH3391Q, [Digi-Key](https://www.digikey.com/en/products/detail/diodes-incorporated/AH3391Q-P-B/6575197), 또는 대안은 [부록](#부록-b-hall-sensor-옵션) 참조)
- 4mm 원형 자석 (예: [Digi-Key](https://www.digikey.com/en/products/detail/radial-magnets-inc/9027/5218822))
- 3-pin right-angle pin headers (예: [Digi-Key](https://www.digikey.com/en/products/detail/sullins-connector-solutions/PREC003SBAN-M71RC/2774931))
- 300mm 3-pin "servo" male-to-male 케이블 (예: [Amazon](https://amzn.to/3FdxP8K) (10개 팩) [또는 [비제휴 링크](https://www.amazon.com/VIMVIP-10pcs-300mm-Extension-Futaba/dp/B00N8OX7VO)], 또는 [AliExpress](https://www.aliexpress.com/item/32800106648.html) (10개 팩))
https://bezeklabs.etsy.com/listing/966380990/splitflap-sensor-pcb-set-bare


**옵션 3: PCB를 직접 주문하고 부품을 별도로 주문**
PCB 주문은 [이 안내](http://)를 따르시고, 위의 옵션 2에 언급된 부품(센서, 헤더, 자석)도 별도로 주문하셔야 합니다.



# 기타 하드웨어 주문

**참고:** AliExpress 상품 목록은 변경되거나 사라지는 경향이 있으며, 이전에 잘 작동했던 동일한 상품 페이지를 사용하더라도 다른 또는 품질이 낮은 제품을 받게 될 수 있습니다(저도 그렇게 알게 됐습니다 🙁). 이는 *제안일 뿐*입니다 - 한때는 잘 작동했지만, 다시 주문할 때 동일한 품질의 제품을 받을 것이라는 **보장은 없습니다!** 또한 AliExpress에서 처음 주문하시는 경우, 대부분의 항목이 도착하기까지 2-4주가 걸린다는 점을 기억해 주십시오. 빠른 배송을 원하시면 Amazon이나 ebay에서 더 비싼 가격에 비슷한 부품을 찾으실 수 있습니다.

**배송 안내:** Cainiao Super Economy로 인해 일련의 좋지 않은 경험(주문 완전 분실)을 했습니다. 또한 ~90일이 지날 때까지 환불 분쟁을 제기할 수도 없습니다. 대신 AliExpress Standard Shipping을 선택하시기를 권장합니다(보통 미국까지 2주 정도 걸리며 제 경험상 매우 안정적이었습니다).

✅가 표시된 링크는 과거에 성공적으로 사용된 것이고, ❓가 표시된 링크는 시도해 보지 않은 것입니다. 이 링크 중 하나를 성공적으로 또는 실패로 사용하셨다면 아래에 인라인으로 댓글을 남겨 주시면 업데이트하도록 노력하겠습니다.

Amazon 링크는 추가 비용 없이 프로젝트를 후원하는 제휴 링크입니다. 제휴 링크 사용을 피하고 싶으시다면 비제휴 직접 링크도 함께 포함했습니다. 모든 항목은 제휴 프로그램과 무관하게 독립적으로 선정되었으며, 특정 제품을 추천하기 위한 후원이나 대가는 받지 않습니다.

| 항목                                                                          | 6 모듈 제작에 필요한 수량 | 링크                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | BezekLabs에서 구매 가능 (미국 한정)                       | 비고                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------------------------------------------------------------------------- | ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 12V 28BYJ-48 Stepper Motor                                                  | 6                             | [+28BYJ-48 Motor Buying Guide](../MotorGuide.ko.md) 참조                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 예 (Chainlink Driver 주문에 선택적으로 추가 가능) | 안타깝게도 같은 이름으로 판매되는 모터의 종류가 매우 다양하고, 적합한 제품을 찾기 어렵습니다. 자세한 내용은 [Motor Buying Guide](../MotorGuide.ko.md)를 참고해 주십시오.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| M4 x 10mm **ISO 7380** bolt                                                 | 66                            | 스테인리스 스틸:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/4000077840372.html) (주문당 20개, 최소 3개 주문 권장)❓ <br><br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/200pcs-ISO7380-Hexagon-Socket-Button-Head-Screws-M4-5-6-8-10-12-16-18-20/32823699185.html) (주문당 200개 - 너무 많음) ✅ <br><br>[McMaster-Carr](https://www.mcmaster.com/92095A190/) (주문당 100개)<br><br>흑색 산화:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/32778146080.html) (주문당 50개)<br><br>[Fastenal](https://www.fastenal.com/products/details/1139900) (주문당 50개) ❓ <br><br>제안 환영 - 여기에 댓글을 남겨 주십시오 | 아니오                                                 | ![](https://paper-attachments.dropboxusercontent.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1627681268542_image.png)<br><br><br>반드시 **ISO 7380** (button head) 볼트를 구매하십시오 - 다른 볼트 헤드 모양은 설계에 비해 너무 클 수 있습니다(오른쪽 사진의 좁은 클리어런스 참조).<br><br>반드시 **10mm 길이**여야 합니다.<br><br><br>----------<br><br>저는 AliExpress의 JINGRUI Hardware에서 대량 주문을 잘 받아본 경험이 있습니다 - 배송과 소통이 좋고, 확실히 스테인리스 스틸(비자성)입니다.<br><br>Fastenal은 미국 내 오프라인 매장이 있어 직접 픽업하실 수 있습니다.<br><br>심미적 이유로 흑색 산화 제품을 사용하시는 경우, 작업 시 다소 기름지고 더러우며 스테인리스만큼의 내식성을 가지지 않는다는 점에 유의해 주십시오. |
| M4 nut (육각)                                                          | 66                            | 스테인리스 스틸:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/1005001493570161.html) (주문당 50개)❓ <br><br>[AliExpress](https://www.aliexpress.com/item/Free-Shipping-1000pcs-Lot-Metric-Thread-DIN934-M4-304-Stainless-Steel-Hex-Nut-Hexagonal-Nut-Screw/32574679688.html) (주문당 1000개 - 너무 많음) ✅ <br><br>[McMaster-Carr](https://www.mcmaster.com/91828A231/) (주문당 100개)<br><br>흑색 산화:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/1005001494639410.html) (주문당 50개) ✅ <br><br>[Fastenal](https://www.fastenal.com/products/details/40146)❓ <br><br>제안 환영 - 여기에 댓글을 남겨 주십시오                       | 아니오                                                 | 모듈당 11개의 너트가 필요하므로, 4 모듈 기준 50개 팩이 적당합니다.<br><br><br>----------<br><br>저는 AliExpress의 JINGRUI Hardware에서 대량 주문을 잘 받아본 경험이 있습니다 - 배송과 소통이 좋고, 확실히 스테인리스 스틸(비자성)입니다.<br><br>Fastenal은 미국 내 오프라인 매장이 있어 직접 픽업하실 수 있습니다.<br><br>심미적 이유로 흑색 산화 제품을 사용하시는 경우, 작업 시 다소 기름지고 더러우며 스테인리스만큼의 내식성을 가지지 않는다는 점에 유의해 주십시오.                                                                                                                                                                                                                                                                     |
| Flap                                                                        | 240                           | 빈 flap: [Etsy](https://bezeklabs.etsy.com/listing/979720975/blank-splitflap-display-flaps) (주문당 240+개) ✅ <br><br>~~사전 인쇄된 flap:~~ [~~Etsy~~](https://bezeklabs.etsy.com/listing/1119149706/splitflap-display-flaps-printed-last) ~~(주문당 40개) ✅~~ <br><br>또는 [PVC ID 카드](https://www.amazon.com/CR80-Mil-Graphic-Quality-Cards/dp/B0045TD22A)와 [Badge Slot Punch](https://www.amazon.com/Badge-Punch-Puncher-Luggage-Credentials/dp/B0006M648E)를 구매하여 [절단 지그를 제작](../Flaps.ko.md#31-build-a-flap-cutting-jig)하고, [flap을 직접 제작](../Flaps.ko.md#32-cut-flaps) ✅                           | 👈 예                                             | 제가 다소 편향되어 있을지도 모르지만, 미국에 계신다면 Etsy에서 die-cut flap을 구매하시기를 *강력히* 권장합니다 - 직접 자르는 것보다 훨씬 쉽고 품질이 훨씬 우수합니다(다만 직접 만드는 것보다 비쌉니다).<br><br>미국에 계신다면 Etsy로 메시지를 보내 주시면 무료 샘플 몇 장을 보내 드리겠습니다.<br><br><br>    - **참고 (2023-12-12): 초기 PRINTED flap 재고가 모두 소진되었습니다.** 업데이트된 디자인을 작업 중이며 2024년 초 출시 예정입니다. 이 새로운 인쇄 flap을 기다리고 계시다면, 레이저 컷 부품 주문도 잠시 보류하시기를 권장합니다. 업데이트된 디자인은 모듈당 40개의 flap이 아닌 52개의 flap을 지원하도록 갱신된 기계 설계와 함께 출시될 예정이기 때문입니다.                                                 |
| 글자 스티커 팩<br>(**빈 flap**을 사용하거나 직접 flap을 자르는 경우) | 3                             | [Amazon](https://amzn.to/3cvqfKB) ✅ [또는 [비제휴](https://www.amazon.com/Duro-Decal-Permanent-Adhesive-Letters/dp/B0027601CM?) [링크](https://www.amazon.com/Duro-Decal-Permanent-Adhesive-Letters/dp/B0027601CM)]                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                    | 각 팩에는 모든 글자가 2개씩 들어 있습니다(또한 더 흔한 글자의 여분이 많이 있는데, 이는 본 프로젝트에는 도움이 되지 않습니다).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 12V 전원 공급기                                                            | 1                             | Amazon에 다양한 옵션 있음                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                    | 각 모듈은 약 0.25A가 필요하므로, **6 모듈 키트의 경우 최소 1.5A 정격의 공급기를 준비해야 합니다.** 이는 사용하시는 28byj-48 모터에 따라 다릅니다. 모든 모터의 저항이 동일한 것은 아니므로 전류 요구량이 다를 수 있습니다.<br><br>2.1mm barrel jack 커넥터가 있는 12V 공급기를 찾을 때 "CCTV"가 좋은 검색어입니다.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |




----------
# v0.5/v0.6/v0.7 Splitflap 조립

디스플레이를 조립할 준비가 되셨습니까? [전체 조립 안내 문서](Assembly.ko.md)를 참고해 주십시오.


----------
# 부록 A: 구버전 레이저 컷 파일
## 구버전 v0.6 레이저 컷 파일

v0.7은 v0.5/v0.6과 비교해 호환되지 않는 치수 변경이 있으므로, 기존 v0.5/v0.6 디스플레이를 확장하시는 경우를 위해 구버전 v0.6 파일을 여기에서 참고할 수 있도록 제공합니다. 신규 제작에는 v0.7 이상을 권장합니다.

**Ponoko**

    - 1 모듈
        - 3mm MDF: https://github.com/scottbez1/splitflap/releases/download/v0.6/v0.6_laser_vector_ponoko_mdf_1x.svg [178.6 x 173.33 mm]
        - 3mm Acrylic: https://github.com/scottbez1/splitflap/releases/download/v0.6/v0.6_laser_vector_ponoko_acrylic_0.08kerf_1x.svg [178.42 x 172.97]
    - 4 모듈
        - 3mm MDF: https://github.com/scottbez1/splitflap/releases/download/v0.6/v0.6_laser_vector_ponoko_mdf_4x.svg [357.2 x 346.66 mm]
        - 3mm Acrylic: https://github.com/scottbez1/splitflap/releases/download/v0.6/v0.6_laser_vector_ponoko_acrylic_0.08kerf_4x.svg [356.84 x 345.94 mm]
    (개발자 참고: 레거시 이유로 MDF와 Acrylic 파일 모두 design `thickness = 3.2`로 생성됩니다.)

**Elecrow**

    - 3mm wood: https://github.com/scottbez1/splitflap/releases/download/v0.6/v0.6_laser_vector_elecrow_wood_0.185kerf_1x.zip
    - 3mm acrylic: [아직 테스트되지 않았습니다. 시도하실 경우 위의 Ponoko 3mm acrylic 파일로 시작하는 것을 권장합니다. 어떤 파일을 사용하셨고 결과가 어땠는지(언더사이즈/오버사이즈 등) 알려 주시면, 그 피드백을 바탕으로 향후 권장 파일을 만들어 두겠습니다.]


----------
# 부록 B: Hall sensor 옵션

AH3391Q hall sensor는 digikey에서 가끔 재고가 부족한 듯합니다. 그래서 제가 테스트해 본 몇 가지 대안이 잘 동작하는 것으로 확인되어 아래에 제시합니다. 반드시 **through-hole** 패키지를 선택하십시오 - 3-SIP가 필요하며 SOT23이나 다른 표면 실장(SMT) 모델은 **사용 불가**입니다.

**저렴한 AliExpress 옵션**
저는 AliExpress의 여러 매장 중 하나에서 "3144" hall-effect 센서를 주문해 본 결과, 기술 사양이나 데이터시트가 전혀 제공되지 않음에도 불구하고 잘 동작하는 것 같았습니다. 단종된 Allegro의 A3144 모방품일 수도 있을까요? 정확히 무엇을 받게 될지는 알 수 없습니다. 어쨌든 매우 저렴하긴 합니다!

참고: ESP32 또는 다른 3.3V 마이크로컨트롤러에는 추가적인 위험이 있습니다. 만약 이것이 실제로 A3144의 클론이라면 데이터시트 상 허용 전압 범위는 4.5V-24V이므로, 3.3V 동작은 정의되지 않은 결과를 만들 수 있습니다. 물론 실제 A3144는 단종되었고 대부분의 판매자가 데이터시트를 전혀 제공하지 않기 때문에, *모든* 결과가 정의되지 않았다고 주장할 수도 있습니다... 🤔

**DigiKey의 정품 대안**
저는 아래 각 옵션을 직접 테스트해 보았으며, 모두 동작함을 확인할 수 있습니다.

| **P/N**     | **유형**       | **trip** | **release** | **비고**               |
| ----------- | -------------- | -------- | ----------- | ----------------------- |
| AH3391Q-P-B | unipolar South | 275G     | 250G        | 잘 동작함, 권장 |
| AH3369Q-P-B | unipolar South | 175G     | 150G        | 잘 동작함              |
| AH3366Q-P-B | unipolar South | 100G     | 85G         | 잘 동작함              |
| AH3365Q-P-B | unipolar South | 100G     | 80G         | 잘 동작함              |
| A1122LUA-T  | unipolar South | 150G     | 125G        | 잘 동작함              |

**LCSC의 대안**
저는 아래 각 옵션을 직접 테스트해 보았으며, 모두 동작함을 확인할 수 있습니다.

| **P/N**                                                                                   | **유형**       | **trip** | **release** | **비고**                                                                                       |
| ----------------------------------------------------------------------------------------- | -------------- | -------- | ----------- | ----------------------------------------------------------------------------------------------- |
| [HX6286UA](https://lcsc.com/product-detail/Magnetic-Sensors_HUAXIN-HX6286UA_C495735.html) | unipolar South | 80G      | 60G         | 잘 동작함                                                                                      |
| [HX3144UA](https://lcsc.com/product-detail/Magnetic-Sensors_HUAXIN-HX3144UA_C558879.html) | unipolar South | 80G      | 60G         | 잘 동작함. 흥미롭게도 데이터시트가 (부품 번호를 제외하고) HX6286UA와 동일합니다...          |
| [SS443R](https://lcsc.com/product-detail/Magnetic-Sensors_Honeywell-SS443R_C396068.html)  | unipolar South | 135G     | 85G         | 잘 동작함                                                                                      |
| [CC6112TO](http://)                                                                       | unipolar South | 40G      | 30G         | 잘 동작함. trip point가 다른 것보다 약간 낮음(잡 자기장에 대한 민감도가 더 높음) |




다른 흔하고/저렴한 hall-effect 센서들 중 상당수가 본 응용에서 올바르게 동작하지 않을 수 있다는 점에 유의해 주십시오. 특히 "low power"로 광고되는 hall-effect 센서는 일반적으로 동작하지 않습니다. 저전력을 달성하기 위해 센서를 낮은 듀티 사이클로 샘플링하기 때문에, split-flap 디스플레이에 필요한 정밀도를 달성할 수 없기 때문입니다.

마찬가지로 omnipolar hall-effect 센서와 "latch" 센서도 주의하시기 바랍니다.

Omnipolar 센서는 동작*할 수도 있지만*, 자석이 센서에 측면으로 접근하기 때문에 자석이 충분히 강하면 자기장의 곡률이 *반대* 방향으로 임계값을 초과하여 자석이 통과하기 직전과 직후에 false activation이 발생할 위험이 있습니다(아래 이미지 참조). Unipolar 센서는 한 자기 극에 의해서만 활성화되고 다른 극에 의해서는 활성화되지 않으므로 이 문제가 없습니다.

![자석이 센서 바로 앞에 있을 때, 센서는 한 방향(이 예에서는 오른쪽)으로 자기장을 감지합니다.](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1625192375466_magnet_field_lines_A.png)
![자석이 센서로부터 옆으로 비껴 있을 때, (더 약한) 반대 방향(이 예에서는 왼쪽) 자기장을 감지할 수 있습니다. omnipolar 센서를 사용하면 이 자기장이 센서를 두 번째로 트리거할 수 있습니다! Unipolar 센서는 이런 잘못된 방향의 자기장을 무시하므로 선호됩니다.](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1625192379404_magnet_field_lines_B.png)


"Latch" 유형 센서는 거의 확실히 동작하지 않습니다. 동일한 강도의 자기장이 반대 방향으로 인가될 때까지 활성화 상태를 유지하기 때문입니다.


----------
## Digi-Key에서 대체 부품 찾기

추천 부품의 재고가 없거나 단종된 경우, Digi-Key는 가능한 대안을 비교적 손쉽게 정렬할 수 있도록 도와줍니다. 다음은 이전에 재고가 없었던 [이 부품](https://www.digikey.com/en/products/detail/PPPC032LFBN-RC/S7106-ND/810243)의 대안을 검색하는 예시입니다:

부품 페이지 하단의 "View Similar" 섹션이 매우 유용합니다. 결정적인 속성(자신이 직접 설계한 것이 아닌 경우 결정이 다소 어려울 수 있음)을 선택하여 일치하는 다른 부품을 찾을 수 있습니다.

이 경우 저는 **Active**(여전히 활발히 제조 중이라는 의미로, 사실 결정적이지 않을 수 있지만 영구적인 품절을 피하기 위해 부품을 추천할 때 항상 선택합니다), **Female Socket**, **6 pins**, 동일한 **0.1" spacing**과 **through-hole** 마운팅, 동일한 전체 높이(쉴드로 꽂히기 때문), **2 rows**를 선택했습니다.

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639590473850_Screenshot+2021-07-23+112433.png)


그런 다음 결과 페이지에서 단일 수량 가격 순으로 결과를 정렬하기 위해 수량 "1"을 입력하고, In Stock과 Exclude marketplace(써드 파티 판매자로 별도 배송비가 발생할 수 있음)도 선택합니다.

![](https://paper-attachments.dropbox.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1639590471321_Screenshot+2021-07-23+112504.png)


그 후에는 사진/데이터시트를 다시 한번 확인하여 예상한 부품과 일치하는지 점검하시는 것이 좋습니다.


# 부록 C: 레거시 Classic Controller

Classic Controller는 더 이상 신규 제작에 권장되지 않습니다. Chainlink 시스템이 선호됩니다.

## Classic 전용 하드웨어
|                                                                         | 4 모듈 제작에 필요한 수량 | 링크                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 비고                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ----------------------------------------------------------------------- | ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Arduino Uno                                                             | 1                             | Amazon 또는 AliExpress에 다양한 옵션 있음                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | (Classic Controller에서만 필요)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 12V 28BYJ-48 Stepper Motor                                              | 4                             | [+28BYJ-48 Motor Buying Guide](../MotorGuide.ko.md) 참조                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 안타깝게도 같은 이름으로 판매되는 모터의 종류가 매우 다양하고, 적합한 제품을 찾기 어렵습니다. 자세한 내용은 [Motor Buying Guide](../MotorGuide.ko.md)를 참고해 주십시오.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| M4 x 10mm **ISO 7380** bolt                                             | 44                            | 스테인리스 스틸:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/4000077840372.html) (주문당 20개, 최소 3개 주문 권장)❓ <br><br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/200pcs-ISO7380-Hexagon-Socket-Button-Head-Screws-M4-5-6-8-10-12-16-18-20/32823699185.html) (주문당 200개 - 너무 많음) ✅ <br><br>[McMaster-Carr](https://www.mcmaster.com/92095A190/) (주문당 100개)<br><br>흑색 산화:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/32778146080.html) (주문당 50개)<br><br>[Fastenal](https://www.fastenal.com/products/details/1139900) (주문당 50개) ❓ <br><br>제안 환영 - 여기에 댓글을 남겨 주십시오 | ![](https://paper-attachments.dropboxusercontent.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1627681268542_image.png)<br><br><br>반드시 **ISO 7380** (button head) 볼트를 구매하십시오 - 다른 볼트 헤드 모양은 설계에 비해 너무 클 수 있습니다(오른쪽 사진의 좁은 클리어런스 참조).<br><br>반드시 **10mm 길이**여야 합니다.<br><br><br>----------<br><br>저는 AliExpress의 JINGRUI Hardware에서 대량 주문을 잘 받아본 경험이 있습니다 - 배송과 소통이 좋고, 확실히 스테인리스 스틸(비자성)입니다.<br><br>Fastenal은 미국 내 오프라인 매장이 있어 직접 픽업하실 수 있습니다.<br><br>심미적 이유로 흑색 산화 제품을 사용하시는 경우, 작업 시 다소 기름지고 더러우며 스테인리스만큼의 내식성을 가지지 않는다는 점에 유의해 주십시오. |
| M4 nut (육각)                                                      | 44                            | 스테인리스 스틸:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/1005001493570161.html) (주문당 50개)❓ <br><br>[AliExpress](https://www.aliexpress.com/item/Free-Shipping-1000pcs-Lot-Metric-Thread-DIN934-M4-304-Stainless-Steel-Hex-Nut-Hexagonal-Nut-Screw/32574679688.html) (주문당 1000개 - 너무 많음) ✅ <br><br>[McMaster-Carr](https://www.mcmaster.com/91828A231/) (주문당 100개)<br><br>흑색 산화:<br>[AliExpress - JINGRUI Hardware](https://www.aliexpress.com/item/1005001494639410.html) (주문당 50개) ✅ <br><br>[Fastenal](https://www.fastenal.com/products/details/40146)❓ <br><br>제안 환영 - 여기에 댓글을 남겨 주십시오                       | 모듈당 11개의 너트가 필요하므로, 4 모듈 기준 50개 팩이 적당합니다.<br><br><br>----------<br><br>저는 AliExpress의 JINGRUI Hardware에서 대량 주문을 잘 받아본 경험이 있습니다 - 배송과 소통이 좋고, 확실히 스테인리스 스틸(비자성)입니다.<br><br>Fastenal은 미국 내 오프라인 매장이 있어 직접 픽업하실 수 있습니다.<br><br>심미적 이유로 흑색 산화 제품을 사용하시는 경우, 작업 시 다소 기름지고 더러우며 스테인리스만큼의 내식성을 가지지 않는다는 점에 유의해 주십시오.                                                                                                                                                                                                                                                                     |
| Flap                                                                    | 160                           | 빈 flap: [Etsy](https://www.etsy.com/listing/979720975/blank-splitflap-display-flaps) (주문당 160+개) ✅ <br><br>사전 인쇄된 flap: [Etsy](https://www.etsy.com/listing/1119149706/splitflap-display-flaps-printed) (주문당 40+개) ✅ <br><br>또는 [PVC ID 카드](https://www.amazon.com/CR80-Mil-Graphic-Quality-Cards/dp/B0045TD22A)와 [Badge Slot Punch](https://www.amazon.com/Badge-Punch-Puncher-Luggage-Credentials/dp/B0006M648E)를 구매하여 [절단 지그를 제작](../Flaps.ko.md#31-build-a-flap-cutting-jig)하고, [flap을 직접 제작](../Flaps.ko.md#32-cut-flaps) ✅                                                       | 제가 다소 편향되어 있을지도 모르지만, 미국에 계신다면 Etsy에서 die-cut flap을 구매하시기를 *강력히* 권장합니다 - 직접 자르는 것보다 훨씬 쉽고 품질이 훨씬 우수합니다(다만 직접 만드는 것보다 비쌉니다).<br><br>미국에 계신다면 Etsy로 메시지를 보내 주시면 무료 샘플 몇 장을 보내 드리겠습니다.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 글자 스티커 팩<br>(빈 flap을 사용하거나 직접 flap을 자르는 경우) | 3                             | [Amazon](https://amzn.to/3cvqfKB) ✅ [또는 [비제휴](https://www.amazon.com/Duro-Decal-Permanent-Adhesive-Letters/dp/B0027601CM?) [링크](https://www.amazon.com/Duro-Decal-Permanent-Adhesive-Letters/dp/B0027601CM)]                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 각 팩에는 모든 글자가 2개씩 들어 있습니다(또한 더 흔한 글자의 여분이 많이 있는데, 이는 본 프로젝트에는 도움이 되지 않습니다).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 12V 전원 공급기                                                        | 1                             | Amazon에 다양한 옵션 있음                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | 각 모듈은 약 0.25A가 필요하므로, **4 모듈 키트의 경우 최소 1A 정격의 공급기를 준비해야 합니다.** 이는 사용하시는 28byj-48 모터에 따라 다릅니다. 모든 모터의 저항이 동일한 것은 아니므로 전류 요구량이 다를 수 있습니다.<br><br>2.1mm barrel jack 커넥터가 있는 12V 공급기를 찾을 때 "CCTV"가 좋은 검색어입니다.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

## 컨트롤러 PCB 주문 (Classic)

**옵션 1: Etsy에서 구매 (미국 배송 한정)**
4개 모듈에는 컨트롤 PCB가 1개만 필요한데, 대부분의 저렴한 PCB 제조사는 최소 10개 보드부터 판매하기 때문에(또는 최소 배송비가 높아 소량 주문이 다소 비싸짐), Etsy 스토어에서 컨트롤러 PCB를 단일 수량으로 구매할 수 있도록 제공하고 있습니다: https://www.etsy.com/listing/980030861/splitflap-classic-controller-pcb-bare

여러 개의 splitflap 모듈을 만들고 컨트롤 보드가 많이 필요하다면, 직접 PCB를 제작하는 것이 더 저렴할 수 있습니다. 자세한 내용은 아래를 참조해 주십시오.

**옵션 2: SeeedStudio, JLCPCB 등에서 PCB 맞춤 주문**
일반적으로 배송비 ~$10-20 + PCB 비용 ~$5(PCB 10개), 도착까지 약 3-4주가 걸립니다.

- [gerber zip 파일](https://github.com/scottbez1/splitflap/releases/download/v0.5/pcb_gerber.zip)을 다운로드하십시오.
    - (또는 PCB당 컨트롤러 2개를 포함하는 [패널화된 gerber zip](https://github.com/scottbez1/splitflap/releases/download/v0.5/pcb_panelized_gerber.zip)을 선택하면, 동일한 $5 가격으로 "10"개 PCB 주문에서 20개의 컨트롤러를 얻을 수 있지만, 무게/크기 증가로 배송비가 더 비쌀 수 있습니다. 주문 시 치수를 48 x 96 대신 96 x 96으로 입력해야 합니다!)
- [SeeedStudio](https://www.seeedstudio.com/fusion_pcb.html)에 접속하십시오.
- "Add Gerber Files"를 클릭하고 방금 다운로드한 zip 파일을 선택하십시오.
- 녹색 박스의 "Gerber Viewer"를 클릭하여 디자인을 미리 보고 SeeedStudio가 올바르게 해석했는지 확인할 수 있습니다.
- 아래 설정을 입력하십시오:
![](https://paper-attachments.dropboxusercontent.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1543801701066_Screenshot+from+2018-12-02+17-48-08.png)

## 센서 PCB 주문
![](https://cdn.tindiemedia.com/images/resize/D5Ui32_szs97XWtsuGfp3h51Wno=/p/full-fit-in/2400x1600/i/334021/products/2018-09-08T16%3A10%3A57.088Z-DSC_2450.jpg)


센서 PCB(브레이크아웃 보드)는 각 모듈에 hall-effect 센서를 손쉽게 장착하고 조정할 수 있게 해줍니다. *반드시* 필요한 것은 아니며 hall-effect 센서를 다른 방법으로 부착할 수도 있지만, PCB가 훨씬 깔끔합니다.


|                               | 4 모듈 제작에 필요한 수량 | 링크                                                                                                                                                                                                                                          | 비고                                                                                                                                                                                                                                                                        |
| ----------------------------- | ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 30cm Male-to-Male Servo 케이블 | 4                             | [AliExpress](https://www.aliexpress.com/item/32800106648.html) (주문당 10개) ✅ <br>[Amazon](https://amzn.to/3FdxP8K) (주문당 10개) ✅ [또는 [비제휴 링크](https://www.amazon.com/VIMVIP-10pcs-300mm-Extension-Futaba/dp/B00N8OX7VO)] | **한 번**만 주문하면 됩니다 - 각 주문은 10개입니다.                                                                                                                                                                                                                                  |
| 자석 직경 4mm           | 4                             | [Digi-Key](https://www.digikey.com/en/products/detail/radial-magnets-inc/9027/5218822) ✅                                                                                                                                                      | Amazon이나 AliExpress의 4mm 직경(1mm-2.5mm 두께) 저가형 네오디뮴 자석 대부분이 일반적으로 잘 동작합니다.<br><br>위 Classic Controller의 단순화된 BOM에 포함되어 있으므로, 이를 사용하시면 별도로 주문하실 필요가 없습니다. |



**[권장] 옵션 1: Etsy에서 구매 (미국 배송 한정)**
원하는 PCB 제조사에서 센서 PCB를 주문할 수도 있지만(아래 참조), 필요한 것보다 훨씬 많은 센서 PCB를 받게 될 가능성이 높습니다. 몇 개만 필요한데 수백 개의 PCB 비용을 지불하는 대안으로, Etsy에서 4개 단위로 판매하고 있습니다: https://www.etsy.com/listing/966380990/splitflap-sensor-pcb-set-4x-bare

**옵션 2: 센서 브레이크아웃 PCB를 사용하지 않음**
센서 PCB 없이 hall-effect 센서를 장착하고 싶으시다면, **servo 케이블의 5V와 GND 핀을 서로 바꾼 다음** 케이블의 커넥터에 센서를 그냥 꽂아 사용하실 수 있습니다.

![브레이크아웃 PCB를 사용하지 않을 때는 빨간 선과 검은 선을 이렇게 바꾸십시오!!!!!!](https://pbs.twimg.com/media/DmTVjZUUYAAo6kJ.jpg:large)
![테이프로 고정?](https://pbs.twimg.com/media/DmTVjoXVAAASQ_Z.jpg:large)


**옵션 3: SeeedStudio에서 PCB 맞춤 주문 (대량 주문에만 해당)**
맞춤 PCB 주문에 익숙하시고 split-flap 모듈을 *많이* 만들 계획이라면, 다음 안내를 따라 200개(!!)의 센서 PCB를 받으실 수 있습니다. 센서 PCB 디자인은 SeeedStudio의 panelization 규칙(개별 보드는 V-cut 홈으로 분리됨)을 사용한 제조에 최적화되어 있으므로, 다른 제조사에서는 디자인 파일이 그대로 동작하지 않을 수 있습니다. 일반적으로 배송비 ~$10-20 + PCB 비용 ~$5(PCB 패널 10개, 각 패널에 20개의 센서 브레이크아웃 보드 = 총 200개), 도착까지 약 3-4주가 걸립니다. 100x100mm 이하 보드 제조 비용은 고정이고 배송비가 무게에 따라 크게 달라지지 않으므로, SeeedStudio에서 비패널화 센서 PCB를 주문하는 것은 비용 절감 효과가 거의 없어 의미가 없습니다.

![](https://paper-attachments.dropboxusercontent.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1543799736438_Screenshot+from+2018-12-02+17-14-12.png)



- [gerber zip 파일](https://github.com/scottbez1/splitflap/releases/download/v0.5/sensor_pcb_gerber.zip)을 다운로드하십시오.
- [SeeedStudio](https://www.seeedstudio.com/fusion_pcb.html)에 접속하십시오.
- "Add Gerber Files"를 클릭하고 방금 다운로드한 zip 파일을 선택하십시오.
- 녹색 박스의 "Gerber Viewer"를 클릭하여 디자인을 미리 보고 SeeedStudio가 올바르게 해석했는지 확인할 수 있습니다.
- 오른쪽에 표시된 설정을 입력하십시오 →
    (사진을 클릭하면 확대됩니다.)



## 전자 부품 주문 (Classic)

**참고:** 이 안내는 따라 하기 쉽도록 설계되었지만, 가장 저렴한 옵션은 아닙니다. 더 숙련된 취미 제작자라면 아래 BOM을 회로도에서 자동 생성된 원본 BOM([여기](https://github.com/scottbez1/splitflap/releases/tag/v0.5)에서 확인 가능)과 자세히 비교해 보시기를 권장합니다. 원본 BOM에는 일부 항목의 대체 출처에 대한 메모가 포함되어 있으며, 일부 항목은 결합하여 약간 더 저렴하게 주문할 수 있습니다. 또한 이미 일부 부품(예: 일반적인 저항)을 가지고 계실 수 있으니, 원하시면 그런 부품을 생략하실 수 있습니다.


- 다음 파일을 다운로드하십시오: https://github.com/scottbez1/splitflap/releases/download/v0.5/bom_simplified_digikey.csv
- https://www.digikey.com/ordering/shoppingcart 에 접속하십시오.
- "Upload a File" 옵션을 사용하여 위에서 다운로드한 bom_simplified_digikey.csv 파일을 업로드하십시오.
- "First Part Record Begins On Row:"에 **2**를 입력하십시오.
- 각 테이블 헤더에 대해 클릭하여 "Quantity", "Digi-Key Part Number", "Customer Reference"를 이 순서대로 선택하십시오.
- "Add to current cart"를 클릭하십시오.
- "An improved value option is available. View Options"라는 메시지가 표시될 수 있는데, 이는 일반적으로 더 *높은 수량*을 구매하면 실제로 더 저렴해진다는 의미입니다. **View Options**를 클릭하여 제안된 변경 사항을 확인하고, 좋아 보이면 Add를 클릭하십시오:
![](https://paper-attachments.dropboxusercontent.com/s_175A71EF755D30C645040845CEAC36F09A2519808F9780643CBAC746263B696C_1543777637600_Screenshot+from+2018-12-02+11-06-42.png)


**Hall sensor 옵션**
권장되는 hall sensor가 Digi-Key에서 품절인 경우, 대안 선택/주문에 대한 자세한 정보는 부록을 참고해 주십시오.


## 확장 컨트롤 보드 주문 (Classic)

컨트롤 보드 디자인은 체이닝 가능하며, 단일 Arduino에 최대 3개의 컨트롤 보드를 연결할 수 있습니다(메인 보드 1개 + 확장 보드 2개).

참고: 원래 명시된 barrel jack은 2.5A 정격뿐이지만 보드 3개는 약 3-5A를 끌어 단일 커넥터의 정격을 초과합니다. 동일한 footprint를 가지면서 6A 정격인 부품 번호 [839-1514-ND](https://www.digikey.com/product-detail/en/tensility-international-corp/54-00131/839-1514-ND/9685440)를 사용하거나, 각 보드에 개별적으로 전원을 공급하는 것을 고려하십시오(ribbon cable이 두 개의 와이어를 통해 보드 간 12V를 연결하지만 이를 잘라 분리할 수 있다는 점에 유의하십시오. 다만 GND는 12V와 5V 공급기 간에 공유되므로 보드 간 연결을 유지해야 합니다).

2개의 확장 컨트롤 보드는 메인 컨트롤 보드와 동일한 PCB를 사용하지만, BOM과 조립에서 몇 가지 작은 변경 사항이 있습니다:

| 컨트롤러 보드 2 & 3을 위한 변경 | 참조 | 부품 번호                             | 설명                                                                                                                                                                                                |
| ---------------------------------- | --------- | ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **추가**                            | J1, J2    | S9170-ND (x2)                              | 확장 커넥터 - **이전** 보드의 "EXP. OUT" 위치에 하나, **이번** 확장 보드의 "EXP. IN" 위치에 하나를 납땜하십시오.                                                      |
| **추가**                            | 없음      | H3CCS-1418G-ND                             | 확장 ribbon cable                                                                                                                                                                                     |
| **생략**                           | CON1      | CP-202A-ND                                 | barrel jack 커넥터는 확장 보드에 필요하지 않습니다 - 전원은 ribbon cable을 통해 확장 보드로 전달되므로 자체 전원 커넥터가 필요 없습니다.                                      |
| **생략**                           | JP1       | S1012EC-02-ND, S9337-ND                 | 이는 PCB를 Arduino에 쉴드로 꽂을 때 사용되는 부품입니다. 확장 보드는 Arduino에 꽂히지 않으며 대신 ribbon cable을 통해 데이터/전원을 받습니다(위 참조). |
| **생략**                           | U1        | S1012EC-03-ND, S1012EC-02-ND, S7106-ND | 이는 PCB를 Arduino에 쉴드로 꽂을 때 사용되는 부품입니다. 확장 보드는 Arduino에 꽂히지 않으며 대신 ribbon cable을 통해 데이터/전원을 받습니다(위 참조). |
| **생략**                           | R9        | CF14JT470RCT-ND                            | Arduino 연결과 관련된 470 ohm 저항(확장 보드는 Arduino에 직접 꽂히지 않음)                                                                                                     |


[Classic Controller 주문 안내 끝]

[Assembly](Assembly.ko.md)로 이동하십시오.

