---
description: Analytics と Target のサブスクリプションを設定する方法  [!DNL Customer Attributes] 、データソースをアクティブ化する方法について説明します。
solution: Experience Cloud
title: でサブスクリプションを設定する方法  [!DNL Customer Attributes]
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 61%

---

# 購読の設定とデータソースのアクティベート

[!DNL Customer Attributes] サブスクリプションを設定すると、Experience Cloudとアプリケーション（[!DNL Analytics] と [!DNL Target]）の間で顧客属性データをやり取りできるようになります。

例えば、Adobe Analytics を購読すると、レポート内で属性データが有効になります。[!DNL Adobe Target] を使用する場合、ターゲティングおよびセグメント化のために顧客属性をアップロードできます。

**サブスクリプションを設定し、データソースをアクティベートするには**

1. 編集用に [!DNL Customer Attributes] でデータソースを見つけます。

   [!DNL Experience Cloud] で、**[!UICONTROL アプリ]**![ メニュー ](assets/menu-icon.png)/**[!DNL Customer Attributes]** をクリックします。

1. [!UICONTROL  顧客属性Sourceを編集 ] で、「**[!UICONTROL ファイルのアップロード]**」をクリックします。

1. 「**[!UICONTROL 購読を設定]**」をクリックします。

   ![Experience Cloud でのサブスクリプション設定](assets/configure-subscriptions.png)

1. 顧客属性ソースをアクティブにするには、「**[!UICONTROL アクティブ]**」をクリックし、「**[!UICONTROL 保存]**」をクリックします。

1. [!DNL Analytics] または [!DNL Target] のサブスクリプションを構成するには、[**[!UICONTROL 構成]**] をクリックします。

   次に、[!DNL Target] サブスクリプションの例を示します。

   ![手順の結果](assets/subscription-target.png)

   | 要素 | 説明 |
   |--- |--- |
   | ソリューション | **Adobe Analytics**<br> 「[!DNL Analytics]」を選択し、属性データを受け取るレポートスイートと含める属性を指定します。<br>**Adobe Target**<br>&#x200B;ターゲティングとセグメント化用に顧客属性をアップロードできます。この機能は、属性データに基づいてテストのターゲットを設定する場合、または Analytics でのセグメント化でデータを使用できるようにする場合に便利です。<br>訪問者のアップロード済み顧客属性データは、 **[!DNL Target]** ／ **オーディエンス** を選択してログイン時に使用できます。<br>複数のデータソースがサポートされています。Web サイトに顧客 ID を設定する場合は、少なくとも 1 つのエイリアスが [!DNL Target] に登録されていることを確認します。 |
   | レポートスイート（Adobe Analytics） | Analytics のレポートスイート。<br>1 つの属性ソース内で Analytics の購読に追加できるレポートスイートの合計は最大 10 です。含めるレポートスイートを選択する際は、以下のアドバイスを考慮してください。<ul><li>認証済みの共通の顧客セットを持つレポートスイートを選択する。あるレポートスイートの認証済み顧客が別のレポートスイートの認証済み顧客と重ならない場合は、これらのレポートスイートを異なる属性ソースに分けてください。</li><li>可能であれば、1 つの属性ソースに含まれるレポートスイートのトラフィック量は同じにする。</li></ul><br>認証済みの共通の顧客セットを持つレポートスイートが 10 以上ある場合は、追加の顧客属性ソースを設定して、それぞれを最大 10 レポートスイートにすることができます。 |
   | 含める属性（Analytics と [!DNL Target]） | アプリケーションに送信する属性。<br>サブスクリプションを設定し属性を選択する場合、_所有するソリューションに応じて、_&#x200B;レポートスイートごとに次の制限が適用されます。<ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：レポートスイートあたり 200 件</li><li>[!DNL Target] Standard：5 件</li><li>[!DNL Target] Premium：200 件</li></ul><br>**注意：** Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |

1. 「**[!UICONTROL 保存]**」をクリックします。
