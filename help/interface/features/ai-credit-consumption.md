---
title: エージェントジョブと AI クレジット消費
description: Experience Cloud アプリケーションでのエージェントジョブと AI クレジット消費について説明します。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: b761697ad1eb14e06ea3f6c868833c4e6c51eac3
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 12%

---

# エージェントジョブと AI クレジット消費

Experience Cloud アプリケーションでの Agentic AI ジョブと AI クレジットの使用について説明します。

## エージェントジョブ

**エージェントジョブ** は、お客様からの入力に応じて、特定の結果を達成するためにエージェントが実行する一連のタスクとアクションです。

AI アシスタントを使用した自然言語プロンプトを使用して、お客様はエージェントに特定のジョブを実行するように依頼できます。 これらの入力に基づいて、Agent Orchestratorは適切なエージェントを調整し、関連するExperience Cloud アプリケーション内で各ステップを実行します。

## AI クレジット

**AI クレジット** は、エージェントジョブの実行を定量化する、使用状況ベースの指標です。 AI クレジットは AI ファーストのアプリケーションには適用されません。

## AI クレジット消費

AI クレジットの使用状況は、実行されるジョブの複雑さと値によって異なる場合があります。

* シンプル（多くの場合、1 つの手順）タスクの方が消費するクレジットが少ない
* 複雑な（多くの場合、複数の手順を踏んだ）タスクの場合は、より多くのクレジットが消費されます
* 高度な推論、検証、複数エージェントの調整、または統合を含むタスクは、より多くのクレジットを消費します

### 推定 AI 信用消費率

| 代理人 | ジョブ | サポートされるアプリケーション | 推定 AI クレジット |
|------|-----|------------------------|----------------------|
| Audience Agent | オーディエンス / アカウントアイデア | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 50 |
| Audience Agent | ナレッジベースのオーディエンス/アカウントの作成 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 150 |
| Audience Agent | オーディエンス / アカウント管理 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 25 |
| Audience Agent | オーディエンス/アカウント分析 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 25 |
| Audience Agent | 購買グループのアイディエーション | <ul><li>Adobe Journey Optimizer（B2B）</li></ul> | 25 |
| Data Insights Agent | データの分析とビジュアライゼーション | <ul><li>Customer Journey Analytics</li></ul> | 25 |
| Data Insights Agent | Data storytellingと共有 | <ul><li>Customer Journey Analytics</li></ul> | 100 |
| Journey Agent | ジャーニー念慮 | <ul><li>Adobe Journey Optimizer（B2B）</li></ul> | 25 |
| Journey Agent | ジャーニーの作成 | <ul><li>Adobe Journey Optimizer（B2B、B2C）</li></ul> | 30 |
| Journey Agent | ジャーニー分析 | <ul><li>Adobe Journey Optimizer（B2B、B2C）</li></ul> | 50 |
| Journey Agent | ジャーニー管理 | <ul><li>Adobe Journey Optimizer（B2B、B2C）</li></ul> | 25 |
| 製品サポート担当者 | ナレッジベースのトラブルシューティング | <ul><li>複数のExperience Cloud アプリケーション</li></ul> | 0 |
| 製品サポート担当者 | サポートケースの作成とトラッキング | <ul><li>複数のExperience Cloud アプリケーション</li></ul> | 10 |
| コンテンツ アドバイザーエージェント | コンテンツ検出 | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 5 |
| コンテンツ アドバイザーエージェント | コンテンツの更新と最適化 | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 10 |
| Brand Experience エージェント | デプロイメントサポート | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 5 |
| Brand Experience エージェント | サイトの最新化 | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 100 |

>[!NOTE]
>
>実際の AI クレジット消費は、実行されたステップの数と、ステップごとの繰り返し回数によって異なる場合があります。
