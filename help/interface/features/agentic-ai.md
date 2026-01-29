---
title: Experience Cloud アプリケーションの Agentic AI
description: Experience Cloud アプリケーションで Agentic AI を使用できる場所について説明します。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
hidefromtoc: true
index: false
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: da7a2a9e9aa8365288fa6e05afb6485e4c33ccb2
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 3%

---

# Adobe Experience Cloudの Agentic AI

更新日：**2026 年 1 月 29 日**

Adobe Experience Platform エージェントは、Experience Platform [Agent Orchestrator](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/home) を使用して、Experience Cloud アプリケーションにエージェントベースの機能を追加します。

これらのエージェントは、タスクの自動化、インサイトの迅速な提供、ワークフローの合理化に役立ちます。 その結果、チームはより効率的に作業し、Experience Cloudからより多くの価値を得ることができます。

Experience Cloudの AI エージェントには、次のいずれかでアクセスできます。

* [既存のExperience Cloud アプリケーション](#existing-apps)
* [AI ファーストのExperience Cloudアプリケーション](#ai-first-apps)

次の節では、Experience Cloudで Agentic AI を有効にする方法について説明します。

## 既存のExperience Cloud アプリケーション {#existing-apps}

既存のアプリケーションでは、自然言語を使用して、[AI アシスタント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/home) 対話型インターフェイスを通じてAdobe Experience Platform Agents に指示できます。 AI アシスタントは、全画面表示と右パネル表示の両方で使用できます。

次のいずれかのカテゴリに属するお客様は、既存のExperience Cloud アプリでエージェントを有効にすることができます。

* Adobe Experience Platform Agents AI クレジットライセンスの購入
* 使用量に制限された体験版に含まれる（AI クレジットは限定的に提供）
* Agent Orchestrator プロモ SKU のトランザクション（時間限定トライアルライセンス）

AI エージェントを使用して _エージェントジョブ_ を実行する場合は、AI クレジットを使用します。 [&#x200B; エージェントジョブと AI クレジット消費 &#x200B;](/help/interface/features/ai-credit-consumption.md) で説明します。

AI エージェントは _あなたの_ 入力、監督に従い、製品レベルのアクセス制御を尊重します。 ジョブの実行や、基になるExperience Cloud製品での使用が許可されているデータへのアクセスのみ可能です。

### 既存のExperience Cloud アプリ内の AI エージェント {#existing-apps-table}

次の表に、既存のExperience Platform アプリケーションで使用できるExperience Cloud エージェントを示します。

| エージェント名 | 機能 | サポートされるアプリケーション |
|---|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 自然言語プロンプトを使用してオーディエンスを作成、管理および最適化し、より簡単で効率の高い、市場投入までの時間を短縮する権限をチームに与えます。 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> |
| **コンテンツ アドバイザーエージェント** | <ul><li>[&#x200B; コンテンツ検出 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/agents/discovery/overview)：シンプルな自然言語プロンプトで、画像、ビデオ、テキストベースのドキュメント、コンテンツフラグメント、フォーム全体でExperience Manager コンテンツを即座に検出し表示することで、オーサリングを迅速化し、検出を強化します。</li><li>[&#x200B; コンテンツの最適化 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-optimization/overview)：自然言語プロンプトを使用して、ソースアセットから視覚的なコンテンツのバリアントを簡単に作成します。</li><li>[&#x200B; エクスペリエンスの実稼働 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/agents/production/overview):CMSで大量のタスクを自動的に実行します。 このエージェントは、手動の長いプロセスを、すべてのエクスペリエンスを最新かつ一貫性のある状態に保つ、AI を利用した高速ワークフローに変え、ビジネスの目標達成を支援します。</li></ul> | <ul><li>Adobe Experience Manager（コンテンツ検出）</li></ul><ul><li>Dynamic Media と OpenAPI のAdobe Experience Manager（コンテンツ最適化）</li></ul><ul><li>Adobe Experience Manager Cloud Services およびEdge Delivery Services（エクスペリエンス実稼働） </li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | データに関する質問にすばやく回答します。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。 | <ul><li>Customer Journey Analytics（B2B と B2C のエディション）</li></ul> |
| **Brand Experience Agent** | [&#x200B; デプロイメントサポート &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/agents/development/overview):AEM CS 開発者と技術管理者が、根本原因を分析して修正を提案することで、Cloud Manager パイプラインのビルドステップエラーをトラブルシューティングするのに役立ちます。 | <ul><li>AEM Cloud Service およびAdobe Managed Servicesの AI アシスタント</li></ul> |
| **ブランドガバナンスエージェント*** | [&#x200B; ブランドガバナンス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview):Experience Manager全体にセキュリティ、規制、ブランドポリシーを適用して、ブランドの整合性とコンプライアンスを保護します。 このエージェントは、視覚的およびメッセージング標準を維持するためにブランドガバナンスを適用します。 アクセスとコンテンツの変更を管理するために詳細な権限を使用し、ライセンスと使用の制約を維持するために DRM を組み込みます。 | <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms</li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | チームがマルチタッチのカスタマージャーニーを大規模にすばやく作成、分析、最適化できるようにします。 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> |
| [&#x200B; 製品サポート担当者 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/new-features/customer-support) | ワークフローを離れることなくサポートの問題をトラブルシューティングしたり、カスタマーサポートチケットを作成したり、AI アシスタントを使用してケースの進行状況を追跡したりできます。 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li><li>Adobe Journey OptimizerB2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

アスタリスク （*）：このエージェントは、エクスプローラープログラムを使用しているお客様がアクセスできます。 エクスプローラープログラムは、Adobeの最新の高度な機能に早期にアクセスできるようにする招待専用プログラムです。 詳しくは、アカウント担当者にお問い合わせください。

## AI ファーストのExperience Cloudアプリケーション {#ai-first-apps}

AI ファーストのアプリケーションは、ジェネレーティブまたはアジェンティック Al をコアとして構築されています。 彼らは主要なタスクにジェネレーティブまたは Agentic Al を使用し、Agentic 機能はすでに Al-first アプリケーションライセンスに含まれています。 そのため、Experience Platform Agent Orchestrator ライセンスは必要ありません。

次の表に、Al-first アプリケーションとして使用できるExperience Platform エージェントを示します。 これらは、次の Al-first アプリケーションのライセンスを取得することで有効になります。

| エージェント名 | 機能 | サポートされるアプリケーション |
|---|----------|----------|
| [&#x200B; 試験事業者 &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | インサイトの自動化、分析、統合を行い、影響の大きい実験や成長の機会を一元的なワークスペースからすばやく特定できます。しかも、手動プロセスを削減できます。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM 最適化エージェント &#x200B;](https://experienceleague.adobe.com/ja/docs/llm-optimizer/using/home) | AI 駆動型検索環境での可視性、精度、影響力を強化し、AI で生成された回答でブランドプレゼンスに関するインサイトを提供し、規範的なコンテンツのレコメンデーションを提供し、最適化の修正を自動化します。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/home) | Web サイトの機能強化を自動的に検出およびデプロイすることで、ビジネスへの影響を最大限に高めます。 生成 AI と複数の監視テクノロジーを使用すると、サイトトラフィックの獲得やエンゲージメントなどを増やすことができます | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/ja/docs/brand-concierge/content/documentation/overview) | 個々の好みや行動に合わせてカスタマイズされた、インテリジェントでコンテキストに対応した製品検出により、コンバージョンとエンゲージメントを強化します。 | <ul><li>AdobeBrand Concierge</li></ul> |

## このトピックに関するその他のヘルプ

* Experience Cloudでの [AI](https://experienceleague.adobe.com/ja/docs/ai) ドキュメントホーム
* [AEMにおけるエージェントの概要 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE &#x200B; 詳しくは、Adobe for Businessを参照してください &#x200B;]{type=Informative url="https://business.adobe.com/jp/products/experience-platform/agent-orchestrator.html" tooltip="Business.adobe.comに移動します"}
