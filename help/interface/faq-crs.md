---
description: Adobe Analytics と Adobe Target での、Adobe Experience Cloud の顧客属性に関するよくある質問。
solution: Experience Cloud
title: 顧客属性に関するよくある質問の回答を得る
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: ht
source-wordcount: '1176'
ht-degree: 100%

---

# [!UICONTROL 顧客属性]に関するよくある質問（FAQ）

Adobe Analytics と Adobe Target の[!UICONTROL 顧客属性]に関するよくある質問とベストプラクティス。

## ベストプラクティスと制限事項 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

[!UICONTROL 顧客属性]を使用する際のガイダンスと制限事項

| 問題 | 説明 |
|--- |--- |
| [!UICONTROL 顧客属性]サブスクリプションに関する制限 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、[!UICONTROL 属性サブスクリプションの上限]に関連するエラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | [!UICONTROL 顧客属性]を使用して顧客プロファイルをデータソースにアップロードする場合は、デバイス（同じ Experience Cloud ID）をユーザー間で共有することはお勧めしません。Experience Cloud ID（ECID）はデバイス上で保持されます。デバイスを共有すると、ECID によって複数のユーザーが同じ ECID にリンクされ、[!DNL Target] で予期しない結果が生じる場合があります。**メモ：**&#x200B;モバイルの場合、ECID はモバイルアプリのインストール後、永続的に使用されます。アプリを再インストールすると、新しい ECID が生成されます。Web の場合は、ブラウザーの cookie がクリアされた後で新しい ECID が生成されます。 |
| 毎日のアップロード頻度の制限 | 顧客属性の更新は、1 日に 1 回のみにすることをお勧めします。同じプロファイルセットに対して別の顧客プロファイルデータファイルをアップロードする場合は、24 時間以上待つ必要があります。 |
| カスタム Analytics ID（`s.visitorID`） | `s.visitorID` を使用して顧客 ID を設定すると、Analytics でユーザーを特定しやすくなります。しかし、`s.visitorID.`<br> を使用して訪問者を特定する場合は、ID サービスを利用して [!DNL Analytics] データを書き出しまたは読み込みする統合は機能しません。これには共有 Audiences、Adobe Target（A4T）向け [!DNL Analytics] 、[!UICONTROL 顧客属性]などが該当しますが、これらに限定されません。<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
|  での文字の長さの制限[!DNL Analytics] | [!DNL Analytics] サブスクリプションの作成時には、アップロードするファイルのフィールド長が 255 文字以下になるように切り捨てられます。 |

{style=&quot;table-layout:auto&quot;}

## 顧客属性に関する FAQ {#section_E47866EEA83348E09FE43CEC5E44C461}

