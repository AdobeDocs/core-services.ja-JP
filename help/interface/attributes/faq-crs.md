---
description: Analyticsとターゲットの顧客属性に関するFAQとベストプラクティスです。
keywords: Customer Attributes
seo-description: Analyticsとターゲットの顧客属性に関するFAQとベストプラクティスです。
seo-title: よくある質問、制限事項、ベストプラクティス
solution: Experience Cloud
title: よくある質問、制限事項、ベストプラクティス
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 75%

---


# よくある質問、制限事項、ベストプラクティス

Analyticsとターゲットの顧客属性に関するFAQとベストプラクティスです。

## ベストプラクティスと制限事項 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Guidance and limitations when using [!UICONTROL Customer Attributes].

| 問題 | 説明 |
|--- |--- |
| [!UICONTROL 顧客属性]サブスクリプションに関する制限 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | 顧客属性を使用して顧客プロファイルをデータソースにアップロードする場合、同じデバイス（同じExperience Cloud ID）を共有しているユーザーに対しては、この方法をお勧めします。 共有すると、ECID サービス（デバイス上で存続）が同じ Experience Cloud ID で複数のユーザーをリンクする可能性があり、[!DNL Target] で予期しない結果が生じる場合があります。**注意：**&#x200B;モバイルの場合、ECID はモバイルアプリのインストール後、永久的に使用されます。新しい ECID を生成するには、アプリを再インストールする必要があります。Web の場合は、ブラウザーの cookie がクリアされた後で新しい ECID が生成されます。 |
| 毎日のアップロード頻度の制限 | 顧客属性の更新は、1日に1回のみ行うことをお勧めします。 同じプロファイルセットに対して別の顧客プロファイルデータファイルをアップロードする場合は、24 時間以上待つ必要があります。 |
| カスタム Analytics ID（`s.visitorID`） | `s.visitorID` を使用して顧客 ID を設定すると、Analytics でユーザーを特定しやすくなります。However, integrations in which Analytics data is exported or imported using the ID Service will not function when a visitor is identified using `s.visitorID.`<br>This includes, but is not limited to, shared Audiences, Analytics for Adobe Target (A4T), and Customer Attributes.<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
| Analytics での文字の長さの制限 | Analytics サブスクリプションの作成時には、アップロードするファイルのフィールド長が 255 文字以下になるように切り詰められます。 |

## FAQ about Customer Attributes {#section_E47866EEA83348E09FE43CEC5E44C461}

