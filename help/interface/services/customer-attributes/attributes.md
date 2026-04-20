---
title: ' [!DNL Customer Attributes] について'
description: Adobe CX Enterpriseの [!DNL Customer Attributes] について説明します。 Adobe Analytics と Adobe Target で使用する顧客属性データのアップロード方法について説明します。
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
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 313
ht-degree: 47%

---

# CX Enterpriseの[!DNL Customer Attributes]

**[!UICONTROL Apps]** ![ メニュー](assets/menu-icon.png) > **[!DNL Customer Attributes]**

Adobe CX Enterpriseの[!DNL Customer Attributes]を使用すると、取り込んだエンタープライズ データをCRM （顧客関係管理）データベースからアップロードできます。 データ ](t-crs-usecase.md)を[CX Enterpriseの[!DNL Customer Attributes] データソースにアップロードしてから、[!DNL Adobe Analytics]および[!DNL Adobe Target]でデータを使用できます。

![顧客属性の概要](assets/custom_reports.png)

## エンタープライズ顧客データについて {#customer-data}

エンタープライズ顧客データとは、顧客、見込み顧客、パートナーについて収集された、組織全体の情報セットのことです。他のシステム上に存在し、メンバーシップ、ロイヤルティレベル、年齢、性別、所有している製品、興味、生涯価値などの情報を含めることができます。

次の画像は、_データファイル_&#x200B;の例で、メンバーID、使用権限のある製品、最も起動数の多い製品など、製品の購読者データを示しています。

![企業顧客データとは ](assets/01_crs_usecase.png)

データファイルを作成した後、**[!UICONTROL CX Enterprise]** > **[!UICONTROL Customer Attributes]**&#x200B;で作成した顧客属性ソースにデータファイルをアップロードできます。

このワークフローについて詳しくは、[顧客属性データのアップロード ](t-crs-usecase.md)を参照してください。

## Analytics と Target における顧客属性の例

データをCX Enterpriseに保管した後は、それをカスタマイズして、レポート、セグメンテーション、アクティビティ、キャンペーン用のソリューションと共有できます。

例：

| ソリューション | メリットと使用例 |
| --- | --- |
| Adobe Analytics | マーケターとアナリストは、次のことを把握できます。<ul><li>ゴールドレベルの顧客に最も効果的なオンラインキャンペーン。</li><li>ゴールドレベルの顧客が検索している製品と、プラチナレベルの顧客が検索している製品の違い。</li><li>サイトを再設計すると、古い顧客のコンバージョン率が向上するか。</li><li>ライフタイム値が低い顧客がサイトで調べる傾向にある製品です。</li></ul> |
| Adobe Target | Adobe Target ユーザーは、属性データを利用して次のことができます。<ul><li>ロイヤルティクラブメンバー専用の特別割引とオファーを表示する。</li><li>高級志向の顧客により高価な製品を勧める。</li><li>既にメールを受け取っている顧客に対し、通常はメールのサインアップ用に確保されているスペースにアップセルのオファーを表示する。</li></ul> |

{style="table-layout:auto"}
