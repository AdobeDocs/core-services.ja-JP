---
title: エージェントのジョブとAI クレジット消費
description: CX エンタープライズアプリケーションにおける担当者の業務とAI クレジットの消費率について説明します。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
TQID: 'https://experienceleague.adobe.com/REonDh6tRlMxB3iAryxC0BLXeVTTaUuwCu98DXyESVQ'
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 1055
ht-degree: 3%

---

# Adobe Experience PlatformのエージェントのジョブとAI クレジットの使用

更新日：**2026年3月5日**

CX エンタープライズアプリケーションにおけるエージェント型AIのジョブとAI クレジット消費について説明します。 既存のCX Enterprise アプリケーションでAgentic AI機能を有効にする方法について詳しくは、[CX EnterpriseでのAgentic AI](agentic-ai.md#existing-apps)を参照してください。

## エージェントジョブ

_エージェントジョブ_&#x200B;は、顧客の入力によって指示されるように、エージェントが特定の結果を達成するために実行する一連のタスクとアクションです。

AI アシスタントによる自然言語プロンプトを使用し、エージェントに特定のジョブの実行を依頼できます。 これらのデータに基づいて、Agent Orchestratorは適切な担当者を調整し、関連するCX Enterprise アプリケーション内の各ステップを実行します。

## AI クレジット

_AI クレジット_&#x200B;は、エージェント ジョブの実行を定量化する使用状況ベースの指標です。 AI クレジットは、[AI ファーストのアプリケーション &#x200B;](/help/interface/features/agentic-ai.md)には適用されません。

## AI クレジット消費

AIによるクレジットの使用状況は、実行されるジョブの複雑さと価値によって異なります。

* 単純な（多くの場合シングルステップ）タスクでは、クレジットの消費が少なくなります
* 複雑な（多くの場合マルチステップ）タスクでは、より多くのクレジットが消費されます
* 高度な推論、検証、マルチエージェントの調整、または統合を伴うタスクは、より多くのクレジットを消費します

### 予測AI クレジット消費量

| エージェント | ジョブ | サポートされているアプリケーション | 推定AI クレジット | サンプルプロンプト |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience Agent | オーディエンス/アカウントのアイデア立案 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 50 | <ul><li><em>富裕層の購入者のフィールドを表示</em></li><li><em>顧客の環境設定に関連するすべてのフィールドを検索</em></li></ul> |
| Audience Agent | ナレッジベースのオーディエンス/アカウント作成 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 150 | <ul><li><em> カリフォルニア在住のユーザーで構成されるオーディエンスを作成</em></li><li><em>今四半期に1000 ドル以上を費やしたVIP メンバーのオーディエンスを生成</em></li><li><em>衣料品を購入したが、過去60日間に購入していないユーザーのオーディエンスを作成する</em></li></ul> |
| Audience Agent | オーディエンス/アカウント管理 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li><em>重複するオーディエンスがありますか？</em></li><li><em>最大5人のオーディエンスを表示します。</em></li><li><em>どの宛先にもアクティブ化されていないオーディエンスを表示</em></li><li><em> ライブジャーニーで使用されているすべてのオーディエンスを一覧表示</em></li></ul> |
| Audience Agent | オーディエンス/アカウント分析 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li><em>先週20%以上増加したオーディエンスはどれですか？</em></li><li><em>30日前の値と比較して、オーディエンス「ロイヤルプラチナ」はどの程度変化していますか？</em></li><li><em>最も急成長しているオーディエンスは何ですか？</em></li></ul> |
| Audience Agent | 購買グループのアイデア創出 | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li><em>これらの製品の意図を示しているアカウントはどれですか？</em></li><li><em>XYZの製品インテント別の上位の人物を表示します。</em></li><li><em>5人以上のメンバーがいる購買グループはどれですか？</em></li></ul> |
| Data Insights Agent | データ分析と可視化 | <ul><li>Customer Journey Analytics（B2CおよびB2B エディション）</li></ul> | 25 | <ul><li><em>7月のトレンド注文</em></li><li><em>地域別の収益を表示します。</em></li><li><em>3月から6月までの性別で注文を表示します。</em></li><li><em>6月の利益別の上位10のSKUは何ですか</em></li><li><em>月別の購入割合</em></li><li><em>製品カテゴリ別の収益の割合</em></li></ul> |
| Journey Agent | ジャーニーの構想 | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li><em>Web サイト上のコンテンツでエンゲージしているユーザーに焦点を当て、ソリューションの意図を持って空白アカウントのジャーニーを作成します</em></li></ul> |
| Journey Agent | ジャーニー制作 | <ul><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li></ul> | 30 | <ul><li><em>過去7日間に最初の購入を完了していないユーザーにリマインダーを送信するジャーニーを生成</em></li><li><em> ユーザーが最初の購入を完了したら、3日後にSMS確認とフォローアップ特典の説明をメールで送信します</em></li></ul> |
| Journey Agent | ジャーニー分析 | <ul><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li></ul> | 50 | <ul><li><em>7月4日のキャンペーンのジャーニーのノード別のフォールアウトを分析します。</em></li><li><em> ジャーニーX</em>のスケジュールに競合があります</li><li><em> ジャーニーX</em>のオーディエンス重複の競合を表示する</li></ul> |
| Journey Agent | ジャーニー管理 | <ul><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li></ul> | 25 | <ul><li><em> ライブジャーニーはいくつありますか？</em></li><li><em> オーディエンス X.</em>を使用するすべてのジャーニーを一覧表示する</li><li><em>現在テストモードにあるすべてのジャーニーを一覧表示</em></li></ul> |
| 製品サポート担当者 | ナレッジベースのトラブルシューティング | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2CおよびB2B エディション）</li><li>Customer Journey Analytics（B2CおよびB2B エディション）</li></ul> | 0 | <ul><li><em> ライセンス使用状況ダッシュボードとExperience Platform ホームページでプロファイル数が異なるのはなぜですか？</em></li><li><em> ジャーニーがトリガーされない理由は何ですか？</em></li><li><em>Adobe Experience Platformでは、リアルタイムのエクスペリエンスをどのように構築できますか？</em></li><li><em>Adobe Experience Platformでアラートを設定および使用する方法は？</em></li><li><em>Adobe Experience Platform アクティベーションの平均プロファイルリッチネス制限は何ですか？</em></li></ul> |
| 製品サポート担当者 | サポートケースの作成と追跡 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2CおよびB2B エディション）</li><li>Customer Journey Analytics（B2CおよびB2B エディション）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em>失敗したセグメント化ジョブの新しいサポートチケットを作成</em></li><li><em>E-001772068 チケットのステータスは？</em></li></ul> |
| Content Advisor エージェント | コンテンツ発見 | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>WKND オファーキャンペーンを作成するためのコンテンツフラグメントを表示します。</em></li><li><em>製品パッケージ PNG画像を検索します。</em></li><li><em>WKND フォルダー内のOffice タグ付きの画像を表示します。</em></li><li><em> フォルダーWKNDにsvgsがありますか？</em></li><li><em>すべてのローン申し込みフォームを表示します。</em></li><li><em>従業員のオンボーディングフォームを探しています。</em></li></ul> |
| Content Advisor エージェント | <ul><li>コンテンツの最適化</li></ul> | <ul><li>Adobe Experience Manager AssetsとDynamic Media</li></ul> | 10 | <ul><li><em>80%の画質で2000 pxのレンディションをJPEGとして作成します。</em></li><li><em>Instagram ストーリーのレンディションを作成します。</em></li><li><em> プロモーションバナーの上に30%割引のグラフィックで画像をオーバーレイし、中央から100 px配置します。</em></li><li><em>PNGの背景色を#ff8932に変更します。</em></li></ul> |
| Brand Governance エージェント | <ul><li>ブランドポリシーチェック</li></ul><ul><li>Content Hubでの権限</li></ul><ul><li>アセットの有効期限</li></ul> | <ul><li>Adobe Experience Manager Sites（ブランドポリシー）</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em>このページはブランドと一致していますか？`https://www.website/en.html`</em></li><li><em>既存のすべてのContent Hub ABAC ルールを表示</em></li><li><em> アセットの有効期限がまもなく切れますか？</em></li></ul> |
| Brand Experience Agent | <ul><li>コンテンツの更新</li><li>Formsによる制作</li><li>パイプラインのトラブルシューティング</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>`URL`に、見出しをHello world</em>に更新します</li><li><em>名前、電子メール、メッセージフィールドを使用して連絡先フォームを作成する</em></li><li><em>失敗したパイプラインのトラブルシューティング </em></li><li><em>失敗したパイプラインをメイン プログラムに一覧表示します。</em></li></ul> |
| Brand Experience Agent | サイトの近代化 | Adobe Experience Manager Cloud Services | 100 | <ul><li><em> ページを移行`https://wknd-trendsetters.site`</em></li></ul> |

>[!NOTE]
>
>実際のAIのクレジット消費量は、実行されるステップの数と1 ステップあたりのイテレーションによって異なる場合があります。

## このトピックの詳細ヘルプ

* [CX エンタープライズにおける生成AI](/help/interface/features/generative-ai.md)
* [CX エンタープライズにおけるAgentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform Agents利用制限トライアル](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
