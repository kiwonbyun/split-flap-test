# Splitflap v0 주문 가이드 ("쉬운" 경로)
[<< 문서 인덱스로 돌아가기](../DocumentationIndex.ko.md)

이 문서는 splitflap 디스플레이의 부품을 주문하는 "쉬운" 방법(미국 한정)을 안내합니다. *주문의 단순함*에 최적화되어 있으며, *최저 비용*을 목표로 하지는 않습니다.

조금 더 저렴할 수 있는 다른 옵션을 검토하고 싶다면 [전체 주문 가이드 문서](OrderingComplete.ko.md)를 확인해 보시기 바랍니다. 다만 그 문서가 다소 부담스럽게 느껴진다면, 지금 보고 계신 이 문서가 적합합니다!

질문이 있으시면 [커뮤니티 Discord 서버](https://discord.gg/Hxnftc8PyW)에 문의해 주십시오!


## 레이저 컷 기계 부품

**공급처:** [Ponoko](https://www.ponoko.com/)를 추천드리지만, 가격이 다소 비쌉니다.

**재질:** MDF는 조립 시 Acrylic보다 다루기 쉽습니다(Acrylic은 부품을 끼울 때 깨지기 쉽고 부서질 수 있습니다). 다만 외관은 Acrylic만큼 멋지지 않다는 점은 인정해야 합니다. 잠재적인 좌절을 줄이기 위해 일반적으로 MDF를 권장합니다.

참고로, 각 모듈의 전면부는 약 **82.6mm 폭**과 **147.8mm 높이**를 가집니다.


- [ ]  각 모듈에 대해 3mm MDF로 제작된 다음 파일을 사용합니다: https://github.com/scottbez1/splitflap/releases/download/v0.7/3d_laser_vector-ponoko-3mm-mdf_1x.svg [177.42mm x 173.37mm]
    전체 주문 지침과 acrylic용 대체 파일은 [여기](OrderingComplete.ko.md)에서 확인할 수 있습니다.


## 전자 부품

**공급처:** [Bezek Labs](https://bezeklabs.etsy.com) (네, 제 자신의 매장을 추천하므로 편향된 시각이긴 합니다만, 이 보드들은 커스텀 보드이며 필요한 모든 부속품도 함께 제공되기 때문에 실제로 가장 쉬운 구매 옵션입니다)


- [ ]  [Chainlink Driver v1.1](https://bezeklabs.etsy.com/listing/1123280069/splitflap-chainlink-driver-v11) (모듈 6개당 1개)
    - 리본 케이블 길이: **45cm**
    - 모터 추가? **예, 28BYJ-48 6개 추가**
- [ ]  [센서 키트 (6개, 센서, 자석, 헤더 포함)](https://bezeklabs.etsy.com/listing/1139795321/splitflap-sensor-kit-6x-with-sensors)  (모듈 6개당 1개)
    - 케이블 포함? **예**
- [ ]  [Chainlink Buddy [T-Display]](https://bezeklabs.etsy.com/listing/1109357786/splitflap-chainlink-buddy-t-display) (*전체* 디스플레이당 1개, 최대 36개 모듈까지)
    - ESP32 T-Display 모듈 포함: **예**


## 플랩(Flap)

**공급처:** [Bezek Labs](https://bezeklabs.etsy.com) (다시 말씀드리지만 편향된 추천이긴 합니다. 그러나 상업적으로 구할 수 있는 대안이 없으며, 직접 만드는 데에는 많은 [시간과 인내](../Flaps.ko.md#option-3-diy-flaps)가 필요합니다)

**두 가지 좋은 옵션** (이 트레이드오프는 전적으로 사용자에게 달려 있습니다):

- [ ]  [~~사전 인쇄된 플랩~~](https://bezeklabs.etsy.com/listing/1119149706/splitflap-display-flaps-printed-last) ~~은 많은 시간을 절약해 주고 보기에도 훌륭하지만 더 비쌉니다. 6개 팩과 24개 팩이 약간의 할인가로 제공됩니다. 검정색 카드에 흰색 텍스트로만 제공됩니다.~~
    - **참고 (2023-12-12): 초기 인쇄 플랩 배치는 매진되었습니다**. 업데이트된 디자인을 작업 중이며, 2024년 초 출시 예정입니다. 이 새로운 인쇄 플랩을 기다리고 계신다면, 레이저 컷 부품 주문도 잠시 보류하실 것을 권장드립니다. 업데이트된 디자인은 모듈당 40개 플랩이 아닌 52개 플랩을 지원하도록 개편된 기계 설계와 함께 출시됩니다.

또는

- [ ]  빈 플랩을 구매한 후 [직접 글자 스티커를 붙일](https://www.youtube.com/watch?v=3lFECISLwyI) 수 있습니다
    - [ ]  [빈 플랩](https://bezeklabs.etsy.com/listing/979720975/blank-splitflap-display-flaps) (**4개 모듈**용 160개 플랩 팩, 또는 **6개 모듈**용 240개 플랩 팩으로 판매됩니다)
    - [ ]  [비닐 글자 스티커](https://amzn.to/37Frsjb) (Amazon에서 구매 가능). 빈 플랩은 흰색 또는 검정색으로 제공되며, 비닐 글자 스티커는 [다양한](https://amzn.to/3ieAZj9) [여러](https://amzn.to/37t1y1R) [색상](https://amzn.to/3tk4Ddh)으로 제공됩니다. (모듈 **2개**당 스티커 팩 1개)


## 하드웨어

**공급처:** McMaster-Carr (신뢰할 수 있지만 특히 배송비를 포함하면 다소 비쌉니다) 또는 다른 곳에서 이러한 일반적인 부품을 찾으세요


- [ ]  M4 x 10mm **버튼 헤드(button-head)** 볼트. 모듈당 11개 볼트가 필요합니다(따라서 6개 모듈에는 최소 66개가 필요합니다). 반드시 button-head 스타일이어야 합니다(예: 더 키가 큰 socket-cap 볼트는 간섭 문제를 일으킬 가능성이 높습니다)
    - [McMaster-Carr](https://www.mcmaster.com/92095A190/) 100개 팩
- [ ]  M4 육각 너트. 모듈당 11개 너트가 필요합니다(따라서 6개 모듈에는 최소 66개가 필요합니다)
    - [McMaster-Carr](https://www.mcmaster.com/91828A231/) 100개 팩


## 전원 공급 장치 및 배선

**공급처:** 다양한 옵션 가능

1~12개 모듈의 경우:

- [ ]  3.3v 전원용 22AWG 와이어 (저전류이므로 굵기는 중요하지 않습니다. 스크류 터미널과 함께 사용할 때는 연선보다 단선이 더 적합합니다)
- [ ]  *최소* **6개 모듈당 1.5A**, 약간의 여유분을 더한 용량의 12V 전원 공급 장치. "12V CCTV" 전원 공급 장치를 검색하면 Chainlink Buddy [T-Display]에 꽂을 수 있는 올바른 배럴 잭 커넥터를 가진 제품을 찾을 수 있는 좋은 방법입니다.
- [ ]  12v 전원 및 접지용 20AWG (또는 길이와 모듈 수에 따라 더 굵은 직경) 와이어

또는, 13~36개 모듈의 경우:

- [ ]  3.3v 전원용 22AWG 와이어 (저전류이므로 굵기는 중요하지 않습니다. 스크류 터미널과 함께 사용할 때는 연선보다 단선이 더 적합합니다)
- [ ]  *최소* **6개 모듈당 1.5A**, 약간의 여유분을 더한 용량의 12V 전원 공급 장치. *전원 공급 장치는 첫 번째 Chainlink Driver의 스크류 터미널에* ***직접*** *연결해야 합니다*. 12개 모듈을 초과할 경우 Chainlink Buddy의 배럴 잭 커넥터를 사용하지 마십시오. 전류 요구 사항을 감당할 수 없습니다!
- [ ]  12v 전원 및 접지용 16AWG (또는 길이와 모듈 수에 따라 더 굵은 직경) 와이어

또는, 36개 모듈을 초과하는 경우:
> [!WARNING]
> 36개 이상의 모듈을 사용하는 디스플레이에는 특별한 고려사항이 적용됩니다! 고전류 DC 전원 공급 장치와 관련된 한계 및 위험에 대해 확실히 이해하고 있어야 하며, 손상/부상으로부터 보호하기 위한 모든 합리적인 예방 조치를 취해야 합니다. 36개 이상 모듈로 [대형 디스플레이](../ElectronicsGuide.ko.md#Large-displays)를 제작할 경우, Chainlink Driver 사용자 가이드를 반드시 읽어 추가 정보를 확인하시기 바랍니다.


## 이것이 전부입니다!

Chainlink 전자 부품의 조립 및 설정에 대한 지침은 [Chainlink Driver 전자 부품 사용자 가이드](../ElectronicsGuide.ko.md)를 참조하십시오.


----------

링크 공시: Amazon Associate로서 적격 구매를 통해 수익을 얻으며, 이는 사용자에게 추가 비용이 발생하지 않습니다.
