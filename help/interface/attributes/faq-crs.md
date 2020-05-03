---
description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
keywords: customer attributes
seo-description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
seo-title: よくある質問、制限事項、ベストプラクティス
solution: Experience Cloud
title: よくある質問、制限事項、ベストプラクティス
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 31811e718be130612c8688e80084cb7579e94f47

---


# よくある質問、制限事項、ベストプラクティス

Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。

## Best practices and limitations {#section_7F5189B3DAA84EE6865B91D2026EE05A}

顧 [!UICONTROL 客属性を使用する場合のガイダンスと制限]。

| 問題 | 説明 |
|--- |--- |
| [!UICONTROL 顧客属性] 購読の制限 | Analytics Premiumにアップグレードする場合、追加の属性が使用可能になるまでに24時間の遅延があります。 この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | 顧客属性を使用して顧客プロファイルをデータソースにアップロードする場合、同じデバイス（同じExperience Cloud ID）を共有しているユーザーに対しては、アドビで推奨されます。 そうすると、ECIDサービス（デバイス上で存続）が同じExperience Cloud IDで複数のユーザーをリンクする原因となり、予期しない結果が生じる場合があり [!DNL Target]ます。 **注意：** Mobileの場合、ECIDはMobileアプリのインストール後に永久的に使用されます。新しいECIDを生成するには、アプリを再インストールする必要があります。 Webの場合、ブラウザーのCookieがクリアされた後に新しいECIDが生成されます。 |
| 毎日の頻度のアップロード制限 | 顧客属性の更新は、1日に1回のみ行うことをお勧めします。 同じプロファイルセットに対して別の顧客プロファイルデータファイルをアップロードするには、24時間以上待つ必要があります。 |
| カスタム解析ID(`s.visitorID`) | `s.visitorID` を使用して顧客 ID を設定すると、Analytics でユーザーを特定しやすくなります。ただし、IDサービスを使用してAnalyticsデータをエクスポートまたはインポートする統合は、「 `s.visitorID.`<br>これには共有オーディエンス、Analytics for Adobeターゲット(A4T)および顧客属性が含まれ、これに限定されません」を使用して訪問者が識別されると、機能しません。<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
| Analyticsの文字長制限 | Analytics購読を作成すると、アップロードされたファイルのフィールドの長さは255文字に切り捨てられます。 |

## 顧客属性に関するFAQ {#section_E47866EEA83348E09FE43CEC5E44C461}

