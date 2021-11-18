---
description: ソリューションのデータソースと、サブスクリプションの設定について説明します。サブスクリプションを設定することで、顧客とExperience Cloud（Analytics と Target）の間で顧客属性データをやり取りできるようになります。
keywords: 顧客属性;コアサービス
application: Experience Cloud
title: 'サブスクリプションの設定方法 '
uuid: f74a8155-0a21-46b3-9b1e-4c838f72f24f
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 81%

---

# Experience Cloud でのサブスクリプションの設定方法

アプリケーションのデータソースと、サブスクリプションの設定について説明します。 サブスクリプションを設定することで、Experience Cloudとアプリケーション ([!DNL Analytics] および [!DNL Target]) をクリックします。

例えば、Adobe Analytics を購読すると、レポート内で属性データが有効になります。Adobe Target を使用している場合は、ターゲティングとセグメント化用に顧客属性をアップロードできます。

**[!UICONTROL 顧客属性ソース]**／**[!UICONTROL 新しい顧客属性ソースを作成]**／**[!UICONTROL 新規]**

![購読のExperience Cloud](assets/configure_subscription_page.png)

| 要素 | 説明 |
|--- |--- |
| ソリューション | **Adobe Analytics**<br> 「Analytics」を選択し、属性データを受け取るレポートスイートおよび含める属性を指定します。<br>**Adobe Target**<br> ターゲティングとセグメント化用に顧客属性をアップロードできます。この機能は、属性データに基づいてテストのターゲットを設定する場合、または Analytics でのセグメント化でデータを使用できるようにする場合に便利です。<br>訪問者のアップロード済み顧客属性データは、**[!DNL Target]**／**Audiences**&#x200B;を選択してログイン時に使用できます。<br>複数のデータソースがサポートされています。Web サイト上で[顧客 ID を設定](core-services.md)する場合は、少なくとも 1 つのエイリアスが [!DNL Target] にサブスクライブされていることを確認します。 |
| レポートスイート（Analytics） | Analytics のレポートスイート。<br>1 つの属性ソース内で Analytics の購読に追加できるレポートスイートの合計は最大 10 です。含めるレポートスイートを選択する際は、以下のアドバイスを考慮してください。<ul><li>認証済みの共通の顧客セットを持つレポートスイートを選択する。あるレポートスイートの認証済み顧客が別のレポートスイートの認証済み顧客と重ならない場合は、これらのレポートスイートを異なる属性ソースに分けてください。</li><li>可能であれば、1 つの属性ソースに含まれるレポートスイートのトラフィック量は同じにする。</li></ul><br>認証済みの共通の顧客セットを持つレポートスイートが 10 以上ある場合は、追加の顧客属性ソースを設定して、それぞれを最大 10 のレポートスイートにすることができます。 |
| 含める属性（Analytics と [!DNL Target]） | アプリケーションに送信する属性。 <br>サブスクリプションを設定し属性を選択する場合、次の制限が適用されます _レポートスイートごと_ 所有するアプリケーションに応じて、次の手順を実行します。<ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：レポートスイートあたり 200 件</li><li>[!DNL Target] Standard：5 件</li><li>[!DNL Target] Premium：200 件</li></ul><br>**注意：** Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |

{style=&quot;table-layout:auto&quot;}
