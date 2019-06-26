---
description: オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。
keywords: コアサービス
seo-description: オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。
seo-title: Analytics オーディエンスセグメントの公開
solution: Experience Cloud
title: Analytics オーディエンスセグメントの公開
uuid: 4201dc22-4b79-457c-a614-949bba087617
translation-type: ht
source-git-commit: 85879d92104d8b6d739fb4d17dc8cfb7483a9343

---


# Analytics オーディエンスセグメントの公開

オーディエンスマーケティングアクティビティ用に、Analytics オーディエンスセグメントを Experience Cloud と Adobe Target に公開します。

1. Analytics で、[セグメントを作成](https://marketing.adobe.com/resources/help/ja_JP/analytics/segment/?f=seg_build)します。
1. セグメントビルダーで、「**[!UICONTROL この Experience Cloud オーディエンスを作成]**」オプションを有効にします。

   ![](assets/ec_audience_example.png)

   | 要素 | 説明 |
   |--- |---|
   | この Experience Cloud オーディエンスを作成 (&lt;レポートスイート名&gt; 向け) | このセグメントを Experience Cloud に公開します。公開されたオーディエンスは、Adobe Target でのマーケティングアクティビティと、Audience Manager でのセグメント化に使用できます。<br>公開するためには、「タイトル」および「説明」フィールドが必須です。<br>このオプションを有効にすると、タイトルとオーディエンスセグメントの定義は共有されますが、実際のデータは共有されません。そのオーディエンスが Target のアクティビティに関連付けられている場合、Analytics は、その Experience Cloud および Target オーディエンスに振り分けられた訪問者の ID を送信し始めます。その時点で、オーディエンス名と対応するデータが Experience Cloud オーディエンスページに表示され始めます。<br>Analytics から Experience Cloud に共有するオーディエンスのオーディエンスメンバーの数が 2,000 万を超えてはなりません。<br>キャッシュの影響により、Analytics で削除したレポートスイートが Experience Cloud に反映されるまで 12 時間かかります。<br>Analytics では、公開されたセグメントを編集または削除できます。セグメントが使用中の場合は、セグメントを編集すると、警告メッセージが表示されます。公開したセグメントが Adobe Target によって使用されている場合は削除できません。<br>訪問者が Analytics から共有されるオーディエンスの資格を得てから、その情報が Target、Advertising Cloud および Campaign で対応可能になるまでに、24～48 時間の遅延があります。<br>**データプライバシー**<br>オーディエンスは、訪問者の認証状態に基づいてフィルタリングされません。訪問者が未認証状態および認証状態でサイトを閲覧できる場合、訪問者が未認証のときに生じるアクションによって、訪問者がオーディエンスに含められる可能性があります。[Analytics のプライバシーの概要](https://marketing.adobe.com/resources/help/ja_JP/reference/?f=c_Privacy_Overview)を確認して、オーディエンス共有のプライバシーに関する完全な影響を理解してください。 |
   | オーディエンス作成用のウィンドウを選択してください | これは、固定ではなく、**周期的** な期間です。 |

1. 「**[!UICONTROL 保存]**」をクリックします。
1. Access [!DNL Adobe Target] にアクセスして、「[!UICONTROL オーディエンス]」をクリックします。
1. [!UICONTROL オーディエンス]ページで、Experience Cloud からのオーディエンスを探します。

   これらのオーディエンスは、アクティビティで使用できます。
