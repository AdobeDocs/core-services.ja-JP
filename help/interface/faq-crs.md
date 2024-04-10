---
description: に関するよくある質問 [!DNL Customer Attributes] Adobe Experience Cloud（Adobe AnalyticsおよびAdobe Targetの場合）
solution: Experience Cloud
title: に関するよくある質問 [!DNL Customer Attributes]
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 64%

---

# に関するよくある質問 [!DNL Customer Attributes]

のよくある質問とベストプラクティス [!DNL Customer Attributes] Adobe AnalyticsとAdobe Target。

## ベストプラクティスと制限事項 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

を使用する際のガイダンスと制限事項 [!DNL Customer Attributes].

| 問題 | 説明 |
|--- |--- |
| [!UICONTROL 顧客属性]サブスクリプションに関する制限 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、[!UICONTROL 属性サブスクリプションの上限]に関連するエラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | 使用時 [!DNL Customer Attributes] Adobeでは、顧客プロファイルをデータソースにアップロードする場合に、デバイス（同じExperience Cloud ID）をユーザー間で共有することはお勧めしません。 Experience Cloud ID（ECID）はデバイス上で保持されます。デバイスを共有すると、ECID によって複数のユーザーが同じ ECID にリンクされ、[!DNL Target] で予期しない結果が生じる場合があります。**メモ：**&#x200B;モバイルの場合、ECID はモバイルアプリのインストール後、永続的に使用されます。アプリを再インストールすると、新しい ECID が生成されます。Web の場合は、ブラウザーの cookie がクリアされた後で新しい ECID が生成されます。 |
| 毎日のアップロード頻度の制限 | Adobeでは、次を更新することをお勧めします [!DNL Customer Attributes] 1 日に 1 回のみ。 同じプロファイルセットに対して別の顧客プロファイルデータファイルをアップロードする場合は、24 時間以上待つ必要があります。 |
| カスタム Analytics ID（`s.visitorID`） | `s.visitorID` を使用して顧客 ID を設定すると、Analytics でユーザーを特定しやすくなります。ただし、次のような統合があります [!DNL Analytics] を使用して訪問者を特定した場合、ID サービスを使用したデータの書き出しまたは読み込みは機能しません `s.visitorID.`<br>これには、共有オーディエンスが含まれますが、これに限定されるものではありません。 [!DNL Analytics] Adobe Target（A4T）の場合 [!DNL Customer Attributes].<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
|  での文字の長さの制限[!DNL Analytics] | [!DNL Analytics] サブスクリプションの作成時には、アップロードするファイルのフィールド長が 255 文字以下になるように切り捨てられます。 |

{style="table-layout:auto"}

## に関する FAQ [!DNL Customer Attributes] {#section_E47866EEA83348E09FE43CEC5E44C461}

