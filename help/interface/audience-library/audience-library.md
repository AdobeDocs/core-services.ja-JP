---
description: 訪問者データからオーディエンスのセグメント化への変換を管理します。
seo-description: 訪問者データからオーディエンスのセグメント化への変換を管理します。
seo-title: オーディエンス
solution: Experience Cloud
title: オーディエンス
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# オーディエンス {#topic_679810123CAA4E0CA4FA3417FB0100C7}

オーディエンスは、訪問者の集合（訪問者 ID のリスト）です。アドビのオーディエンスサービスは、訪問者データからオーディエンスセグメントへの変換を管理します。したがって、オーディエンスを作成および管理することは、セグメントを作成および使用することに似ています。また、オーディエンスセグメントを [!DNL Experience Cloud] と共有することもできます。

![](assets/audiences.png)

オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成される新しいソース
* [!DNL Analytics] に公開された [!DNL Experience Cloud] セグメントから
* 送信元 [!DNL Audience Manager]

**リアルタイムオーディエンスと履歴オーディエンスの比較**

どのオーディエンスも、そのソースを問わず、リアルタイムターゲティングの用途で使用できます。ただし、Analytics から Audience Manager に共有されたオーディエンスは、リアルタイムターゲティング用にはアクセスできません。システムは、オーディエンスを 2 つの方法で評価します。

* 履歴オーディエンスは Analytics をソースとし、12 時間ごとに評価されます。履歴オーディエンスには常にリターン訪問者が含まれます。
* リアルタイムオーディエンスは Experience Cloud オーディエンスをソースとし、リアルタイムで評価されます。


## ソリューションでのオーディエンスの使用方法 {#concept_01EB9345C5344597BC94A864EDD38EE1}

次の表に、Experience Cloud ソリューションでのオーディエンスの使用方法を示します。

| ソリューション | 説明 |
|--- |--- |
| Experience Cloud オーディエンス | [オーディエンスライブラリ](../audience-library/audience-library.md)インターフェイスで直接、オーディエンスを作成、管理、共有します。次のことができます。<ul><li>Analytics の生データを使用して、リアルタイムオーディエンスを使用する。</li><li>オーディエンスを結合して、リアルタイムデータと履歴データを合成したオーディエンスを作成する。</li><li>推定オーディエンスサイズをグラフィック表示する。</li></ul><br>作成するオーディエンスタイプについての推奨事項については、[Experience Cloud オーディエンス](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)を参照してください。 |
| Analytics | セグメンテーションでは、セグメントを構築してレポートスイートと組み合わせ、[Experience Cloud にセグメントを公開](../audience-library/audience-library.md)できます。公開したセグメントは[オーディエンス](../audience-library/audience-library.md)ページに表示されます。また、オーディエンスは、Adobe Target によって提供されるキャンペーンエクスペリエンスの対象オーディエンスとして使用したり、Audience Manager で使用したりできます。オーディエンスが Analytics から共有され、アクティブなキャンペーンで使用するために選択されると、過去 90 日間でセグメント定義条件に適合したすべての訪問者プロファイルが、Experience Cloud Audience Services プラットフォームに送信されます。重要：処理で追加の遅れが生じないように、Analytics から共有されるオーディエンスの数は、20 までに制限する必要があります。Analytics から Experience Cloud に共有するオーディエンスの個別メンバーの数が 2,000 万を超えてはなりません。キャッシュの影響で、Analytics で削除したレポートスイートが Experience Cloud に反映されるまで 12 時間かかります。 |
| Mobile Services | Analyze mobile traffic using the sunburst visualization in the [Device Types](https://marketing.adobe.com/resources/help/en_US/mobile/?f=reports_devices). |
| Target | [ID サービス](https://marketing.adobe.com/resources/help/en_US/mcvid/)により、訪問者 ID とデータが、ソリューション全体ですぐに使用できる単一のプロファイルに統合されます。「[Experience Cloud に公開](../audience-library/audience-library.md)」チェックボックスを Adobe Analytics でセグメント作成処理中にオンにすると、Adobe Target のカスタムオーディエンスライブラリ内でセグメントを使用できるようになります。Analytics または Audience Manager で作成されたセグメントは、Target のアクティビティで使用できます。例えば、Analytics コンバージョン指標および Analytics で作成されたオーディエンスセグメントに基づいてキャンペーンアクティビティを作成できます。 |
| Audience Manager | 共有オーディエンスは、Audience Manager でのセグメント化に使用できます。Experience Cloud オーディエンスはすべて、Audience Manager でネイティブに使用できます。Audience Manager は以下に対応しています。<ul><li>ソリューションワークフローでのオーディエンスの共有および利用の自動化</li><li>他ツールとのデータ連携</li><li>類似モデリング</li></ul> |
| キャンペーン | <ul><li>別の Adobe Experience Cloud ソリューションから Adobe Campaign に共有オーディエンスを読み込む。</li><li>共有オーディエンスの形式で受信者リストを書き出す。これらの共有オーディエンスは、お使いの別の Adobe Experience Cloud ソリューションで使用できます。</li></ul> |
| Media Manager | オーディエンスをターゲットとして使用します。 |


>[!IMPORTANT]
>
>訪問者が Analytics から共有されるオーディエンスの資格を得てから、その情報が Target、Media Manager および Campaign で対応可能になるまでに、24～48 時間の遅延があります。

## その他のヘルプ情報 - 質問、ガイダンス、使用例 {#section_C7F151644D8A45F7B6FC54F58845635D}


| ヘルプ情報 | リソース |
|--- |--- |
| オーディエンスが見つからない場合 | プロビジョニングが完了していることを確認します。詳しくは、[はじめに - コアサービスのソリューションを有効化](../core-services/core-services.md)を参照してください。<br>[ここ](https://www.adobe.com/go/audiences)をクリックして Profiles &amp; Audiences へのアクセス権をリクエストします（統合プロビジョニングフォーム）。 |
| 使用例 | 使用するソリューションの選択については、ナレッジベースで[オーディエンス作成オプション](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)を参照してください。 |
| フォーラム | [オーディエンスフォーラム](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences)でも、オーディエンスを利用するうえで役立つ情報を入手できます。 |


## オーディエンスライブラリのインターフェイス要素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] は、ネイティブのリアルタイムオーディエンス識別機能と共に、オーディエンスを作成および管理するためのライブラリを提供します。

**[!UICONTROL Experience Cloud]**／**[!UICONTROL Experience Platform]**／**[!UICONTROL People]**／**[!UICONTROL オーディエンスライブラリ]**

![](assets/audience_library.png)

| 要素 | 説明 |
|--- |--- |
| 新規 | [オーディエンスを作成](../audience-library/audience-library.md)します。 |
| タイトルと説明 | オーディエンスを識別および説明する列見出し。 |
| 作成者 | オーディエンスセグメントを作成したユーザー。 |
| ソース | オーディエンスが作成された場所を表示します。<ul><li>**Analytics：** Reports &amp; Analytics または Ad Hoc Analysis で作成されてから、[Experience Cloud](../audience-library/audience-library.md) に公開されたセグメント。</li><li>**Experience Cloud：**[Experience Cloud オーディエンスで作成された](../audience-library/audience-library.md)新しいオーディエンス。</li><li>**Audience Manager：** Audience Manager で作成されたオーディエンスは Experience Cloud オーディエンスに自動的に表示されます。</li></ul> |
| 現在のサイズ | 現在のオーディエンスのサイズ。 |
| アクティブ | セグメントのアクティブステータス。 |