| 質問 | 回答 |
|--- |--- |
| 顧客属性のアップロードステータスに関する通知を受け取ることはできますか。 | はい。[通知の管理](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)を参照してください。 |
| 顧客属性の使用を開始するにはどうすればよいですか。 | <ol><li>プロビジョニングを受けます。 Analyticsのお客様の場合、顧客属性に対してアドビがプロビジョニングを行います。 アドビのターゲットのみを使用し、Analyticsを持っていない場合は、コアサービスのプロビジョニングをカスタマーケアに依頼する必要があります。</li> <li>CRMチームにお問い合わせください。 AnalyticsやExperience Cloud全体で使用すると興味深い結果が得られる顧客データの種類を確認します。</li><li>コアサービスを実装します。 実装を最新化する手順については、コアサービスのソリューションの [有効化](https://docs.adobe.com/content/help/ja-JP/core-services/interface/about-core-services/core-services.html) を参照してください。 （重要な情報については、顧客IDの同期に関する節を参照）。</li></ol> **注意：** コアサービスの実装に関する管理者向けのFAQは、こちら [から入手できます](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)。 |
| 使用できる顧客属性はいくつありますか。 | You can upload hundreds of `.csv` columns to the customer attribute service. ただし、購読を設定して属性を選択する場合、所有するソリューションに応じて、（レポートスイートごとに）次の制限が適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>プレミアム： 200</li><li>Adobeターゲット標準： 5</li><li>Adobeターゲットプレミアム： 200</li></ul> |
| Experience Cloud IDサービスへの移行は必要ですか？ | 移行は、使用するソリューションに応じて異なります。 <ul><li>Adobe Analytics:  強く推奨される </li><li>アドビターゲット: 必須。 </li></ul><br> IDサービスを使用すると、リアルタイムオーディエンス、アドビターゲットの最新化、Analytics統合、ビデオハートビートトラッキングなど、最新のExperience Cloud機能の利用を促進できます。 <br> 詳しくは、コアサービス向けソリューションの [有効化を参照してください](https://docs.adobe.com/content/help/ja-JP/core-services/interface/about-core-services/core-services.html)。 <br>**注意：** [Experience Cloud IDサービス](https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/overview.html) は、以前は _Analytics訪問者IDサービスと呼ばれていたサービスの最新の実装です。_ |
| 顧客属性機能とAdobeオーディエンスマネージャーとの関係は何ですか。 | オーディエンスマネージャーはデータを受け取ってオーディエンスの識別を実行できますが、属性を過去の行動データに結び付ける分析機能を実行したり、Adobe Analyticsで使用できるレポート、分析およびセグメント化機能を提供したりすることはできません。 [!UICONTROL ユーザー] により、複数のソリューションからのリッチデータを1つに結び付け、Experience Cloud全体で使用する単一のIDに関連付けることができます。 <br>Adobeターゲットでは、顧客属性は、オーディエンスを作成するために他のルールと組み合わせることができる個々の属性として表示されます。 [!UICONTROL People] サービスに共有されるオーディエンスは、変更できない完全なオーディエンスです。 |
| **（Analyticsのみ）** 、この機能とAnalytics Premiumで提供される機能との違いを教えてください。 | 以前は、顧客属性データとAnalyticsデータの組み合わせに関心のあるお客様は、この機能のdata workbenchツールに大きく依存していました。 顧客属性では、顧客属性をディメンションおよび指標としてReports &amp; Analytics、Ad Hoc分析およびReport Builderに提供することで、この機能をより幅広いオーディエンスに公開しています。 Analytics Standardのお客様は、顧客属性にアクセスできますが、機能には制限があります。 Analytics Premiumのお客様は、すべての機能を使用できます。 |
| **(Adobeターゲットのみ)** Adobeターゲットがこれまでに経験したことのないお客様向けに、データをプリロードまたはアップロードできますか。 | はい。訪問者がAdobeターゲットに対して最初のリクエストを行うと、そのユーザーに関して持っている既存の情報が顧客属性から取得され、ターゲティング用に使用されます。 **注意：**  このデータの取得には、訪問者が最初にAdobeターゲットとやり取りしてから、最大20分かかる場合があります。 |
| **(Adobeターゲットのみ)** 、顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成できますか。 | いいえ。共有オーディエンスデータは完了したオーディエンスです。 |
| **(アドビターゲットのみ)** 、顧客属性機能とアドビターゲットのバルクプロファイルAPIとの比較方法を教えてください。 | 一括プロファイルAPIを使用すると、Adobeターゲットプロファイルを個別のプロファイルまたは一括でAPI経由で直接更新できます。 この機能は顧客属性に似ていますが、次のような大きな違いがあります。<ul><li>プロファイルAPIはREST API呼び出しで、顧客属性はFTPを使用します。</li><li>AdobeターゲットのプロファイルAPIは、Experience Cloud全体ではなく、Adobeターゲットに対してのみデータを送信します。</li><li>顧客属性は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。</li></ul> |
| **(Adobeターゲットのみ)** 顧客属性からAdobeターゲットにデータをアップロードすると、Adobeターゲット訪問者のプロファイル有効期間が延びますか。 | はい。Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html)を参照してください。 |
| **(Adobeターゲットのみ)** 訪問者が顧客IDで識別された直後に、顧客属性にアップロードされたデータにターゲットできますか。 | はい。mboxサードパーティIDを含むAdobeターゲットへのサーバーコール時に、すべての顧客属性データを使用できるようになります。 |
| **(Adobeターゲットのみ)** 「 **[!UICONTROL 同期ステータス]** 」列は、顧客属性ソースにアップロードされたファイルに対して何を表しますか。 | Adobeターゲットが公開および同期したレコードの数は、特定の属性ファイルに対して同期ステータスアイコンをクリックすると表示できます。 `Sync %` は、Adobeターゲットで同期されたプロファイルの割合を指定するリアルタイム指標です。<br> **注意：** 属性がAdobeターゲットと同期されるまで、最大24時間かかる場合があります。 |
| 顧客属性ソースでは、ファイルのアップロード指標は何を表しますか。 | 次の指標を使用して、顧客属性にアップロードされた属性のステータスを確認できます。 <ul><li>レコード：  属性ファイル内のレコード数。</li><li>**新しいレコード：** 属性ファイルに存在する新しいレコードの数。</li> <li>**更新されたレコード：** 顧客属性に既に存在し、ファイル内の値が更新されているレコードの数。</li><li>**すべてのデータ（レコード）:** 顧客属性に正常にアップロードされたレコードの合計数です。</li></ul> |
