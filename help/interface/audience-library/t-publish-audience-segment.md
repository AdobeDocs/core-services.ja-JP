---
description: オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。
keywords: コアサービス
seo-description: オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。
seo-title: Analytics オーディエンスセグメントの公開
solution: Experience Cloud
title: Analytics オーディエンスセグメントの公開
uuid: 4201dc22-4b79-457c-a614-949bba087617
translation-type: tm+mt
source-git-commit: b74e0a08b43dfa8e5b35c5a650d159a58485883c

---


# Analytics オーディエンスセグメントの公開

オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。

1. Analytics で[セグメントを構築](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html)します。
1. On the Segment Builder, enable the **[!UICONTROL Publish this segment to the Experience Cloud]** option.

   ![](assets/ec_audience_example.png)

   | 要素 | 説明 |
   |--- |---|
   | このセグメントをExperience Cloudに公開します（&lt; report suite name&gt;）。 | このセグメントを Experience Cloud に公開します。Adobe Target、Audience Manager、Advertising Cloud、CampaignおよびAudience Analyticsのマーケティングおよびセグメント化アクティビティでオーディエンスを使用できます。<br>公開するためには、「タイトル」および「説明」フィールドが必須です。<br>このオプションを有効にすると、タイトルとオーディエンスセグメントの定義は共有されますが、実際のデータは共有されません。そのオーディエンスが Target のアクティビティに関連付けられている場合、Analytics は、その Experience Cloud および Target オーディエンスに振り分けられた訪問者の ID を送信し始めます。その時点で、オーディエンス名と対応するデータが Experience Cloud オーディエンスページに表示され始めます。<br>Analytics から Experience Cloud に共有するオーディエンスのオーディエンスメンバーの数が 2,000 万を超えてはなりません。<br>キャッシュの影響により、Analytics で削除したレポートスイートが Experience Cloud に反映されるまで 12 時間かかります。<br>Experience Cloudに公開されているセグメントを削除するには、まず公開を取り消す必要があります。To unpublish a segment, just **unclick** the checkbox that you used to publish it. You **cannot** unpublish a segment that is currently in use by any of the following Adobe solutions: [!DNL Analytics] (in [!DNL Audience Analytics]), [!DNL Campaign], [!DNL Advertising Cloud] (for [!DNL Core Service] &amp; [!DNL Audience Manager] customers) and all other external partners (for [!DNL Audience Manager] customers). You **can** unpublish a segment that is in use by [!DNL Target].<br>訪問者が Analytics から共有されるオーディエンスの資格を得てから、その情報が Target、Advertising Cloud および Campaign で対応可能になるまでに、24～48 時間の遅延があります。<br>**データプライバシー**<br>オーディエンスは、訪問者の認証状態に基づいてフィルタリングされません。訪問者が未認証状態および認証状態でサイトを閲覧できる場合、訪問者が未認証のときに生じるアクションによって、訪問者がオーディエンスに含められる可能性があります。[Analytics のプライバシーの概要](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_Privacy_Overview)を確認して、オーディエンス共有にプライバシーが与える大きな影響を理解してください。 |
   | オーディエンス作成用のウィンドウを選択してください | これは、固定ではなく、**周期的**&#x200B;な期間です。 |

1. 「**[!UICONTROL 保存]**」をクリックします。
1. Access [!DNL Adobe Target] にアクセスして、「[!UICONTROL オーディエンス]」をクリックします。
1. [!UICONTROL オーディエンス]ページで、Experience Cloud からのオーディエンスを探します。

   これらのオーディエンスは、アクティビティで使用できます。
