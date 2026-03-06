---
title: エージェントジョブと AI クレジット消費
description: Experience Cloud アプリケーションでのエージェントジョブと AI クレジット消費率について説明します。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: 6a7cd999ec96967084c67d059cb2efd6a3235235
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 3%

---

# Adobe Experience Platform Agent のジョブと AI クレジットの使用

更新日：**2026 年 3 月 5 日**

Experience Cloud アプリケーションでの Agentic AI ジョブと AI クレジットの使用について説明します。 既存のExperience Cloud アプリケーションで Agentic AI 機能を有効にする方法については、[Experience Cloudの Agentic AI](agentic-ai.md#existing-apps) を参照してください。

## エージェントジョブ

_エージェントジョブ_ とは、お客様からの入力に応じて、特定の結果を達成するためにエージェントが実行する一連のタスクとアクションです。

AI アシスタントを使用して自然言語プロンプトを使用すると、エージェントに特定のジョブを実行するように依頼できます。 これらの入力に基づいて、Agent Orchestratorは適切なエージェントを調整し、関連するExperience Cloud アプリケーション内で各ステップを実行します。

## AI クレジット

_AI クレジット_ は、エージェントジョブの実行を定量化する、使用状況ベースの指標です。 AI クレジットは [AI ファーストのアプリケーション &#x200B;](/help/interface/features/agentic-ai.md) には適用されません。

## AI クレジット消費

AI クレジットの使用状況は、実行されるジョブの複雑さと価値に応じて異なる場合があります。

* シンプル（多くの場合、1 つの手順）タスクの方が消費するクレジットが少ない
* 複雑な（多くの場合、複数の手順を踏んだ）タスクの場合は、より多くのクレジットが消費されます
* 高度な推論、検証、複数エージェントの調整、または統合を含むタスクは、より多くのクレジットを消費します

### 推定 AI 信用消費率

| 代理人 | ジョブ | サポートされるアプリケーション | 推定 AI クレジット | サンプルプロンプト |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience Agent | オーディエンス/アカウントの作成 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 50 | <ul><li><em> 裕福な買い手のフィールドを表示 </em></li><li><em> 顧客の環境設定に関連するすべてのフィールドを検索 </em></li></ul> |
| Audience Agent | ナレッジベースのオーディエンス/アカウントの作成 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 150 | <ul><li><em> カリフォルニアに住むユーザーで構成されるオーディエンスを作成 </em></li><li><em> 今四半期に 1,000 ドルを超えたVIP メンバーのオーディエンスを生成 </em></li><li><em> 過去 60 日以内に衣料品を購入しても購入していないユーザーのオーディエンスを作成する </em></li></ul> |
| Audience Agent | Audience/アカウント管理 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li><em> オーディエンスの重複はありますか？</em></li><li><em> 最大 5 人のオーディエンスを表示 </em></li><li><em> どの宛先にもアクティブ化されていないオーディエンスの表示 </em></li><li><em> ライブジャーニーで使用されるすべてのオーディエンスをリストします </em></li></ul> |
| Audience Agent | オーディエンス/アカウント分析 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li><em> 過去 1 週間にサイズが 20% 以上増加したオーディエンスはどれですか？</em></li><li><em> オーディエンス「ロイヤルティプラチナ」は 30 日前の値と比較してどのくらい変化しましたか？</em></li><li><em> 最も急速に成長しているオーディエンスは何ですか？</em></li></ul> |
| Audience Agent | 購買グループのアイディエーション | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li><em> これらの製品の意図を示しているのはどのアカウントですか？</em></li><li><em>XYZ の製品目的別の上位担当者を表示します。</em></li><li><em>5 人以上の購買グループは </em></li></ul> |
| Data Insights Agent | データの分析とビジュアライゼーション | <ul><li>Customer Journey Analytics（B2C と B2B のエディション）</li></ul> | 25 | <ul><li><em>7 月のトレンドオーダー </em></li><li><em> 売上高を地域別に表示 </em></li><li><em>3 月から 6 月の男女別の注文を表示します </em>。</li><li><em>6 月の利益別の上位 10 位の SKU は </em></li><li><em> 月別購入割合 </em></li><li><em> 製品カテゴリ別の売上高のシェア </em></li></ul> |
| Journey Agent | ジャーニー念慮 | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li><em>Web サイト上のコンテンツに関与する人々に焦点を当て、私のソリューションを目的とした空白アカウントのジャーニーを作成します </em></li></ul> |
| Journey Agent | ジャーニーの作成 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 30 | <ul><li><em> 過去 7 日間に最初の購入を完了していないユーザーにリマインダーを送信するジャーニーを生成 </em></li><li><em> ユーザーが最初の購入を完了したら、3 日後にメールで SMS 確認とフォローアップ特典の説明を送信します </em></li></ul> |
| Journey Agent | ジャーニー分析 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 50 | <ul><li><em>7 月キャンペーンの 4 番目のジャーニーのノード別のフォールアウトを分析します。</em></li><li><em> ジャーニー X にスケジュールの競合はありますか </em></li><li><em> ジャーニー X のオーディエンス重複の競合を表示 </em></li></ul> |
| Journey Agent | ジャーニー管理 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 25 | <ul><li><em> ライブジャーニーは何件ありますか？</em></li><li><em> オーディエンス X を使用するすべてのジャーニーをリストします。</em></li><li><em> 現在テストモードにあるすべてのジャーニーをリストします </em></li></ul> |
| 製品サポート担当者 | ナレッジベースのトラブルシューティング | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C と B2B のエディション）</li><li>Customer Journey Analytics（B2C と B2B のエディション）</li></ul> | 0 | <ul><li><em> プロファイル数がライセンス使用状況ダッシュボードとExperience Platform ホームページで異なるのはなぜですか？</em></li><li><em> ジャーニーがトリガーされない理由は何ですか？</em></li><li><em>Adobe Experience Platformは、リアルタイムエクスペリエンスをどのように作成しますか？</em></li><li><em>Adobe Experience Platformでは、アラートをどのように設定して使用しますか？</em></li><li><em>Adobe Experience Platform アクティベーションの平均プロファイル充実制限とは </em></li></ul> |
| 製品サポート担当者 | サポートケースの作成とトラッキング | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C と B2B のエディション）</li><li>Customer Journey Analytics（B2C と B2B のエディション）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em> 失敗したセグメント化ジョブの新しいサポートチケットを作成する </em></li><li><em> チケット E-001772068 のステータスを教えてください。</em></li></ul> |
| コンテンツ アドバイザーエージェント | コンテンツ検出 | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>WKND オファーキャンペーン作成用のコンテンツフラグメントを表示します </em>。</li><li><em> 製品パッケージの PNG 画像を検索します </em>。</li><li><em>Office タグ付き画像をフォルダー WKND に表示します。</em></li><li><em> フォルダー WKND に svg はありますか？</em></li><li><em> すべてのローン申し込みフォームを表示する </em></li><li><em> 従業員のオンボーディングフォームを探しています。</em></li></ul> |
| コンテンツ アドバイザーエージェント | <ul><li>コンテンツの最適化</li></ul> | <ul><li>Adobe Experience Manager Assetsと Dynamic Media</li></ul> | 10 | <ul><li><em>80% の画質で、2000 px のレンディションをJPEGとして作成します。</em></li><li><em>Instagram ストーリーのレンディションの作成 </em></li><li><em> プロモーションバナーの上に 30% 割引のグラフィックを重ねて、中央から 100 ピクセル配置します。</em></li><li><em>PNG の背景色を#ff8932 に変更します。</em></li></ul> |
| ブランドガバナンスエージェント | <ul><li>ブランドポリシーチェック</li></ul><ul><li>Content Hubを使用した権限</li></ul><ul><li>アセットの有効期限</li></ul> | <ul><li>Adobe Experience Manager Sites（ブランドポリシー）</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em> このページはブランドと連携していますか？`https://www.website/en.html`</em></li><li><em> 既存のContent Hub ABAC ルールをすべて表示 </em></li><li><em> アセットの有効期限が間もなく切れることはありますか？</em></li></ul> |
| Brand Experience エージェント | <ul><li>コンテンツの更新</li><li>Formsの作成</li><li>パイプラインのトラブルシューティング</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>`URL` に、ヘッドラインを Hello world に更新してください </em></li><li><em> 名前、メール、メッセージのフィールドを含む連絡先フォームを作成する </em></li><li><em> 失敗したパイプラインのトラブルシューティング </em></li><li><em> 失敗したパイプラインをメインプログラムにリストします </em>。</li></ul> |
| Brand Experience エージェント | サイトの最新化 | Adobe Experience Manager Cloud Services | 100 | <ul><li><em> ページを移行する `https://wknd-trendsetters.site`</em></li></ul> |

>[!NOTE]
>
>実際の AI クレジット消費は、実行されたステップの数と、ステップごとの繰り返し回数によって異なる場合があります。

## このトピックに関するその他のヘルプ

* [Experience Cloudでの GenAI](/help/interface/features/generative-ai.md)
* [Experience Cloudの Agentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform エージェントの使用にバインドされた体験版 &#x200B;](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