| 質問 | 回答 |
|--- |--- |
| 顧客属性のアップロードステータスに関する通知を受け取ることはできますか。 | はい。 |
| 顧客データの使用を開始するために何をおこなう必要がありますか。 | <ol><li>プロビジョニングを受けます。既に Analytics ユーザーになっている場合は、そのユーザーを顧客属性用にアドビがプロビジョニングします。Adobe Target のみを使用していて、Analytics を所有していない場合は、コアサービス用のプロビジョニングをカスタマーケアに依頼する必要があります。</li> <li>CRM チームに連絡します。Analytics や Experience Cloud 全体で使用すると興味深い結果が得られそうな顧客データの種類を見極めます。</li><li>コアサービスを実装します。実装を最新化する方法の手順については、[コアサービスに対するアプリケーションの有効化](core-services.md)を参照してください。（重要な情報については、顧客IDの同期に関する節を参照）。</li></ol> **注意：**&#x200B;コアサービスの実装に関する管理者向けの FAQ については、[こちら](faq.md)を参照してください。 |
| 使用できる顧客属性はいくつありますか。 | 数百の `.csv` 列を顧客属性サービスにアップロードできます。ただし、サブスクリプションを設定して属性を選択する場合、所有するアプリケーションに応じて、（レポートスイートごとに）次の制限が適用されます。  <ul><li>Foundation：0 件</li><li>Select：3 件</li><li>Prime：15 件</li><li>Ultimate：200 件</li><li>Standard：合計 3 件</li><li>Premium：200 件</li><li>Adobe Target Standard：5 件</li><li>Adobe Target Premium：200 件</li></ul> |
| Experience Cloud ID サービスへの移行は必須ですか。 | 移行は、使用するアプリケーションによって異なります。 <ul><li>Adobe Analytics：強くお勧めします。 </li><li>Adobe Target：必要です。 </li></ul><br>Experience Cloud ID サービスを使用すると、リアルタイム Experience Cloud、Adobe Target の最新化、Analytics の統合、ビデオハートビートの追跡など、最新のオーディエンス機能が有効になります。<br>詳しくは、[アプリケーションをコアサービスで有効にする](core-services.md)を参照してください。<br>**注意：**[Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja)は、以前 _Analytics 訪問者 ID サービス_&#x200B;と呼ばれていたサービスの実装を最新化したものです。 |
| 顧客属性機能と Adobe Audience Manager にはどのような関係がありますか？ | Audience Manager は、データを受け取ってオーディエンスの識別を実行することはできますが、属性を履歴行動データに結び付ける分析機能は実行できません。また、Adobe Analytics で使用できるレポート、分析、セグメント化機能も提供していません。[!UICONTROL 人物] は、様々なアプリケーションからのリッチデータを単一の ID に関連付けて、Experience Cloud 全体で使用できるようにします。<br>Adobe Target の場合、顧客属性は、他のルールと統合してオーディエンスを構築できる個人属性として表示されます。[!UICONTROL People] サービスと共有されるオーディエンスは、修正できない完全なオーディエンスです。 |
| **（Analytics のみ）**&#x200B;この機能と Analytics Premium で提供される機能にはどのような違いがありますか。 | 以前は、顧客属性データと Analytics データの組み合わせに興味があっても、この機能を利用するには Data Workbench ツールに大きく依存する必要がありました。[!UICONTROL 顧客属性]では、顧客属性データをディメンションおよび指標として Reports &amp; Analytics、Ad Hoc Analysis および Report Builder に提供することで、この機能をより幅広く利用できるようになりました。Analytics Standard のユーザーは顧客属性にアクセスできますが、使用できる機能には制限があります。Analytics Premium のユーザーは、すべての機能を使用できます。 |
| **（Adobe Target のみ）**&#x200B;これまで Adobe Target で扱っていない顧客のデータをプリロードまたはアップロードできますか。 | はい。訪問者が Adobe Target に対して最初のリクエストをおこなうと、システムは、その訪問者に関してアドビが持っている既存の情報を顧客属性から取得し、ターゲティング用に使用します。**注意：**&#x200B;このデータの取得には、訪問者が最初に Adobe Target とやり取りしてから最大で 20 分かかります。 |
| **（Adobe Target のみ）** 顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成することはできますか？ | いいえ。共有オーディエンスデータは、完了したオーディエンスです。 |
| **（Adobe Target のみ）**[!UICONTROL 顧客属性]機能と Adobe Target の一括プロファイル API にはどのような違いがありますか。 | 一括プロファイル API を使用すると、API を介して、Adobe Target プロファイルを個別または一括で直接更新できます。この機能は顧客属性に似ていますが、次のような大きな違いもあります。<ul><li>プロファイル API は REST API 呼び出しで、顧客属性は FTP を使用します。</li><li>Adobe Target のプロファイル API は、Experience Cloud 全体ではなく、Adobe Target に対してのみデータを送信します。</li><li>顧客属性は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。</li></ul> |
| **（Adobe Target のみ）**&#x200B;顧客属性から Adobe Target にデータをアップロードすると、Adobe Target の訪問者プロファイルの有効期間が延びますか。 | はい。Adobe Target ヘルプの[訪問者プロファイルの有効期間](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=ja)を参照してください。 |
| **（Adobe Target のみ）**&#x200B;訪問者が顧客 ID によって特定された後すぐ、顧客属性にアップロードされたデータをターゲットにできますか。 | はい。mbox サードパーティ ID を含む Adobe Target へのサーバーコール時に、すべての顧客属性データを使用できます。 |
| **（Adobe Target のみ）** 顧客属性ソースにアップロードされたファイルの「**[!UICONTROL 同期ステータス]**」列は何を表していますか？ | Adobe Target で公開および同期されたレコードの数は、特定の属性ファイルに対して、同期ステータスアイコンを選択すると表示できます。`Sync %` は、Adobe Target で同期されたプロファイルの割合（%）を示すリアルタイム指標です。<br> **注意：**&#x200B;属性が Adobe Target と同期するまでに最大 24 時間かかる場合があります。 |
| 顧客属性ソースのファイルアップロード指標は何を表しますか。 | 次の指標を使用して、顧客属性にアップロードされた属性のステータスを確認できます。 <ul><li>レコード：属性ファイル内のレコード数。</li><li>**新しいレコード：**&#x200B;属性ファイルに存在する新しいレコードの数。</li> <li>**更新されたレコード：**&#x200B;顧客属性に既に存在し、ファイル内の値が更新されているレコードの数。</li><li>**すべてのデータ（レコード）：**&#x200B;顧客属性に正常にアップロードされたレコードの合計数です。</li></ul> |

{style=&quot;table-layout:auto&quot;}