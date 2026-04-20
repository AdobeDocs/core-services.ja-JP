---
title: '[!DNL Audience Library]'
description: CX Enterprise [!DNL Audience Library]での訪問者データのオーディエンスセグメンテーションへの変換を管理する方法について説明します。
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
TQID: https://experienceleague.adobe.com/QEAfCWPNI-JhDw-HjZwBGv0TlqyctIqSwz8eVQqS6Gg
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 745
ht-degree: 48%

---

# CX Enterprise audiences

[!DNL Audience Library]はCX Enterpriseにオーディエンスを表示します。 オーディエンスは、訪問者の集合（[!DNL CX Enterprise] ID のリスト）です。 ユーザーは、訪問者データからオーディエンスセグメントへの変換を管理できます。 このように、オーディエンスの作成と管理は、セグメントの作成と使用に似ています。 オーディエンスセグメントは、[!DNL CX Enterprise] の製品やサービスと共有することもできます。

![CX Enterprise オーディエンス &#x200B;](assets/audiences.png)

オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL CX Enterprise]で作成された新しいオブジェクト
* [!DNL Analytics] セグメントが[!DNL CX Enterprise]に公開されました
* [!DNL Audience Manager]

**リアルタイムオーディエンスと履歴オーディエンスの比較**

どのオーディエンスも、そのソースを問わず、リアルタイムターゲティングの用途で使用できます。 ただし、Analytics から Audience Manager に共有されたオーディエンスは、リアルタイムターゲティング用にはアクセスできません。 システムは、オーディエンスを 2 つの方法で評価します。

* Analytics の履歴オーディエンスは 4 時間ごとに評価されます。 処理して共有するのに、合計で最大 8 時間かかる場合があります。 履歴オーディエンスには常にリターン訪問者が含まれます。
* リアルタイムのオーディエンスは、CX Enterprise Audiencesから取得され、リアルタイムで評価されます。

## アプリケーションでのオーディエンスの使用方法

次の表に、CX Enterprise アプリケーションでのオーディエンスの使用方法を示します。

| ソリューション | 説明 |
| --- | --- |
| CX Enterprise Audiences | オーディエンスライブラリを使用して、ネイティブにオーディエンスを作成、管理、共有できます。 実行できる操作は、次のとおりです。<ul><li>生の分析属性を使用してリアルタイムのオーディエンスを活用。</li><li>オーディエンスを組み合わせて合成し、リアルタイムおよび過去のデータを結合します。</li><li>推定オーディエンスサイズのグラフィカルビューを参照してください。</li></ul><br>作成するオーディエンスのタイプの提案について詳しくは、[オーディエンス作成オプション](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=ja)を参照してください。 |
| Analytics | セグメント化では、セグメントを作成し、レポートスイートと組み合わせて、セグメントをCX Enterpriseに公開できます。 セグメントを公開すると、CX Enterpriseの[!DNL Audience Library] ページに表示されます。 （詳しくは、[!DNL Analytics] ヘルプの[CX Enterpriseへのセグメントの公開](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=ja)を参照してください）。 このオーディエンスは、[!DNL Adobe Target]様および[!DNL Audience Manager]様が配信したキャンペーンエクスペリエンスのターゲットオーディエンスとしても利用できます。 [!DNL Adobe Analytics]からオーディエンスを共有し、アクティブなキャンペーンで使用するために選択すると、過去90日間のセグメント定義条件を満たした訪問者プロファイルが[!UICONTROL Audience Services]に送信されます。 共有オーディエンス数の上限は 75 に増えました。 [!DNL Analytics]からCX Enterpriseに共有されたオーディエンスは、2,000万人を超えることはできません。 また、キャッシュが原因で、Analyticsで削除されたレポートスイートは、CX Enterpriseに削除が表示されるまでに12時間かかる場合があります。 |
| Mobile Services | [!UICONTROL Device Types] レポートのサンバースト ビジュアライゼーションを使用して、モバイルトラフィックを分析します。 |
| [!DNL Target] | [ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)は、訪問者 ID とデータを、アプリケーションをまたいで使用するための、アクションにつながる単一のプロファイルに統合します。 Adobe Analyticsのセグメント作成プロセス中の[!UICONTROL Publish to CX Enterprise] チェックボックスを使用すると、セグメントをAdobe Targetのカスタムオーディエンスライブラリ内で利用できます。 [!DNL Analytics] または [!DNL Audience Manager] で作成されたセグメントは、[!DNL Target] のアクティビティで使用できます。 例えば、[!DNL Analytics] コンバージョン指標および [!DNL Analytics] で作成されたオーディエンスセグメントに基づいてキャンペーンアクティビティを作成できます。 |
| [!DNL Audience Manager] | 共有オーディエンスは、[!DNL Audience Manager] でのセグメント化に使用できます。 すべてのCX Enterprise オーディエンスは[!DNL Audience Manager]でネイティブに利用できます。これにより、次の機能が提供されます。<ul><li>アプリケーションワークフローでの共有および利用に関するビルトインの自動処理</li><li>他ツールとのデータ連携</li><li>類似モデリング</li></ul> |
| Campaign | <ul><li>様々なAdobe CX Enterprise アプリケーションからAdobe Campaignに共有オーディエンスを読み込みます。</li><li>共有オーディエンスの形式で受信者リストを書き出す。 これらの共有オーディエンスは、使用するさまざまなAdobe CX Enterprise アプリケーションで使用できます。</li></ul> |
| Advertising Cloud | オーディエンスをターゲットとして使用します。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>訪問者が Analytics から共有されるオーディエンスの資格を得てから、その情報が [!DNL Target]、Ad Cloud および Campaign Standard で対応可能になるまでに、4～8 時間の遅延があります。

## オーディエンスライブラリのインターフェイス要素

[!DNL CX Enterprise]は、ネイティブでリアルタイムのオーディエンス識別を使用して、オーディエンスを作成および管理するためのライブラリを提供します。

**[!UICONTROL CX Enterprise]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Audience Library]**

![オーディエンスライブラリにオーディエンスを追加](assets/audience_library.png)


| 要素 | 説明 |
| --- | --- |
| 新規 | [オーディエンスを作成](https://experienceleague.adobe.com/ja/docs/core-services/interface/services/audiences/create)します。 |
| タイトルと説明 | オーディエンスを識別および説明する列見出し。 |
| 作成者 | オーディエンスセグメントを作成したユーザー。 |
| ソース | オーディエンスが作成された場所を示します。<ul><li>**Analytics:** Adobe Analyticsで作成されたセグメントが、CX Enterpriseに公開されます。</li><li>**CX Enterprise:**&#x200B;新しいオーディエンス [がCX Enterprise Audiences](https://experienceleague.adobe.com/ja/docs/core-services/interface/services/audiences/create)で作成されました。</li><li>Audience Managerを作成した&#x200B;**Audience Manager:**&#x200B;個のオーディエンスは、CX Enterprise Audiencesに自動的に表示されます。</li></ul> |
| 現在のサイズ | 現在のオーディエンスのサイズ。 |
| アクティブ | セグメントのアクティブステータス。 |

{style="table-layout:auto"}

## Adobe Analyticsからのオーディエンスの公開

詳しくは、Adobe Analytics ドキュメントの[CX Enterpriseへのセグメントの公開](https://experienceleague.adobe.com/ja/docs/analytics/components/segmentation/segmentation-workflow/seg-publish)を参照してください。
