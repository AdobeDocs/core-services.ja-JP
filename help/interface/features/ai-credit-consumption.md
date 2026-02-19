---
title: エージェントジョブと AI クレジット消費
description: Experience Cloud アプリケーションでのエージェントジョブと AI クレジット消費率について説明します。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: bb6adf13bed37d4a885b5baec28199efade592e1
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 2%

---

# Adobe Experience Platform Agent のジョブと AI クレジットの使用

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
| ------ |-----|------------------------|----------------------|----------------|
| Audience Agent | オーディエンス/アカウントの作成 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 50 | <ul><li>裕福な購買者向けのフィールドを表示する</li><li>顧客の環境設定に関連するすべてのフィールドを検索</li></ul> |
| Audience Agent | ナレッジベースのオーディエンス/アカウントの作成 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 150 | <ul><li>カリフォルニアに住む人々で構成されるオーディエンスを作成</li><li>今四半期に 1000 ドルを超えたVIP メンバーのオーディエンスを生成します</li><li>過去 60 日間に衣料品を購入したものの購入していないユーザーのオーディエンスを作成します</li></ul> |
| Audience Agent | Audience/アカウント管理 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li>オーディエンスの重複はありますか？</li><li>最大 5 人のオーディエンスを表示します。</li><li>どの宛先にもアクティブ化されていないオーディエンスの表示</li><li>ライブジャーニーで使用されるすべてのオーディエンスをリストします</li></ul> |
| Audience Agent | オーディエンス/アカウント分析 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li>先週、サイズが 20% 以上増加したオーディエンスはどれですか？</li><li>オーディエンス「ロイヤルプラチナ」は 30 日前の値と比較してどのくらい変化しましたか？</li><li>最も急速に成長しているオーディエンスは何ですか？</li></ul> |
| Audience Agent | 購買グループのアイディエーション | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li>これらの製品の意図を示しているのは、どのアカウントですか？</li><li>XYZ の製品目的別の上位担当者を表示します。</li><li>5 人以上のメンバーがいる購買グループは？</li></ul> |
| Data Insights Agent | データの分析とビジュアライゼーション | <ul><li>Customer Journey Analytics（B2C と B2B のエディション）</li></ul> | 25 | <ul><li>7 月の注文のトレンド</li><li>売上高を地域別に表示します。</li><li>3 月から 6 月の間、性別ごとに注文を表示します。</li><li>6 月の利益別の上位 10 位の SKU は何でした</li><li>月別の購入率</li><li>製品カテゴリ別売上高のシェア</li></ul> |
| Journey Agent | ジャーニー念慮 | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li>Web サイト上のコンテンツに関与する人々に焦点を当て、私のソリューションを目的としたホワイトスペースアカウントのジャーニーを作成します</li></ul> |
| Journey Agent | ジャーニーの作成 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 30 | <ul><li>ジャーニーを生成して、過去 7 日間に最初の購入を完了していないユーザーにリマインダーを送信します</li><li>ユーザーが最初の購入を完了したら、3 日後に SMS 確認とフォローアップ特典の説明をメールで送信します</li></ul> |
| Journey Agent | ジャーニー分析 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 50 | <ul><li>7 月のキャンペーンの 4 番目のジャーニーのノード別のフォールアウトを分析します。</li><li>ジャーニー X にスケジュールの競合はありますか？</li><li>ジャーニー X のオーディエンス重複の競合を表示</li></ul> |
| Journey Agent | ジャーニー管理 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 25 | <ul><li>ライブジャーニーの数</li><li>オーディエンス X を使用するすべてのジャーニーをリストします。</li><li>現在テストモードにあるすべてのジャーニーをリストします</li></ul> |
| 製品サポート担当者 | ナレッジベースのトラブルシューティング | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C と B2B のエディション）</li><li>Customer Journey Analytics（B2C と B2B のエディション）</li></ul> | 0 | <ul><li>プロファイル数がライセンス使用状況ダッシュボードとExperience Platform ホームページで異なるのはなぜですか？</li><li>ジャーニーがトリガーされない理由は何ですか。</li><li>Adobe Experience Platformはリアルタイムエクスペリエンスをどのように作成しますか？</li><li>Adobe Experience Platformでは、アラートをどのように設定および使用しますか？</li><li>Adobe Experience Platform アクティベーションの平均プロファイル充実制限とは何ですか？</li></ul> |
| 製品サポート担当者 | サポートケースの作成とトラッキング | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li>Adobe Journey Optimizer（B2C と B2B のエディション）<li>Customer Journey Analytics（B2C と B2B のエディション）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>失敗したセグメント化ジョブの新しいサポートチケットを作成する</li><li>チケットの E-001772068 ールのステータスは？</li></ul> |
| コンテンツ アドバイザーエージェント | コンテンツ検出 | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 5 | <ul><li>WKND オファーキャンペーン作成用のコンテンツフラグメントを表示します。</li><li>製品パッケージの PNG 画像を検索します。</li><li>Office タグ付き画像をフォルダー WKND に表示します。</li><li>WKND フォルダーに svg はありますか？</li><li>すべてのローン申し込みフォームを表示します。</li><li>従業員のオンボーディングフォームを探しています。</li></ul> |
| コンテンツ アドバイザーエージェント | <ul><li>コンテンツの更新</li><li>コンテンツの最適化</li><li>Formsの作成</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 10 | <ul><li>80% の画質で 2,000 px のレンディションをJPEGとして作成します。</li><li>Instagram ストーリーのレンディションを作成します。</li><li>プロモーションバナーの上に 30% 割引のグラフィックを重ねて、中央から 100 px 配置します。</li><li>PNG の背景色を#ff8932 に変更します。</li></ul> |
| Brand Experience エージェント | <ul><li>Experience サポート</li><li>デプロイメントサポート</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 5 | <ul><li>失敗したパイプラインのトラブルシューティング</li><li>メインプログラムの失敗したパイプラインを一覧表示します。</li><li>失敗した「開発パイプライン」というパイプラインを分析します。</li><li>パイプライン実行 1234567 のトラブルシューティング</li></ul> |
| Brand Experience エージェント | サイトの最新化 | Adobe Experience Manager Cloud Services | 100 | <ul><li>ページ https://wknd-trendsetters.siteを移行します。</li></ul> |

>[!NOTE]
>
>実際の AI クレジット消費は、実行されたステップの数と、ステップごとの繰り返し回数によって異なる場合があります。

## このトピックに関するその他のヘルプ

* [Experience Cloudの Agentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform エージェントの使用にバインドされた体験版 &#x200B;](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)