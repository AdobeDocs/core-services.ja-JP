---
description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
keywords: customer attributes
seo-description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
seo-title: よくある質問、制限事項、ベストプラクティス
solution: Experience Cloud
title: よくある質問、制限事項、ベストプラクティス
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 670ceb31b40250215d47857102a09c9dfecfb131

---


# よくある質問、制限事項、ベストプラクティス

Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。

## ベストプラクティスと制限事項 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

顧客属性を使用する際のガイダンスと制限事項

| 問題 | 説明 |
|--- |--- |
| 顧客属性サブスクリプションに関する制限事項 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | 顧客属性を使用して顧客プロファイルをデータソースにアップロードする場合、同じデバイス（つまり、同じExperience Cloud ID）を共有するユーザーに対しては、アドビでは推奨しています。 そうすると、デバイス上で存続するECIDサービスが、同じExperience Cloud IDで複数のユーザーをリンクする原因となり、予期しない結果が生じる場合がありま [!DNL Target]す。 **** 注意：Mobileの場合、ECIDはMobileアプリのインストール後に永久的に使用されます。新しいECIDを生成するには、アプリを再インストールする必要があります。 Webの場合、ブラウザーのCookieがクリアされた後に新しいECIDが生成されます。 |
| 毎日の頻度のアップロード制限 | 顧客属性の更新は、1日に1回のみ行うことをお勧めします。 同じプロファイルのセットに対して別の顧客プロファイルデータファイルをアップロードするには、少なくとも24時間待つ必要があります。 |
| Custom Analytics ID (`s.visitorID`) | `s.visitorID` を使用して顧客 ID を設定すると、Analytics でユーザーを特定しやすくなります。ただし、IDサービスを使用してAnalyticsデータを書き出したり読み込んだりする統合は、訪問者が `s.visitorID.`<br>This includes、Analytics for Target(A4T)および顧客属性を使用して識別された場合は機能しません。<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
| Analytics での文字の長さの制限 | Analytics サブスクリプションの作成時には、アップロードするファイルのフィールド長が 255 文字以下になるように切り詰められます。 |

## 顧客属性に関する FAQ {#section_E47866EEA83348E09FE43CEC5E44C461}

