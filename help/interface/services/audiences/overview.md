---
title: '[!DNL Audience Library]'
description: Experience Cloud  [!DNL Audience Library] で、訪問者データからオーディエンスのセグメント化への変換を管理する方法について説明します。
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: 3043cd913d5165c58fb84f3342b05a00a690d6a6
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 81%

---

# Experience Cloud オーディエンス {#topic_679810123CAA4E0CA4FA3417FB0100C7}

[!DNL Audience Library] は、Experience Cloudでオーディエンスを表示します。 オーディエンスは、訪問者の集合（[!DNL Experience Cloud] ID のリスト）です。ユーザーは、訪問者データからオーディエンスセグメントへの変換を管理できます。したがって、オーディエンスの作成と管理は、セグメントの作成と使用に似ています。 オーディエンスセグメントは、[!DNL Experience Cloud] の製品やサービスと共有することもできます。

![Experience Cloud のオーディエンス](assets/audiences.png)

オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成された新しいテンプレート
* [!DNL Analytics] に公開された [!DNL Experience Cloud] 個のセグメント
* [!DNL Audience Manager]

**リアルタイムオーディエンスと履歴オーディエンスの比較**

どのオーディエンスも、そのソースを問わず、リアルタイムターゲティングの用途で使用できます。ただし、Analytics から Audience Manager に共有されたオーディエンスは、リアルタイムターゲティング用にはアクセスできません。システムは、オーディエンスを 2 つの方法で評価します。

* Analytics の履歴オーディエンスは 4 時間ごとに評価されます。処理して共有するのに、合計で最大 8 時間かかる場合があります。履歴オーディエンスには常にリターン訪問者が含まれます。
* リアルタイムオーディエンスは Experience Cloud オーディエンスをソースとし、リアルタイムで評価されます。

## アプリケーションでのオーディエンスの使用方法 {#concept_01EB9345C5344597BC94A864EDD38EE1}

Experience Cloud アプリケーションでのオーディエンスの使用方法を次の表に示します。

| ソリューション | 説明 |
|--- |--- |
| Experience Cloud Audiences | オーディエンスライブラリを使用して、オーディエンスをネイティブに作成、管理および共有します。 実行できる操作は、次のとおりです。<ul><li>生の分析属性を使用してリアルタイムオーディエンスを使用します。</li><li>オーディエンスを組み合わせて複合オーディエンスを作成し、リアルタイムのデータと履歴データを結合します。</li><li>推定オーディエンスサイズのグラフィカルビューを参照してください。</li></ul><br>作成するオーディエンスのタイプの提案について詳しくは、[オーディエンス作成オプション](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=ja)を参照してください。 |
| Analytics | セグメント化では、セグメントを作成してレポートスイートと組み合わせ、そのセグメントを Experience Cloud に公開します。セグメントを公開すると、Experience Cloud の [!DNL Audience Library] ページに表示されます。（詳しくは、[ のヘルプの ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=ja)Experience Cloudへのセグメントの公開 [!DNL Analytics] を参照してください。） オーディエンスは、[!DNL Adobe Target] によって配信されるキャンペーンエクスペリエンスのターゲットオーディエンスとして、また [!DNL Audience Manager] で使用することもできます。 [!DNL Adobe Analytics] からオーディエンスを共有し、アクティブなキャンペーンで使用するために選択すると、過去 90 日間にセグメント定義条件を満たした訪問者プロファイルが[!UICONTROL オーディエンスサービス]に送信されます。共有オーディエンス数の上限は 75 に増えました。[!DNL Analytics] から Experience Cloud に共有するオーディエンスのユニークメンバー数が 2,000 万を超えてはなりません。キャッシュの影響で、Analytics で削除したレポートスイートが Experience Cloud に反映されるまで 12 時間かかります。 |
| Mobile Services | [!UICONTROL デバイスタイプ]レポートのサンバーストによるビジュアライゼーションを使用してモバイルトラフィックを分析します。 |
| [!DNL Target] | [ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)は、訪問者 ID とデータを、アプリケーションをまたいで使用するための、アクションにつながる単一のプロファイルに統合します。「[!UICONTROL Experience Cloud に公開]」チェックボックスを Adobe Analytics でセグメント作成処理中にオンにすると、Adobe Target のカスタムオーディエンスライブラリ内でセグメントを使用できるようになります。[!DNL Analytics] または [!DNL Audience Manager] で作成されたセグメントは、[!DNL Target] のアクティビティで使用できます。例えば、[!DNL Analytics] コンバージョン指標および [!DNL Analytics] で作成されたオーディエンスセグメントに基づいてキャンペーンアクティビティを作成できます。 |
| [!DNL Audience Manager] | 共有オーディエンスは、[!DNL Audience Manager] でのセグメント化に使用できます。Experience Cloud オーディエンスはすべて、[!DNL Audience Manager] でネイティブに使用でき、次に対応しています。<ul><li>アプリケーションワークフローでの共有および利用に関するビルトインの自動処理</li><li>他ツールとのデータ連携</li><li>類似モデリング</li></ul> |
| Campaign | <ul><li>別の Adobe Experience Cloud アプリケーションから Adobe Campaign に共有オーディエンスを読み込む。</li><li>共有オーディエンスの形式で受信者リストを書き出す。これらの共有オーディエンスは、お使いの別の Adobe Experience Cloud アプリケーションで使用できます。</li></ul> |
| Advertising Cloud | オーディエンスをターゲットとして使用します。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>訪問者が Analytics から共有されるオーディエンスの資格を得てから、その情報が [!DNL Target]、Ad Cloud および Campaign Standard で対応可能になるまでに、4～8 時間の遅延があります。

## オーディエンスライブラリのインターフェイス要素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] は、ネイティブのリアルタイムオーディエンス識別機能と共に、オーディエンスを作成および管理するためのライブラリを提供します。

**[!UICONTROL Experience Cloud]**／**[!UICONTROL Experience Platform]**／**[!UICONTROL People]**／**[!UICONTROL オーディエンスライブラリ]**

![オーディエンスライブラリにオーディエンスを追加](assets/audience_library.png)


| 要素 | 説明 |
|--- |--- |
| 新規 | [オーディエンスを作成](create.md)します。 |
| タイトルと説明 | オーディエンスを識別および説明する列見出し。 |
| 作成者 | オーディエンスセグメントを作成したユーザー。 |
| ソース | オーディエンスが作成された場所を示します。<ul><li>**Analytics:** Adobe Analyticsで作成され、Experience Cloudに公開されたセグメント。</li><li>**Experience Cloud：**[Experience Cloud Audiences で作成された](create.md)新しいオーディエンス。</li><li>**Audience Manager：** Audience Manager で作成されたオーディエンスは Experience Cloud オーディエンスに自動的に表示されます。</li></ul> |
| 現在のサイズ | 現在のオーディエンスのサイズ。 |
| アクティブ | セグメントのアクティブステータス。 |

{style="table-layout:auto"}

## Adobe Analyticsからのオーディエンスの公開

詳しくは、Adobe Analytics ドキュメントの [Experience Cloudへのセグメントの公開 ](https://experienceleague.adobe.com/en/docs/analytics/components/segmentation/segmentation-workflow/seg-publish) を参照してください。
