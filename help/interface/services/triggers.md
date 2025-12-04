---
description: Experience Cloudのトリガー方法について説明します。
solution: Experience Cloud
title: Triggers の概要
uuid: dab536e3-1969-4661-919e-5b15f423fecd
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 9dc26e2f-479b-49a5-93ce-b877559fea43
source-git-commit: e63dd988abba199049da2b3620eed9ebf51043d1
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 75%

---

# Experience Cloud Triggers

Experience Cloudの [!UICONTROL Triggers] を使用すると、主要なコンシューマーの行動を特定、定義、監視し、アプリケーション間のコミュニケーションを生み出して、訪問者を再び引き付けることができます。 リアルタイムでの意思決定とパーソナライゼーションに Triggers を使用できます。

以下に例を示します。

* 買い物かごに製品を追加後に放棄、または製品を削除して買い物かごを放棄した利用者への迅速なリマーケティングの設定
* 入力に不備のあるフォームや申請
* オンサイトでの任意のアクションまたは一連のアクション

![トリガー例](../assets/trigger-abandonment-2.png)

>[!NOTE]
>
>[!UICONTROL Triggers] の使用について詳しくは、[Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html) を参照してください。

## トリガーのタイプ

一般に、トリガーがマーケティングキャンペーンを起動するには 15～90 分かかることがあります。このディレイは、データ収集の実装、パイプラインへの読み込み、定義済みトリガーのカスタム設定、Adobe Campaign のワークフローによって異なります。

* **放棄：**&#x200B;訪問者が製品を表示したが買い物かごに何も追加しない場合に実行するトリガーを作成できます。
* **アクション：**&#x200B;例えば、ニュースレターのサインアップ、電子メールの購読またはクレジットカードの申請（確認）の後に実行するトリガーを作成できます。小売業者の場合、ロイヤルティプログラムにサインアップする訪問者用のトリガーを作成できます。メディアおよびエンターテインメントでは、特定のショーを観て、調査に回答したいと思われる訪問者用のトリガーを作成できます。
* **セッション開始およびセッション終了：**&#x200B;セッション開始およびセッション終了イベントのトリガーを作成します。

## Experience Cloud のトリガーの作成

トリガーを作成し、トリガーの条件を設定します。例えば、買い物かごの放棄のような指標や製品名のようなディメンションなど、訪問中のトリガーのルールに対する条件を指定できます。ルールを満たすと、トリガーが実行されます。

>[!NOTE]
>
>現在、100 トリガーまでという技術的な制限があります。

1. Experience Cloudで、「![menu](../assets/menu-icon.png)」をクリックし、「**[!UICONTROL Data Collection/Launch]**」をクリックします。
1. [!UICONTROL Triggers] カードで、[**[!UICONTROL Manage Triggers]**] をクリックします。
1. 「**[!UICONTROL New Trigger]**」をクリックして、トリガーの種類を指定します。

   ![手順の結果](../assets/add-trigger.png)

1. 次のフィールドに入力し、指標およびディメンション項目をルールのコンテナにドラッグすることで、トリガーを設定します。

   | 要素 | 説明 |
   |--- |--- |
   | [!UICONTROL Name] | このトリガーのわかりやすい名前。 |
   | [!UICONTROL Description] | このトリガーの説明、使い方など。 |
   | [!UICONTROL Report Suite] | このトリガーに使用する Analytics [レポートスイート](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=ja)。この設定は、使用するレポートデータを特定します。 |
   | 訪問には含める必要があります <br> 訪問には、アクションを含めない後の <br>トリガーを含めない <br> メタデータを含める | 条件または発生してほしい訪問者の行動、および発生してほしくない行動を定義できます。例えば、シンプルな買い物かご放棄トリガーのルールは、次のようになります。<ul><li>訪問には [!UICONTROL Cart Addition] （指標）と [!UICONTROL Exists] を含める必要があります。 （特定の製品の表示またはブラウザータイプなどのディメンションでルールをさらに洗練させることができます）。</li><li>訪問には [!UICONTROL Checkout] を含めることはできません。</li><li>次のアクションがなかった後のトリガー：10 分。</li><li>[!UICONTROL Include Meta Data]：訪問者の行動に関連する特定の [!DNL Campaign] ディメンションまたは変数を追加できます。 このフィールドは、Adobe Campaign で適切なリマーケティング電子メールを構築するのに便利です。</li></ul><br> ルールにとって重要な条件に応じて、コンテナ内またはコンテナ間で [!UICONTROL Any]、[!UICONTROL And]、[!UICONTROL Or] の論理を指定できます。 |
   | [!UICONTROL Container] | [!UICONTROL Containers] こに、トリガーを定義するルール、条件またはフィルターを設定し、保存します。 同時にイベントを発生させたい場合、イベントを同じコンテナに配置します。つまり、各コンテナは、ヒットレベルで別々に処理されます。例えば、2 つのコンテナが AND 演算子で結合されている場合、2 つのヒットが要件を満たすタイミングを満たすルールを期待できます。 |
   | この次に新しいセッションを開始 | セッション開始およびセッション終了イベントのトリガーを作成します。 |

   {style="table-layout:auto"}

1. 「**[!UICONTROL Save]**」をクリックします。
1. [!DNL Adobe Campaign] でトリガーを[リアルタイムリマーケティング](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/about-adobe-experience-cloud-triggers.html?lang=ja)に使用します。

## トリガーの例

Experience Cloud Triggers の例を以下に示します。

### 買い物かご放棄トリガー

例えば次のページは、訪問中に表示された商品に基づいて、[!UICONTROL Cart Abandonment]トリガーに使用する可能性のあるルールを示しています。

![買い物かご放棄トリガー](../assets/abandonment-trigger.png)

### リファラートリガー

次のトリガーは、ヒットがメンズブーツの製品および Facebook のリファラーで発生すると実行されます。2 つの条件（*製品*&#x200B;と&#x200B;*リファラー*）が同じヒットで評価されるためには、両方を同じコンテナに追加する必要があります。

![リファラートリガー](../assets/fb-boots-promo.png)

