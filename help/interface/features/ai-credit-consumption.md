---
title: エージェントジョブと AI クレジット消費
description: Experience Cloud アプリケーションでのエージェントジョブと AI クレジット消費について説明します。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: 623bb6e240987cb2ff76bce3488b827b901b84db
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 7%

---


# エージェントジョブと AI クレジット消費

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

### 推定 AI クレジット消費率

| 代理人 | ジョブ | サポート対象アプリケーション | 推定 AI クレジット |
|------|-----|------------------------|----------------------|
| Audience Agent | オーディエンス / アカウントアイデア | Real-Time CDP、Adobe Journey Optimizer | 50 |
| Audience Agent | ナレッジベースのオーディエンス/アカウントの作成 | Real-Time CDP、Adobe Journey Optimizer | 150 |
| Audience Agent | オーディエンス / アカウント管理 | Real-Time CDP、Adobe Journey Optimizer | 25 |
| Audience Agent | オーディエンス/アカウント分析 | Real-Time CDP、Adobe Journey Optimizer | 25 |
| Audience Agent | 購買グループのアイディエーション | Adobe Journey Optimizer（B2B） | 25 |
| Data Insights Agent | データの分析とビジュアライゼーション | Customer Journey Analytics | 25 |
| Data Insights Agent | Data storytellingと共有 | Customer Journey Analytics | 100 |
| Journey Agent | ジャーニー念慮 | Adobe Journey Optimizer（B2B） | 25 |
| Journey Agent | ジャーニーの作成 | Adobe Journey Optimizer（B2B、B2C） | 30 |
| Journey Agent | ジャーニー分析 | Adobe Journey Optimizer（B2B、B2C） | 50 |
| Journey Agent | ジャーニー管理 | Adobe Journey Optimizer（B2B、B2C） | 25 |
| 製品サポート担当者 | ナレッジベースのトラブルシューティング | 複数のExperience Cloud アプリケーション | 0 |
| 製品サポート担当者 | サポートケースの作成とトラッキング | 複数のExperience Cloud アプリケーション | 10 |
| コンテンツ アドバイザーエージェント | コンテンツ検出 | Adobe Experience Manager Cloud Services | 5 |
| コンテンツ アドバイザーエージェント | コンテンツの更新と最適化 | Adobe Experience Manager Cloud Services | 10 |
| Brand Experience エージェント | デプロイメントサポート | Adobe Experience Manager Cloud Services | 5 |
| Brand Experience エージェント | サイトの最新化 | Adobe Experience Manager Cloud Services | 100 |

**注意：** 実際の AI クレジット消費は、実行されたステップ数とステップあたりのイテレーション数によって異なる場合があります。

