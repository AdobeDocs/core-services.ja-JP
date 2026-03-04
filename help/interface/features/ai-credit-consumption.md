---
title: エージェントジョブと AI クレジット消費
description: Experience Cloud アプリケーションでのエージェントジョブと AI クレジット消費率について説明します。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: 1897e2162ba53ebc43a78877a61ebf4370127631
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 3%

---

# Adobe Experience Platform Agent のジョブと AI クレジットの使用

更新日：**2026 年 3 月 4 日**

Experience Cloud アプリケーションでの Agentic AI ジョブと AI クレジットの使用について説明します。 既存のExperience Cloud アプリケーションで Agentic AI 機能を有効にする方法については、[Experience Cloudの Agentic AI](agentic-ai.md#existing-apps) を参照してください。

## エージェントジョブ

_エージェントジョブ_ とは、お客様からの入力に応じて、特定の結果を達成するためにエージェントが実行する一連のタスクとアクションです。

AI アシスタントを使用して自然言語プロンプトを使用すると、エージェントに特定のジョブを実行するように依頼できます。 これらの入力に基づいて、Agent Orchestratorは適切なエージェントを調整し、関連するExperience Cloud アプリケーション内で各ステップを実行します。

## AI クレジット

_AI クレジット_ は、エージェントジョブの実行を定量化する、使用状況ベースの指標です。 AI クレジットは [AI ファーストのアプリケーション ](/help/interface/features/agentic-ai.md) には適用されません。

## AI クレジット消費

AI クレジットの使用状況は、実行されるジョブの複雑さと価値に応じて異なる場合があります。

* シンプル（多くの場合、1 つの手順）タスクの方が消費するクレジットが少ない
* 複雑な（多くの場合、複数の手順を踏んだ）タスクの場合は、より多くのクレジットが消費されます
* 高度な推論、検証、複数エージェントの調整、または統合を含むタスクは、より多くのクレジットを消費します

### 推定 AI 信用消費率

| 代理人 | ジョブ | サポートされるアプリケーション | 推定 AI クレジット | サンプルプロンプト |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience Agent | オーディエンス/アカウントの作成 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 50 | <ul><li>_裕福な買い手のフィールドを表示_</li><li>_顧客の環境設定に関連するすべてのフィールドを検索_</li></ul> |
| Audience Agent | ナレッジベースのオーディエンス/アカウントの作成 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 150 | <ul><li>_カリフォルニアに住むユーザーで構成されるオーディエンスを作成_</li><li>_今四半期に 1,000 ドルを超えたVIP メンバーのオーディエンスを生成_</li><li>_過去 60 日以内に衣料品を購入しても購入していないユーザーのオーディエンスを作成する_</li></ul> |
| Audience Agent | Audience/アカウント管理 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li>_オーディエンスの重複はありますか？_</li><li>_最大 5 人のオーディエンスを表示_</li><li>_どの宛先にもアクティブ化されていないオーディエンスの表示_</li><li>_ライブジャーニーで使用されるすべてのオーディエンスをリストします_</li></ul> |
| Audience Agent | オーディエンス/アカウント分析 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li>_過去 1 週間にサイズが 20% 以上増加したオーディエンスはどれですか？_</li><li>_オーディエンス「ロイヤルティプラチナ」は 30 日前の値と比較してどのくらい変化しましたか？_</li><li>_最も急速に成長しているオーディエンスは何ですか？_</li></ul> |
| Audience Agent | 購買グループのアイディエーション | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li>_これらの製品の意図を示しているのはどのアカウントですか？_</li><li>_XYZ の製品目的別の上位担当者を表示します。_</li><li>_5 人以上の購買グループは_</li></ul> |
| Data Insights Agent | データの分析とビジュアライゼーション | <ul><li>Customer Journey Analytics（B2C と B2B のエディション）</li></ul> | 25 | <ul><li>_7 月のトレンドオーダー_</li><li>_売上高を地域別に表示_</li><li>_3 月から 6 月の男女別の注文を表示します_。</li><li>_6 月の利益別の上位 10 位の SKU は_</li><li>_月別購入割合_</li><li>_製品カテゴリ別の売上高のシェア_</li></ul> |
| Journey Agent | ジャーニー念慮 | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li>_Web サイト上のコンテンツに関与する人々に焦点を当て、私のソリューションを目的とした空白アカウントのジャーニーを作成します_</li></ul> |
| Journey Agent | ジャーニーの作成 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 30 | <ul><li>_過去 7 日間に最初の購入を完了していないユーザーにリマインダーを送信するジャーニーを生成_</li><li>_ユーザーが最初の購入を完了したら、3 日後にメールで SMS 確認とフォローアップ特典の説明を送信します_</li></ul> |
| Journey Agent | ジャーニー分析 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 50 | <ul><li>_7 月キャンペーンの 4 番目のジャーニーのノード別のフォールアウトを分析します。_</li><li>_ジャーニー X にスケジュールの競合はありますか_</li><li>_ジャーニー X のオーディエンス重複の競合を表示_</li></ul> |
| Journey Agent | ジャーニー管理 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> | 25 | <ul><li>_ライブジャーニーは何件ありますか？_</li><li>_オーディエンス X を使用するすべてのジャーニーをリストします。_</li><li>_現在テストモードにあるすべてのジャーニーをリストします_</li></ul> |
| 製品サポート担当者 | ナレッジベースのトラブルシューティング | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2C と B2B のエディション）</li><li>Customer Journey Analytics（B2C と B2B のエディション）</li></ul> | 0 | <ul><li>_プロファイル数がライセンス使用状況ダッシュボードとExperience Platform ホームページで異なるのはなぜですか？_</li><li>_ジャーニーがトリガーされない理由は何ですか？_</li><li>_Adobe Experience Platformは、リアルタイムエクスペリエンスをどのように作成しますか？_</li><li>_Adobe Experience Platformでは、アラートをどのように設定して使用しますか？_</li><li>_Adobe Experience Platform アクティベーションの平均プロファイル充実制限とは_</li></ul> |
| 製品サポート担当者 | サポートケースの作成とトラッキング | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li>Adobe Journey Optimizer（B2C と B2B のエディション）<li>Customer Journey Analytics（B2C と B2B のエディション）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>_失敗したセグメント化ジョブの新しいサポートチケットを作成する_</li><li>_チケット E-001772068 のステータスを教えてください。_</li></ul> |
| コンテンツ アドバイザーエージェント | コンテンツ検出 | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li>_WKND オファーキャンペーン作成用のコンテンツフラグメントを表示します_。</li><li>_製品パッケージの PNG 画像を検索します_。</li><li>_Office タグ付き画像をフォルダー WKND に表示します。_</li><li>_フォルダー WKND に svg はありますか？_</li><li>_すべてのローン申し込みフォームを表示する_</li><li>_従業員のオンボーディングフォームを探しています。_</li></ul> |
| コンテンツ アドバイザーエージェント | <ul><li>コンテンツの最適化</li></ul> | <ul><li>Adobe Experience Manager Assetsと Dynamic Media</li></ul> | 10 | <ul><li>_80% の画質で、2000 px のレンディションをJPEGとして作成します。_</li><li>_Instagram ストーリーのレンディションの作成_</li><li>_プロモーションバナーの上に 30% 割引のグラフィックを重ねて、中央から 100 ピクセル配置します。_</li><li>_PNG の背景色を#ff8932 に変更します。_</li></ul> |
| ブランドガバナンスエージェント | <ul><li>ブランドポリシーチェック</li></ul><ul><li>Content Hubを使用した権限</li></ul><ul><li>パイプラインのトラブルシューティング</li></ul> | <ul><li>Adobe Experience Manager Sites（ブランドポリシー）</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li>_このページはブランドと連携していますか？`https://www.website/en.html`_</li><li>_既存のContent Hub ABAC ルールをすべて表示_</li><li>_アセットの有効期限が間もなく切れることはありますか？_</li></ul> |
| Brand Experience エージェント | <ul><li>コンテンツの更新</li><li>Formsの作成</li><li>パイプラインのトラブルシューティング</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li>_名前、メール、メッセージのフィールドを含む連絡先フォームを作成する_</li><li>_失敗したパイプラインのトラブルシューティング_</li><li>_失敗したパイプラインをメインプログラムにリストします_。</li></ul> |

>[!NOTE]
>
>実際の AI クレジット消費は、実行されたステップの数と、ステップごとの繰り返し回数によって異なる場合があります。

## このトピックに関するその他のヘルプ

* [Experience Cloudの Agentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform エージェントの使用にバインドされた体験版 ](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