| 質問 | 回答 |
|--- |--- |
| のアップロードステータスに関する通知を受信できます [!DNL Customer Attributes]? | はい。 |
| を使い始めるためにすべきこと [!DNL Customer Attributes]? | <ol><li>プロビジョニングを受けます。Analytics をご利用の場合、Adobeでは次のプロビジョニングを行います [!DNL Customer Attributes]. Adobe Target のみを使用していて、Analytics を所有していない場合は、コアサービス用のプロビジョニングをカスタマーケアに依頼する必要があります。</li> <li>CRM チームに連絡します。Analytics やExperience Cloud全体で使用する顧客データの種類を確認します。</li><li>コアサービスを実装します。実装を最新化する方法の手順については、[コアサービスに対するアプリケーションの有効化](core-services.md)を参照してください。（重要な情報については、顧客IDの同期に関する節を参照）。</li></ol> **注意：**&#x200B;コアサービスの実装に関する管理者向けの FAQ については、[こちら](faq.md)を参照してください。 |
| 数 [!DNL Customer Attributes] 使用してもよいですか？ | 数百の `.csv` 列を顧客属性サービスにアップロードできます。ただし、サブスクリプションを設定して属性を選択する場合、所有するアプリケーションに応じて、（レポートスイートごとに）次の制限が適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：200 件</li><li>Adobe Target Standard：5 件</li><li>Adobe Target Premium：200 件</li></ul> |
| Experience Cloud ID サービスへの移行は必須ですか。 | 移行は、使用するアプリケーションによって異なります。 <ul><li>Adobe Analytics：強くお勧めします。 </li><li>Adobe Target：必要です。 </li></ul><br>Experience Cloud ID サービスを使用すると、リアルタイム Experience Cloud、Adobe Target の最新化、Analytics の統合、ビデオハートビートの追跡など、最新のオーディエンス機能が有効になります。<br>詳しくは、[アプリケーションをコアサービスで有効にする](core-services.md)を参照してください。<br>**注意：**[Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja)は、以前 _Analytics 訪問者 ID サービス_&#x200B;と呼ばれていたサービスの実装を最新化したものです。 |
| 顧客属性機能と Adobe Audience Manager にはどのような関係がありますか？ | Audience Manager は、データを受け取ってオーディエンスの識別を実行することはできますが、属性を履歴行動データに結び付ける分析機能は実行できません。また、Adobe Analytics で使用できるレポート、分析、セグメント化機能も提供していません。[!UICONTROL 人物] 複数のアプリケーションからのリッチデータを 1 つの ID に関連付けて、Experience Cloudをまたいで使用できるようになります。 <br>Adobe Targetでは、 [!DNL Customer Attributes] オーディエンスを構築するために他のルールと組み合わせることができる個々の属性として表示されます。 [!UICONTROL People] サービスと共有されるオーディエンスは、修正できない完全なオーディエンスです。 |
| **（Analytics のみ）**&#x200B;この機能と Analytics Premium で提供される機能にはどのような違いがありますか。 | 以前は、顧客属性データと Analytics データの組み合わせに興味があっても、この機能を利用するには Data Workbench ツールに大きく依存する必要がありました。[!DNL Customer Attributes] は、次の機能を提供することで、より幅広いオーディエンスにこの機能を公開します [!DNL Customer Attributes] reports &amp; analytics、Ad Hoc Analysisおよび report builder のディメンションおよび指標として。 Analytics Standard のお客様へのアクセス先 [!DNL Customer Attributes]ただし、使用できる機能には制限があります。 Analytics Premium のユーザーは、すべての機能を使用できます。 |
| **（Adobe Target のみ）**&#x200B;これまで Adobe Target で扱っていない顧客のデータをプリロードまたはアップロードできますか。 | はい。訪問者が初めてAdobe Targetにリクエストを行うと、Adobeが持つ顧客に関する既存の情報は次の場所から取得されます [!DNL Customer Attributes] そのデータをターゲティングに使用します。 **注意：**&#x200B;このデータの取得には、訪問者が最初に Adobe Target とやり取りしてから最大で 20 分かかります。 |
| **（Adobe Target のみ）** 顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成することはできますか？ | いいえ。共有オーディエンスデータは、完了したオーディエンスです。 |
| **（Adobe Targetのみ）** 各アクティビティの特長 [!DNL Customer Attributes] 機能は、Adobe Targetの一括プロファイル API と比較しますか？ | 一括プロファイル API を使用すると、API を介して、Adobe Target プロファイルを個別または一括で直接更新できます。機能はに似ています。 [!DNL Customer Attributes]（主な違いは次のとおりです）。<ul><li>プロファイル API は REST API 呼び出しであり、 [!DNL Customer Attributes] は FTP を使用します。</li><li>Adobe Target のプロファイル API は、Experience Cloud 全体ではなく、Adobe Target に対してのみデータを送信します。</li><li>[!DNL Customer Attributes] は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。</li></ul> |
| **（Adobe Targetのみ）** からデータをアップロードします [!DNL Customer Attributes] Adobe Targetを使用してAdobe Target訪問者のプロファイルの有効期間を延長しますか？ | はい。Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=ja)を参照してください。 |
| **（Adobe Targetのみ）** でアップロードされたデータをターゲットにできますか [!DNL Customer Attributes] 訪問者が顧客 ID で識別された直後 | はい。mbox サードパーティ ID を含む Adobe Target へのサーバーコール時に、すべての顧客属性データを使用できます。 |
| **（Adobe Target のみ）** 顧客属性ソースにアップロードされたファイルの「**[!UICONTROL 同期ステータス]**」列は何を表していますか？ | Adobe Target で公開および同期されたレコードの数は、特定の属性ファイルに対して、同期ステータスアイコンを選択すると表示できます。`Sync %` は、Adobe Target で同期されたプロファイルの割合（%）を示すリアルタイム指標です。<br> **注意：**&#x200B;属性が Adobe Target と同期するまでに最大 24 時間かかる場合があります。 |
| でのファイルアップロード指標の意味 [!DNL Customer Attributes] 出典？ | にアップロードされた属性のステータスを確認できます。 [!DNL Customer Attributes] 次の指標を利用できます。 <ul><li>レコード：属性ファイル内のレコード数。</li><li>**新しいレコード：**&#x200B;属性ファイルに存在する新しいレコードの数。</li> <li>**更新されたレコード :** に存在するのレコードの数 [!DNL Customer Attributes] ファイルの値を更新しました。</li><li>**すべてのデータ （レコード）:** に正常にアップロードされたレコードの合計数 [!DNL Customer Attributes].</li></ul> |

{style="table-layout:auto"}