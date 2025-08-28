---
title: ' [!DNL Customer Attributes] について'
description: Experience Cloud の  [!DNL Customer Attributes]  について説明します。Adobe Analytics と Adobe Target で使用する顧客属性データのアップロード方法について説明します。
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: bd718358c6db1ea4a6150d019773072418b629f9
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 80%

---

# Experience Cloud の [!DNL Customer Attributes]

**[!UICONTROL アプリ]** ![ メニュー ](assets/menu-icon.png) > **[!DNL Customer Attributes]**

Experience Cloud で [!DNL Customer Attributes] を使用すると、顧客関係管理（CRM）データベースから取り込んだ企業データをアップロードできます。Experience Cloud内の [ データソースに ](t-crs-usecase.md) データをアップロード [!DNL Customer Attributes] した後、[!DNL Adobe Analytics] および [!DNL Adobe Target] でそのデータを使用できます。

![顧客属性の概要](assets/custom_reports.png)

## 企業顧客データとは  {#enterprise_data}

企業データは様々なシステムに分散されています。企業データは複雑で、そのデータが持つ意味は人によって異なることがあります。このデータには、メンバーシップ、ロイヤルティ、年齢、性別、所有する製品、興味、ライフタイム値などの情報が含まれます。

次に示すのは、製品の購読者データを示すデータファイルの例です。このデータには、メンバー ID、権利が付与されている製品、市場で最も多く発売されている製品などの情報が含まれています。

![企業顧客データとは ](assets/01_crs_usecase.png)

データファイルを作成したら、**[!UICONTROL Experience Cloud]**/**[!UICONTROL 顧客属性]** で作成する顧客属性ソースにアップロードできます。

このワークフローについては、[ 顧客属性データのアップロード ](t-crs-usecase.md) を参照してください。

## Analytics と Target における顧客属性の例 {#examples}

データを Experience Cloud にアップロードした後は、そのデータをカスタマイズし、レポート、セグメント化、アクティビティおよびキャンペーンで利用するソリューションで共有できます。

以下に例を示します。

| ソリューション | メリットと使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを把握できます。<ul><li>ゴールドレベルの顧客に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索している製品と、プラチナレベルの顧客が検索している製品の違い。</li><li>サイトを再設計すると、古い顧客のコンバージョン率が向上するか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある製品です。</li></ul> |
| Adobe Target | Adobe Target ユーザーは、属性データを利用して次のことができます。<ul><li>ロイヤルティクラブメンバー専用の特別割引とオファーを表示する。</li><li>高級志向の顧客により高価な製品を勧める。</li><li>既にメールを受け取っている顧客に対し、通常はメールのサインアップ用に確保されているスペースにアップセルのオファーを表示する。</li></ul> |

{style="table-layout:auto"}
