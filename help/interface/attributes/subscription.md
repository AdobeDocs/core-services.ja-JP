---
description: ソリューションのデータソースと購読の設定について説明します。 購読を使用すると、Experience Cloudとソリューション(Analyticsとターゲット)の間で顧客属性データをやり取りできます。
keywords: Customer Attributes;core services
seo-description: ソリューションのデータソースと購読の設定について説明します。 購読を使用すると、Experience Cloudとソリューション(Analyticsとターゲット)の間で顧客属性データをやり取りできます。
seo-title: サブスクリプションの設定
solution: Experience Cloud
title: サブスクリプションの設定
uuid: f74a8155-0a21-46b3-9b1e-4c838f72f24f
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# サブスクリプションの設定

ソリューションのデータソースと購読の設定について説明します。 購読を使用すると、Experience Cloudとソリューション(Analyticsと [!DNL Target])の間で顧客属性データを受け渡すことができます。

例えば、Adobe Analytics購読がレポートで属性データを有効にしたとします。 アドビのターゲットを使用する場合は、ターゲティングとセグメント化のために顧客属性をアップロードできます。

**[!UICONTROL 顧客属性ソース]** / **[!UICONTROL 新規顧客属性ソースを]** 作成 **[!UICONTROL /新規]**

![](assets/configure_subscription_page.png)

| 要素 | 説明 |
|--- |--- |
| ソリューション | **Adobe Analytics **<br>「Analytics」を選択し、属性データを受け取るレポートスイートおよび含める属性を指定します。<br>**Adobe**<br>Targetターゲティングとセグメント化のために顧客属性をアップロードできます。 この機能は、属性データに基づいてテストのターゲットを設定する場合、または Analytics でのセグメント化でデータを使用できるようにする場合に便利です。<br>訪問者のアップロード済み顧客属性データは、ログイン時に、**[!DNL Target]**/**&#x200B;オーディエンスで使用できます&#x200B;**。<br>複数のデータソースがサポートされています。When you[set customer IDs](../core-services/core-services.md)on your website, verify that at least one of the aliases is subscribed to[!DNL Target]. |
| レポートスイート（Analytics） | Analytics のレポートスイート。<br>1 つの属性ソース内で Analytics の購読に追加できるレポートスイートの合計は最大 10 です。含めるレポートスイートを選択する際は、以下の推奨事項を考慮してください。<ul><li>認証済みの共通の顧客セットを持つレポートスイートを選択します。 あるレポートスイートの認証済み顧客が別のレポートスイートの認証済み顧客と重複しない場合は、これらのレポートスイートを異なる属性ソースに分けます。</li><li>可能であれば、属性ソースに含まれるレポートスイートは、トラフィック量が同じである必要があります。</li></ul><br>認証済みの共通の顧客セットを持つレポートスイートが 10 以上ある場合は、追加の顧客属性ソースを設定して、それぞれを最大 10 レポートスイートにすることができます。 |
| 含める属性 (Analyticsおよび [!DNL Target]) | ソリューションに送信する属性。 <br>購読を設定して属性を選択する場合、所有するソリューションに _応じて、レポートスイート_ ごとに次の制限が適用されます。<ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：レポートスイートあたり 200 件</li><li>[!DNL Target] 標準： 5</li><li>[!DNL Target] プレミアム： 200</li></ul><br>**注意：**Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |
