---
title: “[!DNL Audience Library]“
description: Experience Cloudで訪問者データのオーディエンスセグメンテーションへの変換を管理する方法について説明します [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: 064f3c981b921fd5aec9b252b839d8b7f59b3dee
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 61%

---

# Experience Cloud Audiences {#topic_679810123CAA4E0CA4FA3417FB0100C7}

この [!DNL Audience Library] オーディエンスをExperience Cloudで表示します。 オーディエンスは、訪問者の集合（のリスト [!DNL Experience Cloud] IDs）. 訪問者データからオーディエンスのセグメント化への変換を管理できます。 したがって、オーディエンスの作成と管理は、セグメントの作成と使用に似ています。オーディエンスセグメントは、[!DNL Experience Cloud] の製品やサービスと共有することもできます。

![Experience Cloud のオーディエンス](assets/audiences.png)

オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成される新しいソース
* [!DNL Experience Cloud] に公開された [!DNL Analytics] セグメント
* [!DNL Audience Manager]

**リアルタイムオーディエンスと履歴オーディエンスの比較**

どのオーディエンスも、そのソースを問わず、リアルタイムターゲティングの用途で使用できます。ただし、Analytics から Audience Manager に共有されたオーディエンスは、リアルタイムターゲティング用にはアクセスできません。システムは、オーディエンスを 2 つの方法で評価します。

* Analytics の履歴オーディエンスは 4 時間ごとに評価されます。処理して共有するのに、合計で最大 8 時間かかる場合があります。履歴オーディエンスには常にリターン訪問者が含まれます。
* リアルタイムオーディエンスはExperience Cloudオーディエンスをソースとし、リアルタイムで評価されます。

## アプリケーションでのオーディエンスの使用方法 {#concept_01EB9345C5344597BC94A864EDD38EE1}

Experience Cloud アプリケーションでのオーディエンスの使用方法を次の表に示します。

| ソリューション | 説明 |
|--- |--- |
| Experience Cloud Audiences | を使用した、オーディエンスのネイティブな作成、管理、共有 [[!DNL Audience Library]](audience-library.md). 次のことができます。<ul><li>Analytics の生データを使用して、リアルタイムオーディエンスを使用する。</li><li>オーディエンスを結合して、リアルタイムデータと履歴データを合成したオーディエンスを作成する。</li><li>推定オーディエンスサイズをグラフィック表示する。</li></ul><br>作成するオーディエンスタイプについての推奨事項については、を参照してください。 [オーディエンス作成オプション](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=ja). |
| Analytics | セグメント化では、セグメントを作成してレポートスイートと組み合わせ、そのセグメントをExperience Cloudに公開できます。 セグメントを公開すると、に表示されます [!DNL Audience Library] Experience Cloudのページ。 （詳しくは、 [Experience Cloudへのセグメントの公開](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=ja) 。対象： [!DNL Analytics] 詳細については、ヘルプを参照してください）。 オーディエンスは、が配信するキャンペーンエクスペリエンスのターゲットオーディエンスとしても使用できます。 [!DNL Adobe Target]、および [!DNL Audience Manager]. オーディエンスを共有する相手 [!DNL Adobe Analytics]を選択し、アクティブなキャンペーンで使用するために選択すると、過去 90 日間にセグメント定義条件を満たした訪問者プロファイルがに送信されます [!UICONTROL Audience サービス]. 共有オーディエンス数の上限は 75 に増えました。からExperience Cloudに共有されたオーディエンス [!DNL Analytics] 一意のメンバーは 2,000 万人を超えることはできません。 また、キャッシュのため、Analytics で削除されたレポートスイートがExperience Cloudに表示されるまで、12 時間かかります。 |
| Mobile Services | [!UICONTROL デバイスタイプ]レポートのサンバーストによるビジュアライゼーションを使用してモバイルトラフィックを分析します。 |
| [!DNL Target] | [ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)は、訪問者 ID とデータを、アプリケーションをまたいで使用するための、アクションにつながる単一のプロファイルに統合します。この [Experience Cloudに公開](audience-library.md) Adobe Analyticsのセグメント作成プロセス中に「」チェックボックスをオンにすると、Adobe Targetのカスタムオーディエンスライブラリ内でセグメントを使用できるようになります。 で作成されたセグメント [!DNL Analytics] または [!DNL Audience Manager] でのアクティビティに使用できます [!DNL Target]. 例えば、[!DNL Analytics] コンバージョン指標および [!DNL Analytics] で作成されたオーディエンスセグメントに基づいてキャンペーンアクティビティを作成できます。 |
| [!DNL Audience Manager] | 共有オーディエンスは、次の場所で利用できます [!DNL Audience Manager] セグメント。 すべてのExperience Cloudオーディエンスは、でネイティブに使用可能です。 [!DNL Audience Manager]は次の機能を提供します。<ul><li>アプリケーションワークフローでの共有および利用に関する組み込み自動処理</li><li>他ツールとのデータ連携</li><li>類似モデリング</li></ul> |
| Campaign | <ul><li>別の Adobe Experience Cloud アプリケーションから Adobe Campaign に共有オーディエンスを読み込む。</li><li>共有オーディエンスの形式で受信者リストを書き出す。これらの共有オーディエンスは、お使いの別の Adobe Experience Cloud アプリケーションで使用できます。</li></ul> |
| Advertising Cloud | オーディエンスをターゲットとして使用します。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>訪問者が Analytics から共有されるオーディエンスの資格を得てから、その情報が [!DNL Target]、Ad Cloud および Campaign Standard で対応可能になるまでに、4～8 時間の遅延があります。

## その他のヘルプ情報 - 質問、ガイダンス、使用例 {#section_C7F151644D8A45F7B6FC54F58845635D}

| ヘルプの内容 | リソース |
|--- |--- |
| オーディエンスが見つからない場合 | プロビジョニングが完了していることを確認します。[はじめに - アプリケーションのコアサービスへの対応](core-services.md)を参照してください。<br>[ここ](https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES)から Profiles &amp; Audiences へのアクセス権をリクエストします（統合プロビジョニングフォーム）。 |
| フォーラム | [Audiences フォーラム](https://experienceleaguecommunities.adobe.com/t5/Adobe-Experience-Cloud-Audiences/ct-p/experience-cloud-audiences-community)でも、オーディエンスを活用するうえで役立つリソースを入手できます。 |

{style="table-layout:auto"}

## オーディエンスライブラリのインターフェイス要素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] は、ネイティブのリアルタイムオーディエンス識別機能と共に、オーディエンスを作成および管理するためのライブラリを提供します。

**[!UICONTROL Experience Cloud]**／**[!UICONTROL Experience Platform]**／**[!UICONTROL People]**／**[!UICONTROL オーディエンスライブラリ]**

![オーディエンスライブラリにオーディエンスを追加](assets/audience_library.png)

| 要素 | 説明 |
|--- |--- |
| 新規 | [オーディエンスを作成](audience-library.md)します。 |
| タイトルと説明 | オーディエンスを識別および説明する列見出し。 |
| 作成者 | オーディエンスセグメントを作成したユーザー。 |
| ソース | オーディエンスが作成された場所を示します。<ul><li>**Analytics:** Adobe Analyticsで作成されたセグメント、その場合 [Experience Cloudに公開](audience-library.md).</li><li>**Experience Cloud：**[Experience Cloud Audiences で作成された](audience-library.md)新しいオーディエンス。</li><li>**Audience Manager:** Audience Managerで作成されたオーディエンスは、Experience Cloudオーディエンスに自動的に表示されます。</li></ul> |
| 現在のサイズ | 現在のオーディエンスのサイズ。 |
| アクティブ | セグメントのアクティブステータス。 |

{style="table-layout:auto"}
