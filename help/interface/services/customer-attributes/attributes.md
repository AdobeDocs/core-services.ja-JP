---
title: ' [!DNL Customer Attributes] について'
description: Experience Cloud の  [!DNL Customer Attributes]  について説明します。Adobe Analytics と Adobe Target で使用する顧客属性データのアップロード方法について説明します。
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: 27b9b789e0d4c448105f5acec3aa05c9404443bf
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 63%

---

# Experience Cloud の [!DNL Customer Attributes]

**[!UICONTROL Apps]** ![ メニュー ](assets/menu-icon.png) > **[!DNL Customer Attributes]**

Experience Cloud で [!DNL Customer Attributes] を使用すると、顧客関係管理（CRM）データベースから取り込んだ企業データをアップロードできます。Experience Cloud内の [ データソースに ](t-crs-usecase.md) データをアップロード [!DNL Customer Attributes] した後、[!DNL Adobe Analytics] および [!DNL Adobe Target] でそのデータを使用できます。

![顧客属性の概要](assets/custom_reports.png)

## 企業顧客データについて {#customer-data}

企業顧客データは、顧客、見込み客、パートナーに関して収集された組織全体の情報セットを指します。他のシステムに存在し、メンバーシップ、ロイヤルティレベル、年齢、性別、所有されている製品、興味、生涯価値などの情報を含めることができます。

次の図は、メンバー ID、資格のある製品、最も売り上げの多い製品など、製品の購読者データを表示する _データファイル_ の例です。

![企業顧客データとは ](assets/01_crs_usecase.png)

データファイルを作成したら、**[!UICONTROL Experience Cloud]**/**[!UICONTROL Customer Attributes]** で作成する顧客属性ソースにアップロードできます。

このワークフローについては、[ 顧客属性データのアップロード ](t-crs-usecase.md) を参照してください。

## Analytics と Target における顧客属性の例

データを Experience Cloud にアップロードした後は、そのデータをカスタマイズし、レポート、セグメント化、アクティビティおよびキャンペーンで利用するソリューションで共有できます。

以下に例を示します。

| ソリューション | メリットと使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを把握できます。<ul><li>ゴールドレベルの顧客に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索している製品と、プラチナレベルの顧客が検索している製品の違い。</li><li>サイトを再設計すると、古い顧客のコンバージョン率が向上するか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある製品です。</li></ul> |
| Adobe Target | Adobe Target ユーザーは、属性データを利用して次のことができます。<ul><li>ロイヤルティクラブメンバー専用の特別割引とオファーを表示する。</li><li>高級志向の顧客により高価な製品を勧める。</li><li>既にメールを受け取っている顧客に対し、通常はメールのサインアップ用に確保されているスペースにアップセルのオファーを表示する。</li></ul> |

{style="table-layout:auto"}
