---
title: 「[!DNL Customer Attributes]」
description: Experience Cloud の  [!DNL Customer Attributes]  について説明します。Adobe Analytics と Adobe Target で使用する顧客属性データのアップロード方法について説明します。
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 96%

---

# Experience Cloud の [!DNL Customer Attributes]

Experience Cloud で [!DNL Customer Attributes] を使用すると、顧客関係管理（CRM）データベースから取り込んだ企業データをアップロードできます。データを Experience Cloud の顧客属性データソースにアップロードすると、そのデータを [!DNL Adobe Analytics] および [!DNL Adobe Target] で使用できます。

## [!DNL Customer Attributes] の機能を見つけます。

1. Experience Cloud にログインします。

1. **[!DNL Experience Platform]**／**[!UICONTROL ユーザー]**／**[!UICONTROL 顧客属性]**&#x200B;に移動します。

![顧客属性の概要](assets/custom_reports.png)

## [!DNL Customer Attributes] をアップロードするための前提条件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **グループメンバーシップ：** 顧客属性データをアップロードするには、ユーザーが顧客属性グループのメンバーである必要があります。 また、Adobe Analytics グループまたは Adobe Target グループのいずれかに属している必要もあります。

  自社が顧客属性にアクセスできるかどうかを知るには、[!DNL Experience Cloud] 管理者が、[Experience Cloud](https://experience.adobe.com) にログインする必要があります。**[!UICONTROL 管理]**／**[!UICONTROL Admin Console]**／**[!UICONTROL グループ]**&#x200B;に移動します。*[!DNL Customer Attributes]* が[!UICONTROL 製品プロファイル]の 1 つとして表示されている場合は、開始する準備が整っています。

  [!DNL Customer Attributes] に追加されたユーザーには、Experience Cloud インターフェイスの左側に[!UICONTROL 顧客属性]メニュー項目が表示されます。

* 顧客属性には、**Adobe Target** `at.js`（任意のバージョン）または `mbox.js` バージョン 58 以降が必要です。

  [at.js のデプロイ方法](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=ja)を参照してください。

## 企業顧客データとは  {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業データは様々なシステムに分散されています。企業データは複雑で、そのデータが持つ意味は人によって異なることがあります。このデータには、メンバーシップ、忠誠度、年齢、性別、所有する製品、興味、ライフタイム値などの情報が含まれます。

次に示すのは、製品の購読者データを示すデータファイルの例です。このデータには、メンバー ID、権利が付与されている製品、市場で最も多く発売されている製品などの情報が含まれています。

![企業顧客データとは ](assets/01_crs_usecase.png)

データファイルを作成したら、**[!UICONTROL Experience Cloud]**／**[!UICONTROL 顧客属性]**&#x200B;で作成する顧客属性ソースにアップロードできます。

このワークフローについては、[顧客属性データのアップロード](t-crs-usecase.md)を参照してください。

## Analytics と Target における顧客属性の例 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

データを Experience Cloud にアップロードした後は、そのデータをカスタマイズし、レポート、セグメント化、アクティビティおよびキャンペーンで利用するソリューションで共有できます。

以下に例を示します。

| ソリューション | メリットと使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを把握できます。<ul><li>ゴールドレベルの顧客に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索している製品と、プラチナレベルの顧客が検索している製品の違い。</li><li>サイトを再設計すると、古い顧客のコンバージョン率が向上するか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある製品です。</li></ul> |
| Adobe Target | Adobe Target ユーザーは、属性データを利用して次のことができます。<ul><li>ロイヤルティクラブメンバー専用の特別割引とオファーを表示する。</li><li>高級志向の顧客により高価な製品を勧める。</li><li>既にメールを受け取っている顧客に対し、通常はメールのサインアップ用に確保されているスペースにアップセルのオファーを表示する。</li></ul> |

{style="table-layout:auto"}
