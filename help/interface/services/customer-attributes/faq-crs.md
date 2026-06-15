---
description: Adobe AnalyticsおよびAdobe TargetのAdobe CX Enterpriseの [!DNL Customer Attributes] に関するよくある質問に対する回答を表示します。
solution: Experience Cloud
title: ' [!DNL Customer Attributes] に関するよくある質問'
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
TQID: https://experienceleague.adobe.com/ZAKogDXCbaZHOiyzlgg6Od0pxGwWi2w9yXtPnKWZKUw
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 1064
ht-degree: 59%

---

# [!DNL Customer Attributes] に関するよくある質問

Adobe Analytics と Adobe Target の [!DNL Customer Attributes] に関するよくある質問とベストプラクティス。

## ベストプラクティスと制限

[!DNL Customer Attributes] を使用する際のガイダンスと制限事項

| 問題 | 説明 |
| --- | --- |
| [!DNL Customer Attributes] [&#x200B; サブスクリプション &#x200B;](subscription.md)の制限 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。 この遅延中に[!UICONTROL attribute Subscription Max] エラーが発生する場合があります。 |
| 同じデバイスでの複数のログイン | [!DNL Customer Attributes]を使用して顧客プロファイルをデータソースにアップロードする場合、Adobeでは、デバイスを共有しているユーザー（つまり、同じCX Enterprise ID）に対して推奨されます。 CX Enterprise ID（ECID）はデバイスに保持されます。 デバイスを共有すると、ECID によって複数のユーザーが同じ ECID にリンクされ、[!DNL Target] で予期しない結果が生じる場合があります。 **メモ：** Mobileの場合、ECIDはモバイルアプリのインストール後に永続的になります。 アプリを再インストールして、新しいECIDを生成します。 Web の場合は、ブラウザーの cookie がクリアされた後で新しい ECID が生成されます。 |
| 毎日のアップロード頻度の制限 | [!DNL Customer Attributes] の更新は、1 日に 1 回のみにすることをお勧めします。 同じプロファイルセットに対して別の顧客プロファイルデータファイルをアップロードする場合は、24 時間以上待つ必要があります。 |
| カスタム Analytics ID（`s.visitorID`） | `s.visitorID`を使用して顧客IDを設定することは、Adobe Analyticsでユーザーを識別する方法です。 ただし、`s.visitorID.`<br>を使用して訪問者を識別する場合、[!DNL Analytics] データがID サービスを使用してエクスポートまたはインポートされる統合は機能しません。これには、共有オーディエンス、[!DNL Analytics]のAdobe Target（A4T）および[!DNL Customer Attributes]が含まれますが、これらに限定されません。<br>これらの統合では、カスタム Analytics IDの設定はサポートされていません。 |
| での文字の長さの制限[!DNL Analytics] | [!DNL Analytics] [&#x200B; サブスクリプション &#x200B;](subscription.md)を作成する場合、アップロードされたファイルのフィールド長は255に切り捨てられます。 |

{style="table-layout:auto"}

## [!DNL Customer Attributes] に関するよくある質問

| 質問 | 回答 |
| --- | --- |
| [!DNL Customer Attributes] のアップロードステータスに関する通知を受け取ることはできますか。 | はい。 |
| [!DNL Customer Attributes] の使用を開始するために何を行う必要がありますか。 | <ol><li>プロビジョニングを受けます。 Adobe Analyticsのお客様の場合は、Adobeで[!DNL Customer Attributes]のプロビジョニングを行います。 Adobe Targetのみを使用し、Analyticsを持っていない場合は、コアサービスのプロビジョニングをリクエストするには、カスタマーケアにお問い合わせください。</li> <li>CRM チームに連絡します。 Adobe AnalyticsやCX Enterprise全体で、どのような顧客データを利用できるのかを確認します。</li><li>コアサービスの実装。</li></ol> ユーザーがこの機能を使用できるようにする方法については、データをアップロードする前に、[前提条件](t-crs-usecase.md#prerequisites-for-using-customer-attributes)を参照してください。 |
| 使用できる顧客属性はいくつありますか。 | 数百の `.csv` 列を顧客属性サービスにアップロードできます。 ただし、サブスクリプションを設定して属性を選択する場合、所有するアプリケーションに応じて、（レポートスイートごとに）次の制限が適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：200 件</li><li>Adobe Target Standard：5 件</li><li>Adobe Target Premium：200 件</li></ul> |
| CX Enterprise ID サービスへの移行は必要ですか？ | 移行は、使用するアプリケーションによって異なります。 <ul><li>Adobe Analytics：強くお勧めします。 </li><li>Adobe Target：必要です。 </li></ul>CX Enterprise ID サービスを使用すると、リアルタイムオーディエンス、Adobe Targetの最新化、Analyticsとの統合、ビデオのハートビートトラッキングなど、最新のCX エンタープライズ機能が可能になります。 |
| 顧客属性機能と Adobe Audience Manager にはどのような関係がありますか。 | Audience Manager は、データを受け取ってオーディエンスの識別を実行することはできますが、属性を履歴行動データに結び付ける分析機能は実行できません。 また、Adobe Analytics で使用できるレポート、分析、セグメント化機能も提供していません。 [!DNL Customer Attributes]を使用すると、複数のアプリケーションからの豊富なデータを統合し、CX Enterprise全体で使用するために単一のIDに関連付けることができます。 <br>Adobe Target の場合、顧客属性は、他のルールと統合してオーディエンスを構築できる個人属性として表示されます。 [!UICONTROL People] サービスに共有されたオーディエンスは、変更できない完全なオーディエンスです。 |
| **（Adobe Analyticsのみ）**&#x200B;この機能は、Analytics Premiumで提供されるものとどのように異なりますか？ | 以前は、顧客属性データとAdobe Analytics データを組み合わせたいと考えているお客様は、この機能はData Workbenchツールに大きく依存していました。 [!DNL Customer Attributes]は、Report Builderで顧客属性をディメンションおよび指標として提供することで、この機能をより多くのユーザーに公開します。 Analytics 標準ユーザーは [!DNL Customer Attributes] にアクセスできますが、使用できる機能には制限があります。 Analytics Premium のユーザーは、すべての機能を使用できます。 |
| **（Adobe Target のみ）**&#x200B;これまで Adobe Target で扱っていない顧客のデータをプリロードまたはアップロードできますか。 | はい。 訪問者が Adobe Target に対して最初のリクエストを行うと、システムは、その訪問者に関してアドビが持つ既存の情報を [!DNL Customer Attributes] から取得し、そのデータをターゲティング用に使用します。 **注意：**&#x200B;このデータの取得には、訪問者が最初に Adobe Target とやり取りしてから最大で 20 分かかります。 |
| **（Adobe Target のみ）**&#x200B;顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成することはできますか。 | いいえ。 共有オーディエンスデータは、完了したオーディエンスです。 |
| **（Adobe Targetのみ）** [!DNL Customer Attributes]とAdobe Targetの一括プロファイル APIの比較はどうなりますか？ | 一括プロファイル API を使用すると、API を介して、Adobe Target プロファイルを個別または一括で直接更新できます。 この機能は [!DNL Customer Attributes] に似ていますが、次のような大きな違いもあります。<ul><li>プロファイル API は REST API 呼び出しで、[!DNL Customer Attributes] は FTP を使用します。</li><li>Adobe Targetのプロファイル APIは、CX Enterprise全体ではなく、Adobe Targetにのみデータを送信します。</li><li>[!DNL Customer Attributes] は、この外部データを作成および管理するシンプルなインターフェイスを提供します。</li></ul> |
| **（Adobe Target のみ）** [!DNL Customer Attributes] から Adobe Target にデータをアップロードすると、Adobe Target の訪問者プロファイルの有効期間が延びますか。 | はい。 Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=ja)を参照してください。 |
| **（Adobe Target のみ）** 訪問者が顧客 ID によって特定された後すぐ、[!DNL Customer Attributes] にアップロードされたデータをターゲットにできますか。 | はい。 mbox サードパーティ IDを含むAdobe Targetへのサーバー呼び出しでは、すべての顧客属性データを使用できます。 |
| **（Adobe Targetのみ）**&#x200B;お客様の属性ソースにアップロードされたファイルの&#x200B;**[!UICONTROL Sync Status]**&#x200B;列は何を表していますか？ | Adobe Target で公開および同期されたレコードの数は、特定の属性ファイルに対して、同期ステータスアイコンを選択すると表示できます。 `Sync %` は、Adobe Target で同期されたプロファイルの割合（%）を示すリアルタイム指標です。<br> **メモ：**&#x200B;属性が Adobe Target と同期するまでに最大 24 時間かかる場合があります。 |
| [!DNL Customer Attributes] ソースのファイルアップロード指標は何を表しますか。 | 次の指標を使用して、[!DNL Customer Attributes] にアップロードされた属性のステータスを確認できます。 <ul><li>レコード：属性ファイル内のレコード数。</li><li>**新しいレコード：**&#x200B;属性ファイルに存在する新しいレコードの数。</li> <li>**更新されたレコード：** [!DNL Customer Attributes] に既に存在し、ファイル内の値が更新されているレコードの数。</li><li>**すべてのデータ（レコード）：** [!DNL Customer Attributes] に正常にアップロードされたレコードの合計数。</li></ul> |

{style="table-layout:auto"}
