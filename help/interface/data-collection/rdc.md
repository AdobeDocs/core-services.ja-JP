---
title: 地域データの収集
description: 顧客体験管理（CX Enterprise）における地域データの収集について詳しく見る。
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
TQID: 'https://experienceleague.adobe.com/0thWRpu2KT2EFomB1hkgehjHfVrXMeKD-K0VN-fvfrM'
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2: id:id:
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 361
ht-degree: 1%

---

# 地域データの収集

Adobe CX Enterpriseでは、Regional Data Collection （RDC）を使用して、訪問者とAdobeのインタラクションが、可能な限り訪問者に近い場所で行われるようにします。 エッジサイトでローカルに収集されたデータは、処理のためにコアサイトに安全に転送されます。 処理されたデータは、Adobe CX Enterpriseの製品およびサービスで利用できます。

地域ごとのデータ収集ワークフローには、次のような利点があります。

* **パフォーマンス**: RDCを使用すると、訪問者は最も近いエッジ サイトに接続します。 この最適化により、応答時間が最速になり、より正確なトラッキングと読み込み時間の短縮が実現します。
* **冗長性**：任意のエッジサイトとコアサイトの間で通信に障害が発生した場合、Adobe インフラストラクチャはデータをローカルに保存し、通信が復元されるとコアサイトに転送します。 また、Adobeでは、特定の場所でweb サイトの障害が発生した場合、他のエッジサイトにトラフィックをルーティングすることもできます。

## ファーストパーティデータの収集

1st パーティデータの収集は、CNAMEを実装して、独自のドメインを介してデータをAdobeに転送します。 お使いのRDC タイプは、[Adobe管理証明書プログラム &#x200B;](adobe-managed-cert.md)のセットアップ プロセスの一部として選択されています。 RDC タイプを確認または更新するには、Adobe アカウントチームにお問い合わせください。 次のRDC タイプと関連するデータセンターを使用できます。

| RDC タイプ | データ収集センター |
| --- | --- |
| グローバル（デフォルト） | オレゴン州、バージニア州、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |
| グローバル +中国* | 北京*、オレゴン、バージニア、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |
| アメリカ大陸のみ | バージニア州オレゴン |
| ヨーロッパのみ | アイルランド、パリ |
| アジア太平洋のみ | ムンバイ、シンガポール、東京、シドニー |
| 中国のみ* | 北京 |

_*China RDCにはChina Performance Optimization アドオンパッケージが必要で、AppMeasurement データ収集を使用するAdobe Analyticsにのみ適用されます。 その他のCX Enterprise サービスおよびWeb SDK データ収集はサポートされていません。 China Performance Optimization アドオンパッケージの詳細については、Adobe アカウント チームにお問い合わせください。_

## サードパーティデータの収集

サードパーティデータの収集では、web サイトのドメインと一致しないCookie ドメインを使用します。 例として、`adobedc.net`、`omtrdc.net`、および `2o7.net` があります。

| RDC タイプ | データ収集センター |
| --- | --- |
| デフォルト | オレゴン州、バージニア州、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |
| Default + China* | 北京*、オレゴン、バージニア、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |

_*China Performance Optimization アドオンパッケージが必要です。 詳しくは、上記の1st パーティデータ収集の節を参照してください。_
