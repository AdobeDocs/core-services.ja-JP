---
title: ' [!DNL Customer Attributes] について'
description: Adobe Experience Cloud [!DNL Customer Attributes]  詳細を説明します。 Adobe Analytics と Adobe Target で使用する顧客属性データのアップロード方法について説明します。
solution: Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
TQID: https://experienceleague.adobe.com/yFspG9mP9PG9KTYJF4V52t15siqJb7a2-eAxU1T60G4
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87id: e43347a8-f2c5-4aa4-8623-6f13875d7e3aid: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 55%

---

# Experience Cloud の [!DNL Customer Attributes]

**[!UICONTROL Apps]** ![ メニュー ](assets/menu-icon.png) > **[!DNL Customer Attributes]**

Adobe Experience Cloudの [!DNL Customer Attributes] を使用すると、顧客関係管理（CRM）データベースから取り込んだ大規模法人データをアップロードできます。 Experience Cloud内の [ データソースに ](t-crs-usecase.md) データをアップロード [!DNL Customer Attributes] した後、[!DNL Adobe Analytics] および [!DNL Adobe Target] でそのデータを使用できます。

![顧客属性の概要](assets/custom_reports.png)

## 企業顧客データについて {#customer-data}

企業顧客データは、顧客、見込み客、パートナーに関して収集された組織全体の情報セットを指します。他のシステムに存在し、メンバーシップ、ロイヤルティレベル、年齢、性別、所有されている製品、興味、生涯価値などの情報を含めることができます。

次の図は、メンバー ID、資格のある製品、最も売り上げの多い製品など、製品の購読者データを表示する _データファイル_ の例です。

![企業顧客データとは ](assets/01_crs_usecase.png)

データファイルを作成したら、**[!UICONTROL Experience Cloud]**/**[!UICONTROL Customer Attributes]** で作成する顧客属性ソースにアップロードできます。

このワークフローについては、[ 顧客属性データのアップロード ](t-crs-usecase.md) を参照してください。

## Analytics と Target における顧客属性の例

データを Experience Cloud にアップロードした後は、そのデータをカスタマイズし、レポート、セグメント化、アクティビティおよびキャンペーンで利用するソリューションで共有できます。

例：

| ソリューション | メリットと使用例 |
|--- |--- |
| Adobe Analytics | マーケターとアナリストは、次のことを把握できます。<ul><li>ゴールドレベルの顧客に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索している製品と、プラチナレベルの顧客が検索している製品の違い。</li><li>サイトを再設計すると、古い顧客のコンバージョン率が向上するか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある製品です。</li></ul> |
| Adobe Target | Adobe Target ユーザーは、属性データを利用して次のことができます。<ul><li>ロイヤルティクラブメンバー専用の特別割引とオファーを表示する。</li><li>高級志向の顧客により高価な製品を勧める。</li><li>既にメールを受け取っている顧客に対し、通常はメールのサインアップ用に確保されているスペースにアップセルのオファーを表示する。</li></ul> |

{style="table-layout:auto"}