| 質問 | 回答 |
|--- |--- |
| 顧客属性のアップロードステータスに関する通知を受け取ることはできますか。 | はい。[通知の管理](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)を参照してください。 |
| 顧客データの使用を開始するために何をおこなう必要がありますか。 | <ol><li>プロビジョニングを受けます。既に Analytics ユーザーになっている場合は、そのユーザーを顧客属性用にアドビがプロビジョニングします。Target のみを使用していて、Analytics を所有していない場合は、コアサービス用のプロビジョニングをカスタマーケアに依頼する必要があります。</li> <li>CRM チームに連絡します。Analytics や Experience Cloud 全体で使用すると興味深い結果が得られそうな顧客データの種類を見極めます。</li><li>コアサービスを実装します。実装を最 [新化する手順については](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html) 、「コアサービスのソリューションを有効にする」を参照してください。 （重要な情報については、顧客 ID の同期に関する節を参照してください）。</li></ol> **注意：**&#x200B;コアサービスの実装に関する管理者向けの FAQ については、[こちら](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)を参照してください。 |
| 使用できる顧客属性はいくつありますか。 | You can upload hundreds of `.csv` columns to the customer attribute service. ただし、購読を設定して属性を選択する場合は、所有するソリューションに応じて、次の制限が（レポートスイートごとに）適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>プレミアム：200</li><li>Target Standard：5 件</li><li>Target Premium：200 件</li></ul> |
| Experience Cloud ID サービスへの移行は必須ですか。 | 移行が必要かどうかは、使用するソリューションによって異なります。 <ul><li>Adobe Analytics：強く推奨されます。 </li><li>Adobe Target：必要です。 </li></ul><br>ID サービスを使用すると、リアルタイムオーディエンス、Target 最新化、Analytics 統合、ビデオハートビート追跡など、最新の Experience Cloud 機能を利用できる機会が広がります。<br> 詳しくは、コアサービ [スのソリューションの有効化を参照してください](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html)。 <br>**注意：** [Experience Cloud IDサービスは](https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html) 、以前の _Analytics訪問者IDサービスと呼ばれる、最新の実装です。_ |
| 顧客属性機能と Adobe Audience Manager にはどのような関係がありますか。 | Audience Manager はデータを受信してオーディエンス識別を実行できますが、属性を履歴行動データに連結する分析機能を実行したり、Adobe Analytics で使用可能なレポート、分析およびセグメント化機能を提供したりすることはできません。People コアサービスは、ソリューション全体からのリッチデータを 1 つにまとめて、Experience Cloud 全体で使用する単一の ID に関連付けることができます。<br>Adobe Target の場合、顧客属性は、他のルールと統合してオーディエンスを構築できる個人属性として表示されます。People コアサービスで共有されるオーディエンスは、修正できない完全なオーディエンスです。 |
| **（Analytics のみ）**&#x200B;この機能と Analytics Premium で提供される機能にはどのような違いがありますか。 | 以前は、顧客属性データと Analytics データの組み合わせに興味があっても、この機能を利用するには data workbench ツールに大きく依存する必要がありました。顧客属性では、顧客属性データをディメンションおよび指標として Reports &amp; Analytics、Ad Hoc Analysis および Report Builder に提供することで、この機能をより幅広く利用できるようになりました。Analytics Standard のユーザーは顧客属性にアクセスできますが、使用できる機能には制限があります。Analytics Premium のユーザーは、すべての機能を使用できます。 |
| **（Target のみ）**&#x200B;これまで Target で扱っていない顧客のデータをプリロードまたはアップロードできますか。 | はい。訪問者が Target に対して最初のリクエストをすると、システムは、その訪問者に関して持っている既存の情報を顧客属性から取得し、ターゲティング用に使用します。**注意：**&#x200B;このデータの取得には、訪問者が最初に Target とやり取りしてから、最大で 20 分かかります。 |
| **（Target のみ）**&#x200B;顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成することはできますか。 | いいえ。共有オーディエンスデータは、完了したオーディエンスです。 |
| **（Target のみ）**&#x200B;顧客属性機能と Target の一括プロファイル API にはどのような違いがありますか。 | 一括プロファイル API を使用すると、API を介して、Target プロファイルを個別または一括で直接更新できます。この機能は顧客属性に似ていますが、次のような大きな違いもあります。<ul><li>プロファイル API は REST API 呼び出しで、顧客属性は FTP を使用します。</li><li>Target のプロファイル API は、Experience Cloud 全体ではなく、Target に対してのみデータを送信します。</li><li>顧客属性は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。 | </li></ul> |
| **（Target のみ）**&#x200B;顧客属性から Adobe Target にデータをアップロードすると、Target の訪問者プロファイルの有効期間が延びますか。 | はい。Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html)を参照してください。 |
| **（Target のみ）**&#x200B;訪問者が顧客 ID によって特定された後すぐ、顧客属性にアップロードされたデータをターゲットにできますか。 | はい。mbox サードパーティ ID を含む Target へのサーバーコール時に、すべての顧客属性データを使用できます。 |
| **（Targetのみ）** 「同期ステータス」列は、顧客属性ソ **[!UICONTROL ースにアップロードされたファイルに対して]** 、何を表しますか。 | Targetが公開および同期したレコードの数は、特定の属性ファイルに対して同期ステータスアイコンをクリックすると表示できます。 `Sync %` は、Targetで同期されたプロファイルの%を指定するリアルタイム指標です。<br> **** 注意：属性がTargetと同期されるまで、最大24時間かかる場合があります。 |
| 顧客属性ソースでは、ファイルのアップロード指標は何を表しますか。 | 次の指標を使用して、顧客属性にアップロードされた属性のステータスを確認できます。 <ul><li> レコード： 属性ファイル内のレコード数。</li><li>**** 新しいレコード：属性ファイルに存在する新しいレコードの数。</li> <li>**** 更新されたレコード：顧客属性に既に存在し、ファイル内の値が更新されたレコードの数。</li><li>**** すべてのデータ（レコード）:顧客属性に正常にアップロードされたレコードの合計数です。</li></ul> |
