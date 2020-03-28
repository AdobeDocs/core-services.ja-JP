---
description: Experience Cloud への顧客属性のアップロードの概要とそのための前提条件に関する情報です。
keywords: core services;customer attributes
seo-description: Experience Cloud への顧客属性のアップロードの概要とそのための前提条件に関する情報です。
seo-title: 顧客属性
solution: Experience Cloud
title: 顧客属性
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# 顧客属性

To locate [!UICONTROL customer attributes] navigate to **[!DNL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

![](assets/custom_reports.png)

## 顧客属性をアップロードするための前提条件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **ソリューションの有効化：** [コアサービス向けにソリューションを有効化](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)します。

* **グループのメンバーシップ：**&#x200B;顧客属性データをアップロードするには、ユーザーは、 顧客属 [性グループ](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。 また、Adobe AnalyticsグループまたはAdobeターゲットグループに属している。

   自社が顧客属性にアクセスできるかどうかを知るには、 [!DNL Experience Cloud] 管理者が、[!DNL Experience Cloud] にログインする必要があります。Navigate to **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]** > **[!UICONTROL Groups]**. グループの 1 つとして&#x200B;*顧客属性*&#x200B;がある場合は、すぐに始めることができます。

   顧客属性グループに追加されたユーザーには、Experience Cloud インターフェイスの左側に[!UICONTROL 顧客属性]メニュー項目が表示されます。

* **顧客属性には** 、Adobeターゲット [!DNL at.js] (任意のバー [!DNL mbox.js] ジョン)またはバージョン58以降が必要です。

   at.js [または](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html) Mbox.js実装のデプロイ方法を参照してください [](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mbox-download.html)。

## What is enterprise customer data? {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業データは他のシステムに存在します。 複雑で、人によって意味が異なる場合もあります。 このデータには、メンバーシップ、忠誠度、年齢、性別、所有する製品、興味、ライフタイム値などの情報が含まれます。

次の図は、メンバーID、権利付与済み製品、最も頻繁に起動する製品など、製品の購読者データを示すデータファイルの例です。

![](assets/01_crs_usecase.png)

After you create the data file, you can upload it to the customer attribute source that you create in **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**.

このワークフローについては、[顧客属性データのアップロード](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)を参照してください。

## ソリューションの使用例 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

データがExperience Cloudに保存されたら、そのデータをカスタマイズして、レポート、セグメント化、アクティビティおよびキャンペーンのソリューションと共有できます。

以下に例を示します。

| ソリューション | 利点と使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを理解できます。<ul><li>ゴールドキャンペーンに最も効果的なオンライン顧客。</li><li>ゴールドレベルの顧客が検索する製品と、プラチナレベルの顧客が検索する製品。</li><li>サイトの再設計が、古い顧客のコンバージョン率に良い影響を及ぼしているか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある商品はどれか。</li></ul> |
| Adobe Target | 属性データを使用すると、アドビのターゲットユーザーは次のことができます。<ul><li>ロイヤルティクラブメンバーに特別割引とオファーを表示</li><li>高級顧客に対して、より高価な商品をレコメンデーションします。</li><li>既に電子メールを受け取っている顧客の場合、通常は電子メールのサインアップ用に予約されているスペースにアップセルオファーを表示します。</li></ul> |
