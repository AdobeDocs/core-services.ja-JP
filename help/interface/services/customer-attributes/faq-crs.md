---
description: Adobe Analytics と Adobe Target での、Adobe Experience Cloud の  [!DNL customer attributes]  に関するよくある質問。
solution: Experience Cloud
title: ' [!DNL customer attributes] に関するよくある質問'
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 81%

---

# [!DNL customer attributes] に関するよくある質問

Adobe Analytics と Adobe Target の [!DNL customer attributes] に関するよくある質問とベストプラクティス。

## ベストプラクティスと制限事項 {#best_practices}

[!DNL customer attributes] を使用する際のガイダンスと制限事項

| 問題 | 説明 |
|--- |--- |
| [!UICONTROL &#x200B; 顧客属性 &#x200B;] サブスクリプションの制限 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、[!UICONTROL attribute Subscription Max] エラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | [!DNL customer attributes] を使用して顧客プロファイルをデータソースにアップロードする場合は、デバイスをユーザー間で共有すること（同じ Experience Cloud ID）はお勧めしません。Experience Cloud ID（ECID）はデバイス上で保持されます。デバイスを共有すると、ECID によって複数のユーザーが同じ ECID にリンクされ、[!DNL Target] で予期しない結果が生じる場合があります。**メモ：**&#x200B;モバイルの場合、ECID はモバイルアプリのインストール後、永続的に使用されます。アプリを再インストールすると、新しい ECID が生成されます。Web の場合は、ブラウザーの cookie がクリアされた後で新しい ECID が生成されます。 |
| 毎日のアップロード頻度の制限 | [!DNL customer attributes] の更新は、1 日に 1 回のみにすることをお勧めします。同じプロファイルセットに対して別の顧客プロファイルデータファイルをアップロードする場合は、24 時間以上待つ必要があります。 |
| カスタム Analytics ID（`s.visitorID`） | `s.visitorID` を使用して顧客 ID を設定することは、Adobe Analyticsでユーザーを識別するための手段です。 しかし、`s.visitorID.`<br> を使用して訪問者を特定する場合は、ID サービスを利用して [!DNL Analytics] データを書き出しまたは読み込みする統合は機能しません。これには共有オーディエンス、Adobe Target（A4T）向け [!DNL Analytics] および [!DNL customer attributes] が該当しますが、これらに限定されません。<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
|  での文字の長さの制限[!DNL Analytics] | [!DNL Analytics] サブスクリプションの作成時には、アップロードするファイルのフィールド長が 255 文字以下になるように切り捨てられます。 |

{style="table-layout:auto"}

## [!DNL customer attributes] に関するよくある質問 {#section_E47866EEA83348E09FE43CEC5E44C461}

| Question | 回答 |
|--- |--- |
| [!DNL customer attributes] のアップロードステータスに関する通知を受け取ることはできますか。 | はい。 |
| [!DNL customer attributes] の使用を開始するために何を行う必要がありますか。 | <ol><li>プロビジョニングを受けます。Adobe Analyticsをご利用のお客様は、Adobeから [!DNL customer attributes] をプロビジョニングしています。 Adobe Targetのみを使用し、Analytics がない場合は、カスタマーケアに連絡してコアサービスのプロビジョニングをリクエストします。</li> <li>CRM チームに連絡します。Analytics や Experience Cloud 全体で使用する顧客データの種類を見極めます。</li><li>コアサービスの実装</li></ol> |
| 使用できる [!DNL customer attributes] はいくつありますか。 | 数百の `.csv` 列を顧客属性サービスにアップロードできます。ただし、サブスクリプションを設定して属性を選択する場合、所有するアプリケーションに応じて、（レポートスイートごとに）次の制限が適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：200 件</li><li>Adobe Target Standard：5 件</li><li>Adobe Target Premium：200 件</li></ul> |
| Experience Cloud ID サービスへの移行は必須ですか。 | 移行は、使用するアプリケーションによって異なります。 <ul><li>Adobe Analytics：強くお勧めします。 </li><li>Adobe Target：必要です。 </li></ul><br>Experience Cloud ID サービスを使用すると、リアルタイムオーディエンス、Experience Cloudの最新化、Analytics の統合、ビデオのハートビートトラッキングなど、最新のAdobe Target機能を利用できます。 |
| 顧客属性機能と Adobe Audience Manager にはどのような関係がありますか。 | Audience Manager は、データを受け取ってオーディエンスの識別を実行することはできますが、属性を履歴行動データに結び付ける分析機能は実行できません。また、Adobe Analytics で使用できるレポート、分析、セグメント化機能も提供していません。[!UICONTROL &#x200B; 顧客属性 &#x200B;] により、様々なアプリケーションからのリッチデータを単一の ID に関連付けて、Experience Cloud全体で使用できるようになります。 <br>Adobe Target の場合、[!DNL customer attributes] は他のルールと統合してオーディエンスを構築できる個人属性として表示されます。[!UICONTROL People] サービスと共有されるオーディエンスは、修正できない完全なオーディエンスです。 |
| **（Adobe Analyticsのみ）** この機能と Analytics Premium で提供される機能にはどのような違いがありますか？ | 以前は、顧客属性データと Analytics データの組み合わせに興味があっても、この機能を利用するにはData Workbench ツールに大きく依存する必要がありました。 [!DNL customer attributes] では、Report Builderでディメンションおよび指標として [!DNL customer attributes] を提供することで、この機能をより幅広くオーディエンスに公開します。 Analytics 標準ユーザーは [!DNL customer attributes] にアクセスできますが、使用できる機能には制限があります。Analytics Premium のユーザーは、すべての機能を使用できます。 |
| **（Adobe Target のみ）**&#x200B;これまで Adobe Target で扱っていない顧客のデータをプリロードまたはアップロードできますか。 | はい。訪問者が Adobe Target に対して最初のリクエストを行うと、システムは、その訪問者に関してアドビが持つ既存の情報を [!DNL customer attributes] から取得し、そのデータをターゲティング用に使用します。**注意：**&#x200B;このデータの取得には、訪問者が最初に Adobe Target とやり取りしてから最大で 20 分かかります。 |
| **（Adobe Target のみ）**&#x200B;顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成することはできますか。 | いいえ。共有オーディエンスデータは、完了したオーディエンスです。 |
| **（Adobe Target のみ）** [!DNL customer attributes] 機能と Adobe Target の一括プロファイル API にはどのような違いがありますか。 | 一括プロファイル API を使用すると、API を介して、Adobe Target プロファイルを個別または一括で直接更新できます。この機能は [!DNL customer attributes] に似ていますが、次のような大きな違いもあります。<ul><li>プロファイル API は REST API 呼び出しで、[!DNL customer attributes] は FTP を使用します。</li><li>Adobe Target のプロファイル API は、Experience Cloud 全体ではなく、Adobe Target に対してのみデータを送信します。</li><li>[!DNL customer attributes] は、この外部データを作成および管理するシンプルなインターフェイスを提供します。</li></ul> |
| **（Adobe Target のみ）** [!DNL customer attributes] から Adobe Target にデータをアップロードすると、Adobe Target の訪問者プロファイルの有効期間が延びますか。 | はい。Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=ja)を参照してください。 |
| **（Adobe Target のみ）** 訪問者が顧客 ID によって特定された後すぐ、[!DNL customer attributes] にアップロードされたデータをターゲットにできますか。 | はい。mbox サードパーティ ID を含むAdobe Targetへのサーバーコール時に、すべての顧客属性データを使用できます。 |
| **（Adobe Target のみ）**&#x200B;顧客属性ソースにアップロードされたファイルの「**[!UICONTROL 同期ステータス]**」列は何を表していますか。 | Adobe Target で公開および同期されたレコードの数は、特定の属性ファイルに対して、同期ステータスアイコンを選択すると表示できます。`Sync %` は、Adobe Target で同期されたプロファイルの割合（%）を示すリアルタイム指標です。<br> **メモ：**&#x200B;属性が Adobe Target と同期するまでに最大 24 時間かかる場合があります。 |
| [!DNL customer attributes] ソースのファイルアップロード指標は何を表しますか。 | 次の指標を使用して、[!DNL customer attributes] にアップロードされた属性のステータスを確認できます。 <ul><li>レコード：属性ファイル内のレコード数。</li><li>**新しいレコード：**&#x200B;属性ファイルに存在する新しいレコードの数。</li> <li>**更新されたレコード：** [!DNL customer attributes] に既に存在し、ファイル内の値が更新されているレコードの数。</li><li>**すべてのデータ（レコード）：** [!DNL customer attributes] に正常にアップロードされたレコードの合計数。</li></ul> |

{style="table-layout:auto"}
