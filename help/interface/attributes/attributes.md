---
description: Adobe Experience CloudのCustomer Attributesサービスと、分析およびターゲットで使用するデータをアップロードする方法について説明します。
keywords: core services;Customer Attributes; Adobe Experience Cloud; Analytics; Target
solution: Experience Cloud
title: '顧客属性の使用方法 '
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 79%

---


# Adobe Experience Cloudでの顧客属性の使用方法

Adobe Experience Cloudの顧客属性を使用すると、顧客関係管理(CRM)データベースから取り込んだ企業データをアップロードできます。 データをExperience Cloud内の顧客属性データソースにアップロードし、そのデータをAdobe AnalyticsおよびAdobe Targetで使用できます。

To locate this feature, navigate to **[!DNL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**

![](assets/custom_reports.png)

## 顧客属性をアップロードするための前提条件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **ソリューションのイネーブルメント：**[ソリューションを Experience Platform サービスに対応させます](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **グループのメンバーシップ：**&#x200B;顧客属性データをアップロードするには、ユーザーは、[顧客属性グループ](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)のメンバーである必要があります。また、Adobe Analytics グループまたは Adobe Target グループのいずれかに属している必要もあります。

   自社が顧客属性にアクセスできるかどうかを知るには、[!DNL Experience Cloud] 管理者が、[Experience Cloud](https://experience.adobe.com) にログインする必要があります。**[!UICONTROL 管理]**／**[!UICONTROL Admin Console]**／**[!UICONTROL グループ]**&#x200B;に移動します。[!UICONTROL 製品プロファイル]の 1 つとして&#x200B;*顧客属性*&#x200B;がある場合は、すぐに始めることができます。

   顧客属性に追加されたユーザーには、Experience Cloud インターフェイスの左側に「[!UICONTROL 顧客属性]」メニュー項目が表示されます。

* 顧客属性には、**Adobe Target** `at.js`（任意のバージョン）または `mbox.js` バージョン 58 以降が必要です。

   [at.js のデプロイ方法](https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html)または [mbox.js の実装](https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/mbox-implement/mbox-download.html)を参照してください。

## 企業顧客データとは {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業データは様々なシステムに分散されています。企業データは複雑で、そのデータが持つ意味は人によって異なることがあります。このデータには、メンバーシップ、忠誠度、年齢、性別、所有する製品、興味、ライフタイム値などの情報が含まれます。

次に示すのは、製品の購読者データを示すデータファイルの例です。このデータには、メンバー ID、権利が付与されている製品、市場で最も多く発売されている製品などの情報が含まれています。

![](assets/01_crs_usecase.png)

作成したデータファイルは、**[!UICONTROL Experience Cloud]**／**[!UICONTROL 顧客属性]**&#x200B;を選択して作成する顧客属性ソースにアップロードできます。

このワークフローについては、[顧客属性データのアップロード](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)を参照してください。

## Analyticsとターゲットにおける顧客属性の例 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

データを Experience Cloud にアップロードした後は、そのデータをカスタマイズし、レポート、セグメント化、アクティビティおよびキャンペーンで利用するためにソリューションで共有できます。

以下に例を示します。

| ソリューション | メリットと使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを把握できます。<ul><li>ゴールドレベルの顧客に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索している製品と、プラチナレベルの顧客が検索している製品の違い。</li><li>サイトを再設計すると、古い顧客のコンバージョン率が向上するか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある製品は何か。</li></ul> |
| Adobe Target | Adobe Target ユーザーは、属性データを利用して次のことができます。<ul><li>ロイヤルティクラブメンバー専用の特別割引とオファーを表示する。</li><li>高級志向の顧客により高価な製品を勧める。</li><li>既に E メールを受け取っている顧客に対し、通常は E メールのサインアップ用に確保されているスペースにアップセルのオファーを表示する。</li></ul> |
