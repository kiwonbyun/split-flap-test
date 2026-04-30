[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

# 플랩(flap)에 대하여
![플랩 치수](img/flapAnnotated.svg)

이 디자인의 플랩은 표준 신용카드 크기의 PVC 카드(일명 CR80)를 기반으로 합니다. 각 플랩은 카드의 1/2 크기이며, 양쪽 측면에 노치를 잘라내어 "핀"을 만들어 플랩 스풀에 끼워져 자유롭게 회전할 수 있도록 합니다.

각 모듈마다 52개의 플랩(v2) 또는 40개의 플랩(v0)이 필요하므로, 작은 6자리 디스플레이의 경우 완전한 DIY 방식으로 진행한다면 잘라내고 글자를 붙여야 할 플랩이 총 312개(v2) 또는 240개(v0)가 됩니다.

대형 디스플레이에 필요한 플랩의 수가 매우 많기 때문에, 저는 [Bezek Labs Etsy 상점](https://bezeklabs.etsy.com/)에서 판매하는 맞춤 제작 플랩(빈 플랩과 사전 인쇄된 플랩 모두)도 제작했으며, 이를 통해 많은 시간을 절약하고 이 프로젝트의 지속적인 개발을 지원할 수 있습니다.




# 옵션 1: 사전 인쇄된 플랩
<img src="img/flaps/bezekLabsPrintedFlaps.jpg" height="200" alt="Bezek Labs professionally cut blank white flaps" />

가장 많은 시간을 절약하고 싶다면, [전문적으로 재단되고 인쇄된 플랩 패키지](https://www.etsy.com/listing/1685633114)를 판매하고 있으며, 이는 split-flap 디스플레이에 바로 설치할 수 있도록 준비되어 있습니다. 이는 v2 디스플레이용으로 설계되었습니다.

이 프로젝트만을 위한 완전한 맞춤 제작이기 때문에 가격이 가장 높은 옵션이지만(한 패키지에 52개의 서로 다른 인쇄 디자인이 필요합니다!), 외관이 훌륭하고 장기간 사용에도 잘 견딥니다.

<a href="https://www.etsy.com/listing/1685633114">Bezek Labs Etsy 상점에서 1팩, 6팩, 24팩으로 구매 가능합니다</a>.

<a href="https://www.etsy.com/listing/1685633114">
<img src="img/flaps/bezekLabsPrintedFlapsListing.png" width="500" />
</a>

[^ 맨 위로](#about-flaps)

[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

# 옵션 2: 사전 재단된 빈 플랩
<img src="img/flaps/bezekLabsBlankFlaps.jpg" height="200" alt="Bezek Labs professionally cut blank white flaps" />
<img src="img/flaps/bezekLabsBlankFlapsBlack.jpg" height="200" alt="Bezek Labs professionally cut blank black flaps" />

중간 옵션은 사전 재단된 빈 플랩을 구매한 후, 원하는 글자 스티커를 직접 부착하는 것입니다. 이렇게 하면 모든 플랩을 자르고 펀칭하는 번거로움은 줄일 수 있지만, 모든 플랩에 스티커를 붙이는 다소 지루한 작업은 여전히 필요합니다.

<a href="https://bezeklabs.etsy.com/listing/979720975">Bezek Labs Etsy 상점</a>에서 빈 플랩 패키지를 판매하며, 광택 흰색 또는 무광 검정으로 제공됩니다.

<a href="https://bezeklabs.etsy.com/listing/979720975">
<img src="img/flaps/bezekLabsBlankFlapsListing.png" width="500" />
</a>

빈 플랩에는 [글자 스티커를 부착](#33-apply-letter-stickers)해야 합니다.

[^ 맨 위로](#about-flaps)

[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

# 옵션 3: DIY 플랩
<img src="img/flapCuttingJig/flaps.jpg" height="200" alt="flap with notches cut by hand" />

완전한 DIY 경험을 원한다면, CR80 카드를 반으로 자른 다음, 절반의 카드 양쪽에 노치를 펀칭하고, 마지막으로 글자 스티커를 부착하여 플랩을 만들 수 있습니다.

이 작업이 지루하게 들린다면, 사실 그렇다는 점을 인정합니다. 하지만 저는 처음 몇 개의 splitflap 모듈을 이렇게 만들었습니다.

## 3.1 플랩 절단 지그(jig) 만들기

40개의 플랩 모두에 대해 노치 절단이 일관되게 이루어져야 하므로, 우선 [배지 슬롯 펀치](http://www.amazon.com/gp/product/B009YDRRB4)용 지그를 만들어 절단 시 플랩을 정확한 위치에 고정할 수 있도록 합니다.

이 지그는 PVC 카드를 사용하여 손으로 만들 수도 있고, 3D 프린터가 있다면 간단히 출력할 수도 있습니다 ([아래 참조](#3d-printing-a-jig)).


### 지그 3D 프린팅하기

3D 프린터가 있다면, 손으로 지그를 만드는 대신 지그 모델을 출력할 수 있습니다. 다음과 같은 모습이 됩니다:

<img src="img/flapCuttingJig/printedJig1.jpg" width="320" alt="3d-printed jig" />

이 지그를 출력하려면, [3d/punch_jig.scad](https://github.com/scottbez1/splitflap/blob/master/3d/tools/punch_jig.scad)를 열어 렌더링한 후 STL 파일로 내보내십시오. 원하는 슬라이서를 사용하여 모델을 3D 프린팅용으로 준비할 수 있습니다.

<img src="img/flapCuttingJig/printedJig2.jpg" width="320" alt="3d-rinted jig" /> <img src="img/flapCuttingJig/printedJigModel.png" width="320" alt="Model of the 3d printed jig" />

(지그를 프린팅한다는 [아이디어](https://twitter.com/SilentM4X/status/974688413373870085)를 제공해주신 [@SilentM4X](https://twitter.com/SilentM4X)님께 감사드립니다!)


### 손으로 지그 만들기

PVC 카드로 만든 지그는 최종적으로 다음과 같은 모습이 됩니다:

<img src="img/flapCuttingJig/complete1.jpg" width="320" alt="badge punch with alignment jig" />

이를 만들기 위해, 먼저 PVC 카드의 절반(또는 주변에 굴러다니는 여분의 ID 카드나 신용카드)을 펀치 안쪽 끝까지 완전히 삽입하고 중앙에 슬롯을 펀칭합니다. 펀치가 여전히 맞물려 있는 동안(카드를 제자리에 고정한 상태에서) X-Acto 칼을 가져와 펀치의 바깥쪽 가장자리를 따라 카드 윗면에 살짝 흠집을 냅니다(표시할 정도로만).

<img src="img/flapCuttingJig/punched.jpg" width="320" alt="punched card with marked edges" />

카드와 자를 가져와 표시한 두 줄을 따라 흠집을 냅니다(카드 두께의 약 1/3 정도까지 자르되, 적게 자르는 쪽으로 신중하게 작업하십시오). 그런 다음 자를 펀칭된 슬롯의 카드 가장자리에 가장 가까운 평평한 모서리에 맞추고, 칼을 사용하여 펀칭된 슬롯의 오른쪽에서 카드 오른쪽 끝까지 카드를 완전히 잘라냅니다. 그런 다음 자를 90도 회전시켜 펀칭된 슬롯의 왼쪽에서 약 1~2mm 바깥쪽에 두고(이것이 플랩 "핀"의 두께를 결정합니다) 슬롯의 아래쪽 가장자리에서 카드 위쪽까지 자릅니다.

<img src="img/flapCuttingJig/scoresAndCuts.jpg" width="320" alt="punched card with scores and cuts" />

이 두 절단 부분을 연결하여 카드의 오른쪽 위 부분이 완전히 제거될 수 있도록 합니다:

<img src="img/flapCuttingJig/scoresAndCuts2.jpg" width="320" alt="punched card with section moved" />

흠집을 낸 두 모서리를 따라 카드를 자신으로부터 90도 멀어지는 방향으로 접습니다:

<img src="img/flapCuttingJig/folded.jpg" width="320" alt="folded jig" />

지그를 펀치에 삽입하고(처음 펀칭한 것과 동일한 방향으로) 테이프로 고정합니다:

<img src="img/flapCuttingJig/complete1.jpg" width="320" alt="folded jig in punch" /> <img src="img/flapCuttingJig/complete2.jpg" width="320" alt="folded jig in punch 2" />

<img src="img/flapCuttingJig/complete3.jpg" width="320" alt="folded jig in punch 3" /> <img src="img/flapCuttingJig/complete4.jpg" width="320" alt="folded jig in punch 4" />

이제 플랩 절단 지그가 완성되었습니다!

[^ 맨 위로](#about-flaps)

[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)


## 3.2 플랩 자르기

CR80 PVC 카드에서 플랩을 잘라내려면 먼저 반으로 잘라야 합니다. 종이 재단기로도 할 수 있겠지만, 저는 그것을 가지고 있지 않아서 유틸리티 칼로 흠집을 내고 반으로 부러뜨리는 지그를 만들었습니다.

먼저 폐목재 조각에 못 3개를 박아 카드를 제자리에 고정합니다:

<img src="img/flaps/cardPins.jpg" width="320" alt="nails to align card" />

그런 다음 작업 공간 양쪽에 카드 한두 장(저는 PVC 카드와 명함을 사용했습니다)을 놓아 자를 받쳐주는 받침대로 사용하며, 이 자는 흠집 내기를 위한 직선 가이드로 클램프로 고정됩니다.

<img src="img/flaps/ruler.jpg" width="320" alt="ruler placement" />

자가 위쪽 두 못으로부터 정확히 카드 길이의 1/2만큼 떨어진 위치에 클램프되었는지 확인하십시오:

<img src="img/flaps/rulerCaliper.jpg" width="320" alt="ruler alignment" />

그런 다음 빈 카드를 자 아래로 밀어 넣고 못에 단단히 밀착시킨 상태에서 자의 가장자리를 따라 흠집을 냅니다.

<img src="img/flaps/card1.jpg" width="320" alt="card to be cut" />

깔끔한 선이 만들어져야 하며, 너무 깊을 필요는 없습니다.

<img src="img/flaps/card2.jpg" width="320" alt="card with score line" />

자른 부분에서 카드를 반대 방향으로 구부려 자체적으로 접히도록 하되, 카드의 양 끝이 서로 일치하는지 확인하십시오(그렇지 않다면 자 정렬을 조정하여 수정하십시오). 그런 다음 카드를 다시 펴고 반대 방향으로 구부려 반으로 부러뜨립니다.

<img src="img/flaps/card3.jpg" width="320" alt="folded card" />
<img src="img/flaps/card4.jpg" width="320" alt="folded card 2" />

이 작업을 20장의 카드로 진행하여 40개의 절반 카드를 얻습니다. 그런 다음 각 절반 카드를 가져와 [[플랩 절단 지그|플랩 절단 지그 만들기]]를 사용하여 양쪽에 노치를 펀칭합니다.

<img src="img/flaps/punchedCard.jpg" width="320" alt="punched card" />
<img src="img/flaps/punchedCardStack.jpg" width="320" alt="stack of punched cards" />

펀칭된 구멍이 완전히 깔끔하지 않을 수 있지만(예: 구멍 외부에 일부 재료가 남아있음) 괜찮습니다. 대각 커터로 여분의 재료를 잘라내고 펀칭된 노치의 위쪽/아래쪽을 정리합니다.

<img src="img/flaps/clipCard.jpg" width="320" alt="clipping card with diagonal cutters" /> <img src="img/flapCuttingJig/flaps.jpg" width="320" alt="final cut flaps" />

플랩과 컷아웃의 더 정확한 치수와 그 값에 대한 근거에 관심이 있다면 다음 토론을 참조하십시오: https://github.com/scottbez1/splitflap/issues/8

시간을 절약하고 싶다면, 직접 플랩을 자르는 대신 제가 전문적으로 제작한 사전 재단 플랩을 [Etsy에서](https://bezeklabs.etsy.com/listing/979720975) 구매하는 것이 대안이 될 수 있습니다. 저로부터 사전 재단된 플랩을 구매하시면 이 오픈 소스 프로젝트의 지속적인 개발에도 도움이 됩니다.

[^ 맨 위로](#about-flaps)

[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)

## 3.3 글자 스티커 부착하기

플랩에 글자 스티커를 부착하기 위해, 일반적으로 시판되는 비닐 글자 스티커 패키지를 구매하는 것을 권장합니다(자세한 내용은 [v2 전체 주문 가이드](/docs/v2/OrderingComplete.ko.md) 또는 [v0 전체 주문 가이드](/docs/v0/OrderingComplete.ko.md)를 참조하십시오).

Cricut이나 Silhouette과 같은 비닐 커터가 있다면, [generate_fonts.py](https://github.com/scottbez1/splitflap/blob/master/3d/scripts/generate_fonts.py) 스크립트를 사용하여 원하는 글꼴/디자인의 맞춤 플랩 글자 스티커를 생성할 수 있습니다. 이 작업에 대한 팁은 [Dave Madison의 훌륭한 블로그 게시물](https://www.partsnotincluded.com/building-diy-split-flap-displays/#:~:text=Letter%20Generation)을 참고하시기 바랍니다! (그리고 이 글꼴 생성 스크립트를 프로젝트에 기여해주신 Dave Madison에게 감사드립니다!)

40개의 각 플랩에 글자 스티커를 부착하는 것은 고통스럽고 느린 과정입니다. 어느 정도 연습 후에도, 새로운 플랩 세트에 모든 스티커를 부착하는 데 약 1.5시간과 많은 인내가 필요했습니다:

[![비디오 타임랩스](img/flaps/timeLapseThumbnail.jpg)](https://www.youtube.com/watch?v=N_ifOY9FLs8)

**참고:** 그 이후로 글자 스티커를 부착하는 더 좋은 방법을 발견했습니다 - [새 지침](#new-instructions)을 참조하십시오. [기존 지침](#old-instructions)도 아래에 포함되어 있지만 더 이상 권장되지 않습니다.

### 새 지침

[유튜브 영상](https://www.youtube.com/watch?v=3lFECISLwyI)을 시청하십시오:

<a href="https://www.youtube.com/watch?v=3lFECISLwyI"><img src="https://img.youtube.com/vi/3lFECISLwyI/mqdefault.jpg" /></a>


이 방법은 훨씬 덜 스트레스가 되며, 이전 방법보다 정렬이 훨씬 더 잘 됩니다.

1. 오래된 신용카드나 호텔 키카드를 테이프로 고정하여 2개의 플랩을 받쳐줄 U자형 지그를 형성합니다. 빈 플랩 2개를 그 지그에 놓습니다. (선택적으로, 아래쪽 플랩의 하단 3/16인치(4.76mm)를 덮는 또 다른 카드나 종이를 테이프로 고정합니다 -- 이는 스티커 정렬을 위한 기준선 역할을 합니다)
1. 식품 보관용 클링 랩을 투명 용기 위에 단단히 적용한 다음, 글자 스티커를 **거꾸로**(끈끈한 면이 위로) 클링 랩 위에 올립니다. 정전기로 인해 클링 랩에 부착될 것이며, 이를 통해 스티커가 떨어지지 않고 전체를 뒤집을 수 있습니다.
1. 용기+클링 랩+스티커를 뒤집고, 투명 용기와 클링 랩을 통해 보면서 글자를 2개의 플랩에 정렬합니다(위에서 언급한 선택적 기준선 정렬 가이드가 있다면 사용하십시오). 용기를 아래로 눌러 스티커가 플랩에 부착되도록 한 후 용기를 제거합니다.
1. 손가락을 사용하여 글자 스티커 전체를 눌러 잘 부착되고 공기 방울이 없는지 확인합니다.
1. 글자 스티커를 두 플랩 사이의 간격을 따라 반으로 자릅니다.
1. 지그에서 아래쪽 플랩을 제거하고 따로 둡니다. 위쪽 플랩을 가져와 아래쪽 플랩 위치로 뒤집어 놓고, 새로운 빈 플랩을 위쪽 위치에 놓습니다.
1. 다음 글자 스티커로 2-6단계를 반복합니다.

### 기존 지침

스풀에 (빈) 플랩 두 개를 제외하고 모두 미리 끼워둔 상태에서 시작하면 순서를 올바르게 유지하기가 가장 쉽다는 것을 발견했습니다. 플랩의 가운데가 스풀의 중심에서 멀어지도록 부드럽게 눌러 스풀에 플랩을 추가하거나 제거할 수 있습니다: 검지 손가락을 컵 모양으로 만들어 플랩 아래에 받쳐 플랩의 가장자리만 손가락에 닿도록 하고, 엄지 손가락을 가운데로 눌러 플랩이 검지 손가락의 윤곽을 따라 휘어지도록 합니다. 이렇게 하면 핀이 안쪽으로 충분히 이동하여 플랩을 제자리에 끼워 넣거나 빼낼 수 있습니다:

<img src="img/flaps/addRemoveSpool.jpg" width="320" alt="Gently bend the flap to add/remove it from the spool" />

스풀에서 분리한 빈 플랩 2개로 시작하여, 작업 공간에 평평하게 놓고 스풀에 있을 때처럼 배치합니다(수직으로 서로를 미러링하며, 핀이 가운데에 위치).

각 글자에 대해:

1. 취미용 칼을 사용하여 글자 스티커를 반으로 자릅니다. 자보다 작고 이동이 쉬우므로, 1.5인치 높이로 자른 여분의 PVC 카드를 가이드로 사용했습니다.
1. 글자의 절반을 떼어내고(칼날을 사용하여 스티커를 백킹에서 분리하는 데 도움을 받을 수 있습니다), 자른 가장자리가 플랩의 자른 가장자리에 맞도록 플랩 중 하나에 조심스럽게 부착합니다.
1. 글자의 나머지 절반에도 같은 작업을 반복하되, 이미 부착한 절반과 정렬되도록 주의하십시오.
1. 아래쪽 플랩을 가져와 두 빈 슬롯 중 아래쪽 위치의 스풀에 다시 끼웁니다.
1. 위쪽 플랩(여전히 작업 공간에 있음)을 가져와 수직으로 뒤집어 아래쪽 플랩 방향으로 뒤집힌 상태가 되도록 합니다.
1. 스풀에서 빈 슬롯 위에 있는 빈 플랩을 제거하고, 위쪽 플랩 방향으로 작업 공간에 놓습니다.
1. 각 글자에 대해 단계를 반복합니다. 항상 다음 글자의 아래쪽 절반을 이전 글자의 위쪽 절반이 있는 플랩의 뒷면에 놓게 됩니다(예: "C"의 아래쪽 절반은 "B"의 위쪽 절반이 있는 플랩의 뒷면에 위치하고, "9"의 아래쪽 절반은 "8"의 위쪽 절반과 같은 물리적 플랩에 위치합니다).

[^ 맨 위로](#about-flaps)

[<< 문서 색인으로 돌아가기](../DocumentationIndex.ko.md)
