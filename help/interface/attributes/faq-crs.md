---
description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
keywords: customer attributes
seo-description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
seo-title: よくある質問、制限事項、ベストプラクティス
solution: Experience Cloud
title: よくある質問、制限事項、ベストプラクティス
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# よくある質問、制限事項、ベストプラクティス

Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。

## Best practices and limitations {#section_7F5189B3DAA84EE6865B91D2026EE05A}

顧客属性を使用する場合のガイダンスと制限。

| 問題 | 説明 |
|--- |--- |
| 顧客属性の購読の制限 | Analytics Premiumにアップグレードすると、追加の属性が使用可能になるまでに24時間の遅延が発生します。 この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | 顧客属性を使用して顧客プロファイルをデータソースにアップロードする場合、同じデバイス（同じExperience Cloud ID）を共有するユーザーに対しては、アドビでは推奨します。 これを行うと、ECIDサービス（デバイス上で存続）が同じExperience Cloud IDで複数のユーザーをリンクし、予期しない結果が生じる可能性がありま [!DNL Target]す。 **注意：** Mobileの場合、ECIDはMobileアプリのインストール後に永久的に使用されます。新しいECIDを生成するには、アプリを再インストールする必要があります。 Webの場合、ブラウザーのCookieがクリアされた後に新しいECIDが生成されます。 |
| 毎日の頻度のアップロード制限 | 顧客属性は1日に1回のみ更新することをお勧めします。 同じプロファイルのセットに対して別の顧客プロファイルデータファイルをアップロードするには、少なくとも24時間待つ必要があります。 |
| カスタム解析ID(`s.visitorID`) | `s.visitorID` を使用して顧客 ID を設定すると、Analytics でユーザーを特定しやすくなります。ただし、IDサービスを使用してAnalyticsデータを書き出しまたは読み込む統合は、 `s.visitorID.`<br>Thisを使用して訪問者が識別された場合は機能しません。Thisは、共有オーディエンス、Analytics for Adobe Target(A4T)および顧客属性を含みます。<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
| Analyticsの文字長の制限 | Analyticsサブスクリプションを作成すると、アップロードされたファイルのフィールドの長さが255文字に切り捨てられます。 |

## 顧客属性に関するFAQ {#section_E47866EEA83348E09FE43CEC5E44C461}

