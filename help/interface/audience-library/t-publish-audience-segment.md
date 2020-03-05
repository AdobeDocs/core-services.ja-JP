---
title: Analytics オーディエンスセグメントの公開
description: オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。
translation-type: tm+mt
source-git-commit: 83e70059c9b7c0ef606b14d145b450481ba5c38c

---


# Analytics オーディエンスセグメントの公開

オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。

手順については、 [Adobe Analyticsのドキュメントを参照](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-publish.html) してください。

<!-->1.  In Analytics, [build a segment](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html).
1. セグメントビルダーで、「**[!UICONTROL このセグメントを Experience Cloud に公開します]**」オプションを有効にします。

   ![](assets/ec_audience_example.png)

   | 要素 | 説明 |
   |--- |---|
   | このセグメントを　Experience Cloud　（&lt;レポートスイート名> 用）に公開します。 | このセグメントを Experience Cloud に公開します。Adobe Target、Audience Manager、Advertising Cloud、Campaign、および Audience Analytics.でオーディエンスをマーケティングおよびセグメント化アクティビティに使用できます。<br>公開するためには、「タイトル」および「説明」フィールドが必須です。<br>このオプションを有効にすると、タイトルとオーディエンスセグメントの定義は共有されますが、実際のデータは共有されません。そのオーディエンスが Target のアクティビティに関連付けられている場合、Analytics は、その Experience Cloud および Target オーディエンスに振り分けられた訪問者の ID を送信し始めます。その時点で、オーディエンス名と対応するデータが Experience Cloud オーディエンスページに表示され始めます。<br>Analytics から Experience Cloud に共有するオーディエンスのオーディエンスメンバーの数が 2,000 万を超えてはなりません。<br>キャッシュの影響により、Analytics で削除したレポートスイートが Experience Cloud に反映されるまで 12 時間かかります。<br>Experience Cloud に公開されているセグメントを削除するには、まず非公開にする必要があります。セグメントを非公開にするには、公開するために使用したチェックボックスの&#x200B;**チェックを解除**&#x200B;します。次のいずれかのアドビソリューションで現在使用中のセグメントの公開を取り消すことは&#x200B;**できません**：[!DNL Analytics]（[!DNL Audience Analytics]の場合）、[!DNL Campaign]、[!DNL Advertising Cloud]（[!DNL Core Service]および[!DNL Audience Manager] の顧客の場合）、およびその他すべての外部パートナー（[!DNL Audience Manager] の顧客の場合）。[!DNL Target] で使用中のセグメントを非公開にすることが&#x200B;**できます**。<br>訪問者が Analytics から共有されるオーディエンスの資格を得てから、その情報が Target、Advertising Cloud および Campaign で対応可能になるまでに、24～48 時間の遅延があります。<br>**データプライバシー&#x200B;**<br>オーディエンスは、訪問者の認証状態に基づいてフィルタリングされません。訪問者が未認証状態および認証状態でサイトを閲覧できる場合、訪問者が未認証のときに生じるアクションによって、訪問者がオーディエンスに含められる可能性があります。[Analytics のプライバシーの概要](https://docs.adobe.com/help/en/analytics/technotes/privacy-overview.html)を確認して、オーディエンス共有にプライバシーが与える大きな影響を理解してください。 |
   | オーディエンス作成用のウィンドウを選択してください | これは、固定ではなく、**周期的**&#x200B;な期間です。 |

1. 「**[!UICONTROL 保存]**」をクリックします。
1. Access [!DNL Adobe Target] にアクセスして、「[!UICONTROL オーディエンス]」をクリックします。
1. [!UICONTROL オーディエンス]ページで、Experience Cloud からのオーディエンスを探します。

   これらのオーディエンスは、アクティビティで使用できます。&lt;-->
