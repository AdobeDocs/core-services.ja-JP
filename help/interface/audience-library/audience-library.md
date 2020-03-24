---
description: 訪問者データからオーディエンスのセグメント化への変換を管理します。
seo-description: 訪問者データからオーディエンスのセグメント化への変換を管理します。
seo-title: オーディエンス
solution: Experience Cloud
title: Audiences
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: 14d6e0ae15b023ad4dd3f8aca0606f26b39a21e9

---


# オーディエンス {#topic_679810123CAA4E0CA4FA3417FB0100C7}

オーディエンスは、訪問者の集まり（訪問者IDのリスト）です。 アドビのオーディエンスサービスは、訪問者データからオーディエンスセグメントへの変換を管理します。 したがって、オーディエンスを作成および管理することは、セグメントを作成および使用することに似ています。また、オーディエンスセグメントを [!DNL Experience Cloud] と共有することもできます。

![](assets/audiences.png)

オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成される新しいソース
* [!DNL Analytics] に公開された [!DNL Experience Cloud] セグメントから
* 送信元 [!DNL Audience Manager]

**リアルタイムオーディエンスと履歴オーディエンスの比較**

どのオーディエンスも、そのソースを問わず、リアルタイムターゲティングの用途で使用できます。ただし、Analytics から Audience Manager に共有されたオーディエンスは、リアルタイムターゲティング用にはアクセスできません。システムは、次の2つの方法でオーディエンスを評価します。

* Analyticsの履歴オーディエンスは、4時間ごとに評価されます。 処理と共有に要する合計時間は最大8時間です。  履歴オーディエンスには常に再訪問者が含まれます。
* リアルタイムオーディエンスは Experience Cloud オーディエンスをソースとし、リアルタイムで評価されます。

## ソリューションでのオーディエンスの使用方法 {#concept_01EB9345C5344597BC94A864EDD38EE1}

次の表に、Experience Cloudソリューションでのオーディエンスの使用方法を示します。

| ソリューション | 説明 |
|--- |--- |
| Experience Cloud オーディエンス | [オーディエンスライブラリ](../audience-library/audience-library.md)インターフェイスで直接、オーディエンスを作成、管理、共有します。次のことができます。<ul><li>生の分析属性を使用したリアルタイムオーディエンスの使用</li><li>オーディエンスを組み合わせて、リアルタイムデータと履歴データを結合した複合オーディエンスを作成</li><li>推定オーディエンスサイズのグラフィカルな表示</li></ul><br>作成するオーディエンスのタイプに関する提案については、以下を参照してください。 [Experience Cloudオーディエンス](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)。 |
| Analytics | セグメンテーションでは、セグメントを構築してレポートスイートと組み合わせ、[Experience Cloud にセグメントを公開](../audience-library/audience-library.md)できます。公開したセグメントは[オーディエンス](../audience-library/audience-library.md)ページに表示されます。また、オーディエンスは、Adobe Target によって提供されるキャンペーンエクスペリエンスの対象オーディエンスとして使用したり、Audience Manager で使用したりできます。オーディエンスが Analytics から共有され、アクティブなキャンペーンで使用するために選択されると、過去 90 日間でセグメント定義条件に適合したすべての訪問者プロファイルが、Experience Cloud Audience Services プラットフォームに送信されます。共有オーディエンスの制限が75に増加しました。  AnalyticsからExperience Cloudに共有されるオーディエンスは、2,000万人を超える一意のメンバーを超えることはできません。 また、キャッシュのため、Analyticsで削除されたレポートスイートは、Experience Cloudに削除が表示されるまで12時間かかります。 |
| Mobile Services | デバイスタイプレポートのサンバースト視覚化を使用して、モバ [!UICONTROL イルトラフィックを分析] 。 |
| Target | The [ID service](https://docs.adobe.com/content/help/en/id-service/using/home.html) unifies visitor IDs and data into a single, actionable profile for use across solutions. 「[Experience Cloud に公開](../audience-library/audience-library.md)」チェックボックスを Adobe Analytics でセグメント作成処理中にオンにすると、Adobe Target のカスタムオーディエンスライブラリ内でセグメントを使用できるようになります。Analytics または Audience Manager で作成されたセグメントは、Target のアクティビティで使用できます。例えば、Analytics コンバージョン指標および Analytics で作成されたオーディエンスセグメントに基づいてキャンペーンアクティビティを作成できます。 |
| Audience Manager | 共有オーディエンスは、Audience Managerのセグメント化で使用できます。 Experience Cloud オーディエンスはすべて、Audience Manager でネイティブに使用できます。Audience Manager は以下に対応しています。<ul><li>ソリューションワークフローでの共有方法と使用方法に関するビルトインの自動化</li><li>オフサイトの宛先</li><li>類似モデリング</li></ul> |
| キャンペーン | <ul><li>別の Adobe Experience Cloud ソリューションから Adobe Campaign に共有オーディエンスを読み込む。</li><li>共有オーディエンスの形式で受信者リストを書き出す。 これらの共有オーディエンスは、使用する様々なAdobe Experience Cloudソリューションで使用できます。</li></ul> |
| Media Manager | オーディエンスをターゲットとして使用します。 |

>[!IMPORTANT]
>
>訪問者がAnalyticsから共有されたオーディエンスの資格を得ると、その情報がTarget、Ad Cloud、Campaign Standardでアクション可能になるまでに4 ～ 8時間の遅延が発生します。

## その他のヘルプ情報 - 質問、ガイダンス、使用例 {#section_C7F151644D8A45F7B6FC54F58845635D}

| ヘルプの | リソース |
|--- |--- |
| オーディエンスが見つからない場合 | プロビジョニングが完了していることを確認します。 See [Getting started - enable your solutions for core services](../core-services/core-services.md).<br>プロファ [イル](https://www.adobe.com/go/audiences) &amp;オーディエンス（統合プロビジョニングフォーム）へのアクセスをリクエストするには、ここをクリックします。 |
| 使用例 | 使用するソリューションの詳細については、ナレッジベースの [「オーディエンスの作成](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) 」オプションを参照してください。 |
| フォーラム | オーディ [エンスフォーラムは](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) 、オーディエンスに関するヘルプを得るための追加のリソースです。 |

## オーディエンスライブラリのインターフェイス要素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] は、ネイティブのリアルタイムオーディエンス識別機能と共に、オーディエンスを作成および管理するためのライブラリを提供します。

**[!UICONTROL Experience Cloud]** / **[!UICONTROL Experience Platform]** /人/オーデ **[!UICONTROL ィエンスラ]****[!UICONTROL イブラリ]**

![](assets/audience_library.png)

| 要素 | 説明 |
|--- |--- |
| 新規 | [オーディエンスを作成](../audience-library/audience-library.md)します。 |
| タイトルと説明 | オーディエンスを識別および説明する列見出し。 |
| 作成者 | オーディエンスセグメントを作成した人。 |
| ソース | オーディエンスが作成された場所を識別します。<ul><li>**Analytics：** Reports &amp; Analytics または Ad Hoc Analysis で作成されてから、[Experience Cloud](../audience-library/audience-library.md) に公開されたセグメント。</li><li>**Experience Cloud：**[Experience Cloud オーディエンスで作成された](../audience-library/audience-library.md)新しいオーディエンス。</li><li>**Audience Manager：** Audience Manager で作成されたオーディエンスは Experience Cloud オーディエンスに自動的に表示されます。</li></ul> |
| 現在のサイズ | 現在のオーディエンスのサイズ。 |
| アクティブ | セグメントのアクティブステータス。 |
