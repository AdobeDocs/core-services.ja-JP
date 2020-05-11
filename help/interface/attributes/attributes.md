---
description: 顧客属性をExperience Cloudにアップロードする際の概要と前提条件を示します。
keywords: core services;Customer Attributes
seo-description: 顧客属性をExperience Cloudにアップロードする際の概要と前提条件を示します。
seo-title: 顧客属性
solution: Experience Cloud
title: 顧客属性
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 顧客属性

/ **[!DNL Experience Platform]** 人/ **[!UICONTROL 顧客属性に移動します]****[!UICONTROL 。]**

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

![](assets/custom_reports.png)

## 顧客属性をアップロードするための前提条件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **ソリューションの有効化：** [エクスペリエンスプラットフォームサービスのソリューションを有効にします](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **グループのメンバーシップ：**&#x200B;顧客属性データをアップロードするには、ユーザーは、 [Customer Attributesグループ](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。 また、Adobe AnalyticsグループまたはAdobeターゲットグループのいずれかに属している必要があります。

   To know whether your company has access to Customer Attributes, your [!DNL Experience Cloud] administrator should log into the [!DNL Experience Cloud]. **[!UICONTROL 管理]** /管理コンソールを **[!UICONTROL 起動]** / **[!UICONTROL グループに移動します]**。 グループの 1 つとして&#x200B;*顧客属性*&#x200B;がある場合は、すぐに始めることができます。

   顧客属性グループに追加されたユーザーには、Experience Cloud インターフェイスの左側に[!UICONTROL 顧客属性]メニュー項目が表示されます。

* **顧客属性には、Adobeターゲット**[!DNL at.js] （任意のバージョン）または [!DNL mbox.js] バージョン58以降が必要です。

   at.js [または](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html) Mbox.js実装のデプロイ方法を参照してください [](https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/mbox-implement/mbox-download.html)。

## What is enterprise customer data? {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業データは他のシステムに格納されます。 複雑で、人によって意味が異なる場合もあります。 このデータには、メンバーシップ、忠誠度、年齢、性別、所有する製品、興味、ライフタイム値などの情報が含まれます。

次の図は、メンバーID、権利付与済み製品、最も頻繁に起動する製品など、製品の購読者データを示すデータファイルの例です。

![](assets/01_crs_usecase.png)

After you create the data file, you can upload it to the customer attribute source that you create in **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**.

このワークフローについては、[顧客属性データのアップロード](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)を参照してください。

## ソリューションの使用例 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

データがExperience Cloudに保存されたら、そのデータをカスタマイズして、レポート、セグメント化、アクティビティおよびキャンペーン向けのソリューションと共有できます。

以下に例を示します。

| ソリューション | 利点と使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを理解できます。<ul><li>ゴールドレベルのお客様に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索する製品と、プラチナレベルの顧客が検索する製品。</li><li>サイトの再設計が、古い顧客のコンバージョン率に良い影響を与えているか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある商品はどれか。</li></ul> |
| Adobe Target | 属性データを使用すると、アドビターゲットユーザーは次のことができます。<ul><li>ロイヤルティクラブメンバーに特別割引とオファーを表示します。</li><li>高級品を高級品のお客様に勧めます。</li><li>既に電子メールを受信している顧客の場合、通常は電子メールのサインアップ用に確保されている領域にアップセルオファーを表示します。</li></ul> |
