---
description: 顧客属性をExperience Cloudにアップロードする際の概要と前提条件を示します。
keywords: core services;Customer Attributes
seo-description: 顧客属性をExperience Cloudにアップロードする際の概要と前提条件を示します。
seo-title: 顧客属性
solution: Experience Cloud
title: 顧客属性
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 75d3d045964aa42f7ac6b32b25cfd77aa7f663a9
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 71%

---


# 顧客属性

/ **[!DNL Experience Platform]** 人/ **[!UICONTROL 顧客属性に移動します]****[!UICONTROL 。]**

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

![](assets/custom_reports.png)

## 顧客属性をアップロードするための前提条件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **ソリューションの有効化：** [エクスペリエンスプラットフォームサービスのソリューションを有効にします](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **グループのメンバーシップ：** 顧客属性データをアップロードするには、ユーザーが [顧客属性グループのメンバーである必要があります](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。 また、Adobe Analytics グループまたは Adobe Target グループのいずれかに属している必要もあります。

   To know whether your company has access to Customer Attributes, your [!DNL Experience Cloud] administrator should log into the [Experience Cloud](https://experience.adobe.com). **[!UICONTROL 管理]** / **[!UICONTROL 管理コンソール]** / ****&#x200B;製品に移動します。 If *Customer Attributes* displays as one of the [!UICONTROL Product Profiles], you are ready to begin.

   Users that are added to the Customer Attributes will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

* **顧客属性には、Adobe Target**[!DNL at.js] （任意のバージョン）または [!DNL mbox.js] version 58以降が必要です。

   [at.js のデプロイ方法](https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html)または [mbox.js の実装](https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/mbox-implement/mbox-download.html)を参照してください。

## 企業顧客データとは {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業データは様々なシステムに分散されています。企業データは複雑で、そのデータが持つ意味は人によって異なることがあります。このデータには、メンバーシップ、忠誠度、年齢、性別、所有する製品、興味、ライフタイム値などの情報が含まれます。

次に示すのは、製品の購読者データを示すデータファイルの例です。このデータには、メンバー ID、権利が付与されている製品、市場で最も多く発売されている製品などの情報が含まれています。

![](assets/01_crs_usecase.png)

作成したデータファイルは、**[!UICONTROL Experience Cloud]**／**[!UICONTROL 顧客属性]**&#x200B;を選択して作成する顧客属性ソースにアップロードできます。

このワークフローについては、[顧客属性データのアップロード](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)を参照してください。

## ソリューションの使用例 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

データを Experience Cloud にアップロードした後は、そのデータをカスタマイズし、レポート、セグメント化、アクティビティおよびキャンペーンで利用するためにソリューションで共有できます。

以下に例を示します。

| ソリューション | メリットと使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを把握できます。<ul><li>ゴールドレベルの顧客に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索している製品と、プラチナレベルの顧客が検索している製品の違い。</li><li>サイトを再設計すると、古い顧客のコンバージョン率が向上するか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある製品は何か。</li></ul> |
| Adobe Target | Adobe Target ユーザーは、属性データを利用して次のことができます。<ul><li>ロイヤルティクラブメンバー専用の特別割引とオファーを表示する。</li><li>高級志向の顧客により高価な製品を勧める。</li><li>既に E メールを受け取っている顧客に対し、通常は E メールのサインアップ用に確保されているスペースにアップセルのオファーを表示する。</li></ul> |
