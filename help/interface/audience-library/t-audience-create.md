---
description: Experience Cloud で属性ルールを使用して、オーディエンスを作成し、複合オーディエンスを定義する方法について説明します。
keywords: コアサービス
seo-description: Experience Cloud で属性ルールを使用して、オーディエンスを作成し、複合オーディエンスを定義する方法について説明します。
seo-title: オーディエンスの作成
solution: Experience Cloud
title: オーディエンスの作成
uuid: 7e622539-296e-4ff3-93b0- ec1c08b35429
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# オーディエンスの作成

Experience Cloud で属性ルールを使用して、オーディエンスを作成し、複合オーディエンスを定義する方法について説明します。

この記事では、以下の方法について説明します。

* オーディエンスの作成
* ルールの作成
* ルールを使用した複合オーディエンスの定義


下の図は、複合オーディエンスの 2 つのルールを表しています。

![](assets/audience_sharing.png)

それぞれの円が、オーディエンスのメンバーシップを定義するルールを表します。重なっている両方のオーディエンスルールのメンバーと認定される訪問者が、複合オーディエンスとして定義されます。

>[!NOTE]
>
>オーディエンスは、指定した期間のデータ収集後に完全に定義されます。
次の例は、複合オーディエンスのルールを作成する方法を示したものです。このオーディエンスは、次のもので構成されます。

* ページデータまたは Analytics の生データから得られる Home &amp; Garden セクション
* に公開された [!DNL Adobe Analytics] セグメント [から派生したChromeおよびSafari](../audience-library/audience-library.md#task_32FEEFE0B32E4E388CD4D892D727282A) ユーザー [!DNL Experience Cloud]。


   ![](assets/audience_create.png)

1. で [!DNL Experience Cloud]**[!UICONTROL 、人物]** / **[!UICONTROL オーディエンスライブラリ]** をクリックします。
1. [!UICONTROL オーディエンス] ページで、 **[!UICONTROL 「新規]**」をクリックします。 ![](assets/add_icon_small.png)

![Step Result](assets/audience_create_new.png)

1. [!UICONTROL 新しいオーディエンスを作成]ページで、タイトルと説明を指定します。
1. 「[!UICONTROL ルール]」で、属性のソースを選択します。

* **[!UICONTROL リアルタイム Analytics データ：]**（生データ）リアルタイムの Analytics イメージリクエストから得られる属性データであり、eVar やイベントなどのデータが含まれます。この属性ソースを使用する場合は、レポートスイートを選択し、含めるディメンションまたはイベントを定義する必要があります。このレポートスイートの選択により、レポートスイートで使用された変数構造が提供されます。

   >[!NOTE]
   >
   >キャッシュにより、Analyticsで削除されたレポートスイートは、削除がExperience Cloudに表示されるまで12時間かかります。

* **[!UICONTROL Experience Cloud:]**[!DNL Experience Cloud] ソースから派生する属性データ。例えば、[!DNL Analytics] で作成したオーディエンスセグメントからのデータや、[!DNL Audience Manager] からのデータです。

1. オーディエンスルールを定義します。

>[!NOTE]
>
>オーディエンスルールを定義する際には、実装変数を理解する必要があります。

[!UICONTROL 「ルール]」で *`Home & Garden`* 、属性の選択を次のように定義します。

* **[!UICONTROL 属性のソース：]** Analytics 生データ
* **[!UICONTROL レポートスイート：]** レポートスイート 31
* Dimension= **[!UICONTROL Store（Merch）（v6）]** &gt; **[!UICONTROL Equals]** &gt; **[!UICONTROL Home&amp; Garden]**

   ![](assets/home_garden.png)

   *ChromeおよびSafariの訪問者* は、Analyticsから共有されたオーディエンスセグメントです。

* **[!UICONTROL 属性のソース：]** Experience Cloud
* **[!UICONTROL ディメンション：]** Chrome &amp; Safari Visitors

   ![](assets/chrome_safari.png)

   比較する場合、 *&quot;OR* 」ルールを追加して、「テラスと家具」などのサイトセクションへのすべての訪問者を表示できます。

   ![](assets/audiences_rule_patio.png)

1. 結果を表示します。

このルールの結果として得られるのは、Home &amp; Garden を訪問した Chrome および Safari ユーザーで構成される、定義されたオーディエンスです。「Patio &amp; Furniture」セグメントにより、このサイトセクションに訪問するすべての訪問者に対する追加のインサイトが得られます。

![](assets/defined_audience.png)

**履歴による予測：**（点線の円）[!DNL Analytics] データに基づいて作成されたルールを表しています。

**実際のオーディエンス：**（実線の円）Audience Manager からの 30 日間のデータで作成されたルールです。Audience Manager データが 30 日に達すると、線が実線になり、実際の数を表します。

特定期間のデータ収集が終了すると、円は結合されて、定義されたオーディエンスを表示します。

1. ルールを定義したら **[!UICONTROL 、「保存]**」をクリックします。

オーディエンスを保存すると、他のソリューションで使用できるようになります。例えば、Target のアクティビティに共有オーディエンスを含めることができます。