| 質問 | 回答 |
|--- |--- |
| 顧客属性のアップロードステータスに関する通知を受け取ることはできますか。 | はい。[通知の管理](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)を参照してください。 |
| 顧客属性の使用を開始するには、どのような方法が必要ですか。 | <ol><li>プロビジョニングを受けます。 Analyticsのお客様の場合、アドビでは顧客属性のプロビジョニングを行っています。 Adobe Targetのみを使用し、Analyticsを持っていない場合は、カスタマーケアに問い合わせて、コアサービスのプロビジョニングをリクエストする必要があります。</li> <li>CRMチームとお問い合わせください。 AnalyticsやExperience Cloud全体で使用すると興味深い顧客データの種類を確認します。</li><li>コアサービスを実装します。 実装を最 [新化する手順については、](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html) 「コアサービスのソリューションを有効にする」を参照してください。 （重要な情報については、「顧客IDの同期」の節を参照してください）。</li></ol> **注意：** コアサービスの実装に関する管理者向けのFAQについては、こちらを参照して [ください](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)。 |
| 使用できる顧客属性はいくつありますか。 | You can upload hundreds of `.csv` columns to the customer attribute service. ただし、購読を設定して属性を選択する場合、所有するソリューションに応じて、（レポートスイートごとに）次の制限が適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>プレミアム：200</li><li>Adobe Target Standard:5</li><li>Adobe Target Premium:200</li></ul> |
| Experience Cloud IDサービスへの移行は必要ですか？ | 移行は、使用するソリューションによって異なります。 <ul><li>Adobe Analytics: 強く推奨 </li><li>Adobe Target:必須。 </li></ul><br> IDサービスを使用すると、リアルタイムオーディエンス、Adobe Targetの最新化、Analyticsの統合、ビデオハートビートの追跡など、最新のExperience Cloud機能を利用するための扉が開かれます。 <br> 詳しくは、コアサービスのソ [リューションを有効にするを参照してくださ](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html)い。 <br>**注意：** [Experience Cloud IDサービスは](https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html) 、以前の _Analytics訪問者IDサービスと呼ばれていた最新の実装です。_ |
| 顧客属性機能とAdobe Audience Managerとの関連性を教えてください。 | Audience Managerは、データを受け取ってオーディエンスの識別を実行できますが、属性を履歴行動データに結び付ける分析機能を実行したり、Adobe Analyticsで使用できるレポート、分析およびセグメント化機能を提供したりすることはできません。 Peopleコアサービスを使用すると、複数のソリューションからのリッチデータを1つに結び付け、単一のIDに関連付けて、Experience Cloud全体で使用できます。 <br>Adobe Targetでは、顧客属性は、他のルールと組み合わせてオーディエンスを作成できる個々の属性として表示されます。 Peopleコアサービスで共有されるオーディエンスは、変更できない完全なオーディエンスです。 |
| **（Analyticsのみ）** 、この機能とAnalytics Premiumで提供される機能との違いを教えてください。 | 以前は、顧客属性データとAnalyticsデータの組み合わせに関心のあるお客様は、この機能に対してData Workbenchツールに大きく依存していました。 顧客属性は、顧客属性をディメンションおよび指標としてReports &amp; Analytics、Ad Hoc AnalysisおよびReport Builderに提供することで、この機能をより幅広いオーディエンスに公開します。 Analytics Standardのお客様は、顧客属性にアクセスできますが、機能が制限されます。 Analytics Premiumのお客様は、すべての機能を利用できます。 |
| **（Adobe Targetのみ）** 、Adobe Targetがこれまで見たことのない顧客向けに、データをプリロードまたはアップロードできますか。 | はい。訪問者がAdobe Targetに対して最初のリクエストを行うと、システムは、その訪問者に関して持っている既存の情報を顧客属性から取得し、そのデータをターゲティングに使用します。 **注意：** このデータの取得には、訪問者がAdobe Targetと最初にやり取りしてから、最大20分かかる場合があります。 |
| **（Adobe Targetのみ）顧客属性データを** 、共有オーディエンスデータと組み合わせて、スーパーオーディエンスを作成できますか。 | いいえ。共有オーディエンスデータは、完了したオーディエンスです。 |
| **（Adobe Targetのみ）** 、顧客属性機能とAdobe TargetのバルクプロファイルAPIとの比較方法を教えてください。 | 一括プロファイルAPIを使用すると、Adobe Targetプロファイルを、個々のプロファイルまたは一括でAPIを介して直接更新できます。 この機能は顧客属性に似ていますが、次のような主な違いがあります。<ul><li>プロファイルAPIはREST API呼び出しで、顧客属性はFTPを使用します。</li><li>Adobe TargetのプロファイルAPIは、Experience Cloud全体ではなく、Adobe Targetにのみデータを送信します。</li><li>顧客属性は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。</li></ul> |
| **（Adobe Targetのみ）顧客属性からAdobe Targetにデータをアップロードすると** 、Adobe Target訪問者のプロファイルの有効期間が延びますか。 | はい。Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html)を参照してください。 |
| **（Adobe Targetのみ）** 、訪問者が顧客IDで識別された直後に、顧客属性にアップロードされたデータをターゲットに設定できますか。 | はい。mboxサードパーティIDを含むAdobe Targetへのサーバー呼び出し時に、すべての顧客属性データが使用可能になります。 |
| **（Adobe Targetのみ）** 「同期ステータス」列は **[!UICONTROL 、顧客属性ソースにアップロードされたファイルに対して]** 、どのような意味を持ちますか。 | Adobe Targetによって公開および同期されたレコードの数は、特定の属性ファイルに対して同期ステータスアイコンをクリックすると表示できます。 `Sync %` は、Adobe Targetで同期されたプロファイルの%を指定するリアルタイム指標です。<br> **注意：** 属性がAdobe Targetと同期されるまで、最大24時間かかる場合があります。 |
| 顧客属性ソースのファイルアップロード指標は何を表しますか。 | 次の指標を使用して、顧客属性にアップロードされた属性のステータスを確認できます。 <ul><li>レコード： 属性ファイル内のレコード数。</li><li>**新しいレコード：** 属性ファイルに存在する新しいレコードの数。</li> <li>**更新されたレコード：** 顧客属性に既に存在し、ファイル内の値が更新されているレコードの数。</li><li>**すべてのデータ（レコード）:** 顧客属性に正常にアップロードされたレコードの合計数です。</li></ul> |
