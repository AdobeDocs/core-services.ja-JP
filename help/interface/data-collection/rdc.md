---
title: 地域データの収集
description: CX Enterpriseの地域別データ収集の詳細。
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
TQID: https://experienceleague.adobe.com/hjHQDRoNOP2e6pKhKHB9DZaII2o8eJVzL5wjRzaMFwM
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
    internal-label: Experience Cloud Services
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: a714343bc3e17145e51fd99f64690e7d69ab4d9d
workflow-type: tm+mt
source-wordcount: '399'
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

[CDN](cdn.md)を介してデータ収集をルーティングする場合、リージョンロックされたRDC タイプには、[顧客が管理する証明書](customer-managed-cert.md)を持つファーストパーティのオリジンが必要です。

## サードパーティデータの収集

サードパーティデータの収集では、web サイトのドメインと一致しないCookie ドメインを使用します。 例として、`adobedc.net`、`omtrdc.net`、および `2o7.net` があります。

| RDC タイプ | データ収集センター |
| --- | --- |
| デフォルト | オレゴン州、バージニア州、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |
| Default + China* | 北京*、オレゴン、バージニア、アイルランド、パリ、ムンバイ、シンガポール、東京、シドニー |

_*China Performance Optimization アドオンパッケージが必要です。 詳しくは、上記の1st パーティデータ収集の節を参照してください。_

CDNを介して[&#x200B; サードパーティのオリジン &#x200B;](cdn.md#third-party-origin)にルーティングされたデータは、常にデフォルトのRDC タイプを使用します。
