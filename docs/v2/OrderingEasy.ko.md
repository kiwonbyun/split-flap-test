# Splitflap v2 주문 가이드
[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

이 문서는 splitflap 디스플레이 부품을 주문하는 “쉬운” 방법(미국 한정)입니다. *주문의 단순함*에 최적화되어 있으며, *최저 비용*을 목표로 하지는 않습니다.

조금 더 저렴할 수 있는 다른 옵션들을 검토하고 싶다면 [전체 주문 문서](OrderingComplete.ko.md)를 확인해 보십시오. 다만 그 문서가 다소 부담스럽게 느껴진다면, 이 문서가 적합한 출발점이 될 것입니다!

질문이 있다면 [커뮤니티 Discord 서버](https://discord.gg/Hxnftc8PyW)에서 문의해 주십시오!


## 레이저 컷 기계 부품

**공급업체:** [Elecrow](https://www.elecrow.com/acrylic-cutting.html)는 합리적인 가격에 적절한 품질을 제공합니다

**소재:** Acrylic

v2 디자인은 모듈당 52장 또는 40장의 flap을 공식적으로 지원합니다. 이 문서에서는 52-flap 디자인을 기본으로 권장하며, 사전 인쇄된 "Epilogue" flap 세트를 구매할 계획이라면 완벽한 선택입니다. 다만 40-flap 변형에 대한 자세한 내용은 고급 주문 안내서를 참고하실 수 있습니다.

참고로, 각 모듈의 전면은 너비 약 **82.6mm**, 높이 약 **143.53mm**입니다.

- [ ] 3mm acrylic으로 제작된 52-flap 디자인을 주문하려면 다음 파일을 사용하십시오 (Matte Black (P502) 권장): [zip](https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-elecrow-3mm-acrylic_1x.zip)
    - [Elecrow acrylic laser cutting](https://www.elecrow.com/acrylic-cutting.html)으로 이동하여 zip 파일을 업로드합니다
    - 치수 입력: <img height="18" src="https://s3.amazonaws.com/splitflap-artifacts/refs/tags/releases/mechanics/v2/3d/3d_laser_vector-52-elecrow-3mm-acrylic_1x_dimensions.svg" />
    - 두께 선택: 3mm
    - 각인(Engrave): No
    - Acrylic 색상: Matte Black (P502) 권장

전체 주문 안내, acrylic/mdf의 대체 파일, 그리고 52-flap이 아닌 40-flap 모듈용 파일은 [여기](OrderingComplete.ko.md)에서 확인할 수 있습니다.

이전에는 Ponoko에서 주문할 것을 권장했었으며, 여전히 우수한 품질과 고객 서비스를 제공한다고 생각합니다. 그러나 가격이 너무 비싸져서 더 이상 기본 권장 사항으로 삼기 어려워졌습니다 😞 


## 전자 부품

**공급업체:** [Bezek Labs](https://bezeklabs.etsy.com) (네, 제 자신의 상점을 추천하는 것은 편향적이지만, 이 보드들은 커스텀 제품이고 필요한 부속품도 모두 포함되어 있어서 정말로 가장 쉬운 구매 옵션입니다). 


- [ ] [Chainlink Driver](https://bezeklabs.etsy.com/listing/1123280069/splitflap-chainlink-driver-v11) (문자 모듈 6개당 1개)
    - 리본 케이블 길이: **45cm**
    - 모터 추가? **예, 28BYJ-48 6개 추가**
- [ ] [Sensor kit v2 (자석과 헤더 포함 6개입)](https://bezeklabs.etsy.com/listing/1696745674/splitflap-sensor-kit-v2-beta-6x-with) (문자 모듈 6개당 1개)
    - 케이블 포함? **예**
- [ ] [Chainlink Buddy [T-Display]](https://bezeklabs.etsy.com/listing/1109357786/splitflap-chainlink-buddy-t-display) (*전체* 디스플레이당 1개, 최대 36개의 문자 모듈까지)
    - ESP32 T-Display 모듈 포함: **예**


## Flap

**공급업체:** [Bezek Labs](https://bezeklabs.etsy.com) (다시 말씀드리지만 편향적인 추천이지만, 상업적으로 구매 가능한 대안이 없으며 직접 만들려면 많은 [시간과 인내](../Flaps.ko.md#option-3-diy-flaps)가 필요합니다)

**두 가지 좋은 옵션이 있으며** (이 트레이드오프는 전적으로 본인의 선택입니다):

- [ ] [”Epilogue” 사전 인쇄된 v2 flap](https://bezeklabs.etsy.com/listing/1685633114/splitflap-epilogue-printed-flaps-beta-52)은 엄청난 시간을 절약해 주며 멋진 외관을 자랑하지만, 분명히 더 비쌉니다. 6팩과 24팩이 소량 할인된 가격에 제공됩니다. 검은색 카드에 흰색 텍스트만 제공됩니다.

또는

- [ ] 빈 flap을 구매하여 [직접 글자 스티커를 부착](https://www.youtube.com/watch?v=3lFECISLwyI)할 수 있습니다
    - [ ] [빈 flap](https://bezeklabs.etsy.com/listing/979720975/blank-splitflap-display-flaps) (52-flap 디자인의 경우 1x52 또는 6x52 팩을 구매하십시오. 6x 팩은 소량 할인된 가격에 제공됩니다)
    - [ ] [비닐 글자 스티커](https://amzn.to/37Frsjb) (Amazon에서 판매). 빈 flap은 흰색 또는 검은색으로 제공되며, 비닐 글자 스티커는 [다양한](https://amzn.to/3ieAZj9) [여러](https://amzn.to/37t1y1R) [색상](https://amzn.to/3tk4Ddh)으로 [구매](https://amzn.to/3ieAZj9)할 수 있습니다. (모듈 **2**개당 스티커 1팩)


## 하드웨어

**공급업체:** McMaster-Carr (신뢰할 수 있지만, 특히 배송비를 포함하면 다소 비쌉니다) 또는 이러한 일반 부품은 다른 곳에서도 찾을 수 있습니다


- [ ] M4 x 10mm **button-head**. 모듈당 10개 필요 (즉, 6개 모듈에는 최소 60개 필요). 반드시 button-head 스타일이어야 합니다 (예: 더 키가 큰 socket-cap 볼트는 간섭 문제를 일으킬 가능성이 높습니다)
    - [McMaster-Carr](https://www.mcmaster.com/92095A190/) 100개입 팩
- [ ] M4 hex nut. 모듈당 10개 필요 (즉, 6개 모듈에는 최소 60개 필요)
    - [McMaster-Carr](https://www.mcmaster.com/91828A231/) 100개입 팩


## 전원 공급 장치 및 배선

**공급업체:** 다양한 옵션이 있으며, 특정 권장 사항은 없습니다

1~12개 모듈의 경우:

- [ ] 3.3v 전원용 22AWG 와이어 (저전류이므로 굵기는 중요하지 않으며, 스크류 터미널과 함께 사용할 때는 stranded보다 solid wire가 더 적합합니다)
- [ ] **모듈 6개당 최소 1.5A** 이상의 12V 전원 공급 장치, 약간의 여유 포함. “12V CCTV” 또는 LED 전원 공급 장치를 검색하면 Chainlink Buddy [T-Display]에 연결할 수 있는 적절한 barrel jack 커넥터를 가진 공급 장치를 찾을 수 있습니다. 
    - Amazon, AliExpress 등에서 판매되는 공급 장치의 전류 정격은 과대 표시되어 있다고 가정하고, 이를 고려하여 필요한 것보다 더 높은 전류 정격의 공급 장치를 선택하십시오.
- [ ] 12v 전원 및 접지용 20AWG 와이어 (또는 길이와 모듈 수에 따라 더 굵은 직경)

또는, 13~36개 모듈의 경우:

- [ ] 3.3v 전원용 22AWG 와이어 (저전류이므로 굵기는 중요하지 않으며, 스크류 터미널과 함께 사용할 때는 stranded보다 solid wire가 더 적합합니다)
- [ ] **모듈 6개당 최소 1.5A** 이상의 12V 전원 공급 장치, 약간의 여유 포함. *전원 공급 장치는 첫 번째 Chainlink Driver의 스크류 터미널에* ***직접*** *연결해야 합니다*. 12개를 초과하는 모듈에는 Chainlink Buddy의 barrel jack 커넥터를 사용하지 마십시오. 전류 요구 사항을 감당할 수 없습니다!
    - Amazon, AliExpress 등에서 판매되는 공급 장치의 전류 정격은 과대 표시되어 있다고 가정하고, 이를 고려하여 필요한 것보다 더 높은 전류 정격의 공급 장치를 선택하십시오.
- [ ] 12v 전원 및 접지용 16AWG 와이어 (또는 길이와 모듈 수에 따라 더 굵은 직경)

또는, 36개를 초과하는 모듈의 경우:
> [!WARNING]
> 36개를 초과하는 모듈을 사용하는 디스플레이에는 특별한 고려 사항이 적용됩니다! 고전류 DC 전원 공급 장치와 관련된 한계와 위험에 대해 깊이 이해하고 있어야 하며, 손상/부상을 방지하기 위해 합리적인 모든 예방 조치를 취해야 합니다. 36개 이상의 모듈로 [대형 디스플레이](../ElectronicsGuide.ko.md#Large-displays)를 제작할 예정이라면 자세한 내용은 Chainlink Driver 사용자 가이드를 반드시 읽어 보십시오.


## 이상입니다!

조립 방법에 대한 안내는 [Splitflap v2 조립 가이드](Assembly.ko.md) 및 [Chainlink Driver 전자 부품 사용자 가이드](../ElectronicsGuide.ko.md)를 참고하십시오. 



----------

링크 공시: Amazon Associate로서 본인은 자격 있는 구매에 대해 추가 비용 없이 수익을 얻습니다.
