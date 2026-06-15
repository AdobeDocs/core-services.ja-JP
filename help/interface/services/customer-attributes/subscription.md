---
description: AnalyticsとTargetのサブスクリプションを [!DNL Customer Attributes] で設定する方法と、データソースをアクティブ化する方法について説明します。
solution: Experience Cloud
title: ' [!DNL Customer Attributes]でサブスクリプションを設定する方法'
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
TQID: https://experienceleague.adobe.com/I--LZ-Nqu0VdVAAs8qvv88pZTcaRQ97XiHWXd15WQcE
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 421
ht-degree: 46%

---

# 顧客属性サブスクリプションの設定

[!DNL Customer Attributes] サブスクリプションを使用すると、CX Enterpriseとアプリケーション （[!DNL Analytics]および[!DNL Target]）間の顧客属性データフローが有効になります。

例えば、Adobe Analytics を購読すると、レポート内で属性データが有効になります。 [!DNL Adobe Target]を使用している場合は、ターゲットとセグメント化のために顧客属性をアップロードできます。

**サブスクリプションを設定し、データ ソースをアクティブ化するには**

1. 編集用に[!DNL Customer Attributes]でデータソースを見つけます。

   [!DNL CX Enterprise]で、**[!UICONTROL アプリ]** ![ メニュー](assets/menu-icon.png) > **[!DNL Customer Attributes]**&#x200B;をクリックします。

1. [!UICONTROL 顧客属性を編集Source]で、**[!UICONTROL ファイルアップロード]**&#x200B;をクリックします。

1. 「**[!UICONTROL 購読の設定]**」をクリックします。

   ![CX Enterpriseでのサブスクリプションの設定](assets/configure-subscriptions.png)

1. 顧客属性ソースをアクティブにするには、**[!UICONTROL アクティブ]**&#x200B;をクリックし、**[!UICONTROL 保存]**&#x200B;をクリックします。

1. サブスクリプションを[!DNL Analytics]または[!DNL Target]に設定するには、**[!UICONTROL Configure]**&#x200B;をクリックします。

   次の例は、[!DNL Target] サブスクリプションを示しています。

   ![手順の結果](assets/subscription-target.png)

   | 要素 | 説明 |
   | --- | --- |
   | ソリューション | **Adobe Analytics**<br> 「[!DNL Analytics]」を選択し、属性データを受け取るレポートスイートと、含める属性を指定します。<br>**Adobe Target**<br>&#x200B;ターゲティングとセグメント化用に顧客属性をアップロードできます。 この機能は、属性データに基づいてテストをターゲットにする場合や、データをAnalyticsでセグメント化に利用できるようにする場合に便利です。<br>訪問者用にアップロードされた顧客属性データは、**[!DNL Target]** > **オーディエンス**&#x200B;のログイン時に利用できます。<br>複数のデータソースがサポートされています。 Web サイトで顧客IDを設定する際に、少なくとも1つのエイリアスが[!DNL Target]に登録されていることを確認します。 |
   | レポートスイート（Adobe Analytics） | Analyticsのレポートスイート。<br>1つの属性ソース内のAnalytics サブスクリプションに、合計10個を超えるレポートスイートを追加することはできません。 含めるレポートスイートを選択する際は、以下のアドバイスを考慮してください。<ul><li>認証済みの共通の顧客セットを持つレポートスイートを選択する。 あるレポートスイートの認証済み顧客が別のレポートスイートの認証済み顧客と重ならない場合は、これらのレポートスイートを異なる属性ソースに分けてください。</li><li>可能であれば、1 つの属性ソースに含まれるレポートスイートのトラフィック量は同じにする。</li></ul><br>認証済みの共通の顧客セットを持つレポートスイートが 10 以上ある場合は、追加の顧客属性ソースを設定して、それぞれを最大 10 レポートスイートにすることができます。 |
   | 含める属性（Analytics と [!DNL Target]） | アプリケーションに送信する属性。 <br>サブスクリプションを設定し属性を選択する場合、_所有するソリューションに応じて、_&#x200B;レポートスイートごとに次の制限が適用されます。<ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：レポートスイートあたり 200 件</li><li>[!DNL Target] Standard：5 件</li><li>[!DNL Target] Premium：200 件</li></ul><br>**注意：** Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。 この遅延の間に発行された属性サブスクリプションの最大エラーが表示される場合があります。 |

1. 「**[!UICONTROL 保存]**」をクリックします。
