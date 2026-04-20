---
title: 地域データの収集
description: CX Enterpriseの地域別データ収集の詳細。
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
TQID: https://experienceleague.adobe.com/hjHQDRoNOP2e6pKhKHB9DZaII2o8eJVzL5wjRzaMFwM
product_v2: id: e1971122-7081-4556-9222-8a31bd71800c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 1%

---

# 地域データの収集

Adobe CX Enterpriseでは、Regional Data Collection （RDC）を使用して、訪問者とAdobe間のインタラクションを、可能な限り訪問者に近い場所で実行します。 エッジサイトでローカルに収集されたデータは、処理のためにコアサイトに安全に転送されます。 処理されたデータは、Adobe CX Enterpriseの製品およびサービスで利用できます。

地域ごとのデータ収集ワークフローには、次のような利点があります。

* **パフォーマンス**: RDCを使用すると、訪問者は最も近いエッジ サイトに接続します。 この最適化により、応答時間が最速になり、より正確なトラッキングと読み込み時間の短縮が実現します。
* **冗長性**：任意のエッジサイトとコアサイトの間で通信に障害が発生した場合、Adobe インフラストラクチャはデータをローカルに保存し、通信が復元されるとコアサイトに転送します。 また、Adobeでは、特定の場所でweb サイトの障害が発生した場合、他のエッジサイトにトラフィックをルーティングすることもできます。

現在、RDCには次の場所が含まれています（変更される場合があります）。

## ファーストパーティデータの収集

| RDC タイプ | データ収集センター |
| --- | --- |
| グローバル（デフォルト） | オレゴン州、バージニア州、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |
| グローバル +中国* | 北京*、オレゴン、バージニア、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |
| アメリカ大陸のみ | バージニア州オレゴン |
| ヨーロッパのみ | アイルランド、パリ |
| アジア太平洋のみ | ムンバイ、シンガポール、東京、シドニー |
| 中国のみ* | 北京 |

{style="table-layout:auto"}

_*China RDCにはChina Performance Optimization アドオンパッケージが必要で、AppMeasurement データ収集を使用するAdobe Analyticsにのみ適用されます。 その他のCX Enterprise サービスおよびWeb SDK データ収集はサポートされていません。 China Performance Optimization アドオンパッケージの詳細については、Adobe アカウント チームにお問い合わせください。_

## サードパーティデータの収集

サードパーティデータの収集には、web サイトのドメインと一致しないCookie ドメインが含まれます。 例として、`adobedc.net`、`omtrdc.net`、および `2o7.net` があります。

| RDC タイプ | データ収集センター |
| --- | --- |
| デフォルト | オレゴン州、バージニア州、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |
| Default + China* | 北京*、オレゴン、バージニア、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |

{style="table-layout:auto"}