| 質問 | 回答 |
|--- |--- |
| 顧客属性のアップロードステータスに関する通知を受け取ることはできますか。 | はい。[通知の管理](https://docs.adobe.com/content/help/ja-JP/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)を参照してください。 |
| 顧客属性の使用を開始するにはどうすればよいですか。 | <ol><li>プロビジョニングを受けます。Analyticsのお客様の場合、アドビでは顧客属性のプロビジョニングを行います。 Adobe Target のみを使用していて、Analytics を所有していない場合は、コアサービス用のプロビジョニングをカスタマーケアに依頼する必要があります。</li> <li>CRM チームに連絡します。Analytics や Experience Cloud 全体で使用すると興味深い結果が得られそうな顧客データの種類を見極めます。</li><li>コアサービスを実装します。実装を最新化する方法の手順については、[ソリューションのコアサービスへの対応](https://docs.adobe.com/content/help/ja-JP/core-services/interface/about-core-services/core-services.html)を参照してください（重要な情報については、顧客IDの同期に関する節を参照）。</li></ol> **注意：**&#x200B;コアサービスの実装に関する管理者向けの FAQ については、[こちら](https://docs.adobe.com/content/help/ja-JP/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)を参照してください。 |
| 使用できる顧客属性の数はいくつですか。 | 数百の `.csv` 列を顧客属性サービスにアップロードできます。ただし、サブスクリプションを設定し属性を選択する場合、所有するソリューションに応じて、（レポートスイートごとに）次の制限が適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：200 件</li><li>Adobe Target Standard：5 件</li><li>Adobe Target Premium：200 件</li></ul> |
| Experience Cloud ID サービスへの移行は必須ですか。 | 移行が必要かどうかは、使用するソリューションによって異なります。 <ul><li>Adobe Analytics：強くお勧めします。 </li><li>Adobe Target：必要です。 </li></ul><br>ID サービスを使用すると、リアルタイムオーディエンス、Adobe Target 最新化、Analytics 統合、ビデオハートビート追跡など、最新の Experience Cloud 機能を利用できる機会が広がります。<br>詳しくは、[ソリューションのコアサービスへの対応](https://docs.adobe.com/content/help/ja-JP/core-services/interface/about-core-services/core-services.html)を参照してください。<br>注意：[ Experience Cloud ID サービス](https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/overview.html)は、以前 _Analytics 訪問者 ID サービス_&#x200B;と呼ばれていたサービスの実装を最新化したものです。 |
| 顧客属性機能と Adobe Audience Manager にはどのような関係がありますか。 | Audience Manager はデータを受信してオーディエンス識別を実行できますが、属性を履歴行動データに連結する分析機能を実行したり、Adobe Analytics で使用可能なレポート、分析およびセグメント化機能を提供したりすることはできません。[!UICONTROL People] は、ソリューション全体からのリッチデータを 1 つにまとめて、Experience Cloud 全体で使用する単一の ID に関連付けることができます。<br>Adobe Targetでは、顧客属性は、他のルールと組み合わせてオーディエンスを作成できる個々の属性として表示されます。 [!UICONTROL People] サービスと共有されるオーディエンスは、修正できない完全なオーディエンスです。 |
| **（Analytics のみ）**&#x200B;この機能と Analytics Premium で提供される機能にはどのような違いがありますか。 | 以前は、顧客属性データと Analytics データの組み合わせに興味があっても、この機能を利用するには Data Workbench ツールに大きく依存する必要がありました。顧客属性では、顧客属性をディメンションおよび指標としてReports &amp; Analytics、Ad Hoc AnalysisおよびReport Builderに提供することで、この機能をより幅広いオーディエンスに公開しています。 Analytics Standardのお客様は、顧客属性にアクセスできますが、機能には制限があります。 Analytics Premium のユーザーは、すべての機能を使用できます。 |
| **（Adobe Target のみ）**&#x200B;これまで Adobe Target で扱っていない顧客のデータをプリロードまたはアップロードできますか。 | はい。訪問者が Adobe Target に対して最初のリクエストをおこなうと、システムは、その訪問者に関して持っている既存の情報を顧客属性から取得し、ターゲティング用に使用します。**注意：**&#x200B;このデータの取得には、訪問者が最初に Target とやり取りしてから最大で 20 分かかります。 |
| **（Adobe Target のみ）**&#x200B;顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成することはできますか。 | いいえ。共有オーディエンスデータは、完了したオーディエンスです。 |
| **（Adobe Targetのみ）** 顧客属性機能とAdobe Targetの一括プロファイルAPIとの比較 | 一括プロファイル API を使用すると、API を介して、Adobe Target プロファイルを個別または一括で直接更新できます。この機能は顧客属性に似ていますが、次のような大きな違いがあります。<ul><li>プロファイルAPIはREST API呼び出しで、顧客属性はFTPを使用します。</li><li>Adobe Target のプロファイル API は、Experience Cloud 全体ではなく、Adobe Target に対してのみデータを送信します。</li><li>顧客属性は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。</li></ul> |
| **（Adobe Targetのみ）** 顧客属性からAdobe Targetにデータをアップロードすると、Adobe Target訪問者のプロファイル有効期間が延びますか。 | はい。Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://docs.adobe.com/content/help/ja-JP/target/using/audiences/visitor-profiles/visitor-profile.html)を参照してください。 |
| **（Adobe Targetのみ）** 、顧客IDで訪問者が識別された直後に、顧客属性にアップロードされたデータにターゲットできますか。 | はい。mbox サードパーティ ID を含む Adobe Target へのサーバーコール時に、すべての顧客属性データを使用できます。 |
| **（Adobe Target のみ）**&#x200B;顧客属性ソースにアップロードされたファイルの「**[!UICONTROL 同期ステータス]**」列は何を表していますか。 | Adobe Target で公開および同期されたレコードの数は、特定の属性ファイルに対して「同期ステータス」アイコンをクリックすると表示できます。`Sync %` は、Adobe Target で同期されたプロファイルの割合（%）を示すリアルタイム指標です。<br> **注意：**&#x200B;属性が Adobe Target と同期するまでに最大 24 時間かかる場合があります。 |
| 顧客属性ソースのファイルアップロード指標は何を表しますか。 | 次の指標を使用して、顧客属性にアップロードされた属性のステータスを確認できます。 <ul><li>レコード：属性ファイル内のレコード数。</li><li>**新しいレコード：**&#x200B;属性ファイルに存在する新しいレコードの数。</li> <li>**更新されたレコード：**&#x200B;顧客属性に既に存在し、ファイル内の値が更新されているレコードの数。</li><li>**すべてのデータ（レコード）：**&#x200B;顧客属性に正常にアップロードされたレコードの合計数です。</li></ul> |
