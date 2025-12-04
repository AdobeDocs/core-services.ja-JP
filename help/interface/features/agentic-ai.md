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
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: e63dd988abba199049da2b3620eed9ebf51043d1
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 6%

---

# Experience CloudのExperience Platform エージェント

更新日：**2025年12月2日（PT）**

Adobe [!DNL Experience Platform] [Agent Orchestrator](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/home) およびAdobe Experience Platform エージェントは、Experience Cloud アプリケーション内で高度な機能を有効にします。

これらの高度な機能には、次のいずれかの方法でアクセスできます。

* [&#x200B; 既存  [!DNL Experience Cloud]  アプリ &#x200B;](#existing-apps)：これらのアプリケーションは単独で動作しますが、Experience Platform Agent Orchestratorとエージェントを有効にすると、これらのアプリケーションで実行される既存のジョブとワークフローの効率が向上し、それらを使用するチームの生産性が向上します。 現在ライセンスを取得しているExperience Cloud アプリケーションでこれらの高度な機能を有効にするには、Agent Orchestrator ライセンスも購入する必要があります。

* [AI-first [!DNL Experience Cloud] apps](#ai-first-apps)：これらのアプリケーションは、ジェネレーティブまたはアジェンティック AI をコアとして構築されています。 これらのユーザーは、主要なタスクにジェネレーティブ AI またはエージェンティック AI を使用します。エージェンティック機能は、既に AI ファースト アプリケーション ライセンスに含まれており、Agent Orchestrator ライセンスは必要ありません。

## 既存の [!DNL Experience Cloud] アプリケーション

以下は、既存の experience cloud アプリケーションで使用でき、Agent Orchestratorのライセンスで有効になるExperience Platform エージェントのリストです。

| エージェント名 | 対象 | 機能 | サポートされるアプリケーション |
|---|----------|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 利用可能 | 自然言語プロンプトを使用してオーディエンスを作成、管理および最適化し、より簡単で効率の高い、市場投入までの時間を短縮する権限をチームに与えます。 | <ul><li>Real-Time CDP（B2B と B2C のエディション）</li><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> |
| [&#x200B; コンテンツ最適化エージェント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/content-optimization/using) | 利用可能 | 自然言語プロンプトを使用して、ソースアセットから視覚的なコンテンツのバリアントを簡単に作成できます。 | <ul><li>Adobe Experience Manager（[Dynamic Media with OpenAPI](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview) を使用）</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | 利用可能 | データに関するデータの質問にすばやく回答します。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。 | <ul><li>Customer Journey Analytics</li></ul> |
| [&#x200B; 開発援助機関 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/development/overview) | 利用可能 | は、AEM CS 開発者と技術管理者が、根本原因を分析して修正を提案することで、Cloud Manager パイプラインのビルドステップエラーをトラブルシューティングするのに役立ちます。 | <ul><li>AEM Cloud Service およびAdobe Managed Servicesの AI アシスタント</li></ul> |
| [&#x200B; 探索エージェント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/discovery/using) | 利用可能 | シンプルな自然言語プロンプトにより、画像、ビデオ、テキストベースのドキュメント、コンテンツフラグメント、フォーム全体でExperience Manager コンテンツを即座に見つけて表示し、オーサリングを迅速化して検出を強化します。 | <ul><li>Adobe Experience Manager Cloud Services</li></ul> |
| [Experience Production エージェント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/production/overview) | 利用可能 | CMSで手間のかかる大量タスクを自動化します。 このエージェントは、手動の長いプロセスを、すべてのエクスペリエンスを最新かつ一貫性のある状態に保つ、AI を利用した高速ワークフローに変え、ビジネスの目標達成を支援します。 | <ul><li>Adobe Experience Manager Cloud Services とEdge Delivery Services</li></ul> |
| [&#x200B; ガバナンス機関 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/governance/overview) | 利用可能 | Experience Manager全体でセキュリティ、規制、ブランドポリシーを適用することで、ブランドの整合性とコンプライアンスを保護します。 このエージェントは、視覚的およびメッセージング標準を維持するためにブランドガバナンスを適用します。 アクセスとコンテンツの変更を管理するために詳細な権限を使用し、ライセンスと使用の制約を維持するために DRM を組み込みます。 | <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms </li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | 利用可能 | チームがマルチタッチのカスタマージャーニーを大規模にすばやく作成、分析、最適化できるようにします。 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> |
| [&#x200B; 製品サポート担当者 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/new-features/customer-support) | 利用可能 | ワークフローを離れることなくサポートの問題をトラブルシューティングしたり、カスタマーサポートチケットを作成したり、AI アシスタントを使用してケースの進行状況を追跡したりできます。 | <ul><li>Real-Time CDP（B2B と B2C のエディション）</li><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li><li>Adobe Journey OptimizerB2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

<!-- | Agent name  | Availability | Capabilities | Supported applications   |
|---|----------|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/audience)  | Available | Empower your teams to create, manage, and optimize audiences using natural language prompts for greater ease, efficiency, and speed to market. | <ul><li>Real-Time CDP (B2B and B2C editions)</li><li>Adobe Journey Optimizer (B2B and B2C editions)</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai)  | Available | Quickly answers data questions about your data. It builds relevant visualizations in Analysis Workspace using components from your data view and using your actual data. | <ul><li>Customer Journey Analytics</li></ul>  |
| [Journey Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | Available | Enable your teams to quickly create, analyze, and optimize multi-touch customer journeys at scale. | <ul><li>Adobe Journey Optimizer (B2B and B2C editions)</li></ul>    |
| [Product Support Agent](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/new-features/customer-support) | Available | Troubleshoot support issues without leaving your workflows, create customer support tickets, and track case progress using AI Assistant. | <ul><li>Real-Time CDP (B2B and B2C editions)</li><li>Adobe Journey Optimizer (B2B and B2C editions)</li><li>Adobe Journey Optimizer B2B Edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul>  | -->


## AI ファーストのExperience Cloudアプリケーション

以下は、AI ファーストのアプリケーションで使用でき、これらの AI ファーストのアプリケーションのライセンスを取得することで有効になるExperience Platform エージェントのリストです。

| エージェント名 | 対象 | 機能 | サポートされるアプリケーション |
|---|----------|----------|----------|
| [&#x200B; 試験事業者 &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | 利用可能 | インサイトの自動化、分析、統合を行い、影響の大きい実験や成長の機会を一元的なワークスペースからすばやく特定できます。しかも、手動プロセスを削減できます。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM 最適化エージェント &#x200B;](https://experienceleague.adobe.com/ja/docs/llm-optimizer/using/home) | 利用可能 | AI 駆動型検索環境での可視性、精度、影響力を強化し、AI で生成された回答でブランドプレゼンスに関するインサイトを提供し、規範的なコンテンツのレコメンデーションを提供し、最適化の修正を自動化します。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/home) | 利用可能 | Web サイトの機能強化を自動的に検出およびデプロイすることで、ビジネスへの影響を最大限に高めます。 生成 AI と複数の監視テクノロジーを使用すると、サイトトラフィックの獲得やエンゲージメントなどを増やすことができます | <ul><li>AEM Sites Optimizer</li></ul> |

<!-- | Agent name  | Availability | Capabilities | Supported applications   |
|---|----------|----------|----------|
| [Content Optimization Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/content-optimization/using) | Available | Simplify creating visual content variants from source assets using natural language prompts.|  <ul><li>Adobe Experience Manager (with [Dynamic Media with OpenAPI](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview))</li></ul>  |
| [Development Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/development/overview) | Available | Helps AEM CS developers and technical administrators troubleshoot build-step failures in the Cloud Manager pipeline by analyzing the root cause and suggesting fixes.|  <ul><li>AI Assistant in AEM Cloud Service and Adobe Managed Services</li></ul>  |
| [Discovery Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/discovery/using) | Available | Speed authoring and boost discovery with simplified natural-language prompts to instantly find and surface Experience Manager content across images, videos, text-based documents, content fragments, and forms.|  <ul><li>Adobe Experience Manager Cloud Services</li></ul>  |
| [Experience Production Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/production/overview) | Available | Automates high-effort and high-volume tasks in the CMS. This agent turns manual, lengthy processes into fast, AI-assisted workflows that keep every experience current and consistent, helping your business achieve your goals.|  <ul><li>Adobe Experience Manager Cloud Services and Edge Delivery Services</li></ul>  |
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | Available | Automate, analyze, and synthesize insights, so you can quickly identify high-impact experiments and growth opportunities from a centralized workspace — all while reducing manual processes.  | <ul><li>AJO Experimentation Accelerator</li></ul>   |
| [Governance Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/business-agents/governance/overview) | Available | Safeguard brand integrity and compliance by enforcing security, regulatory, and brand policies across Experience Manager. This agent applies brand governance to maintain visual and messaging standards. It uses granular permissions to manage access and content changes, and incorporates DRM to uphold licensing and usage constraints. |  <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms </li></ul>  |
| [LLM Optimization Agent](https://experienceleague.adobe.com/ja/docs/llm-optimizer/using/home) | Available | Enhance visibility, accuracy, and influence in AI-driven search environments, provide insights into brand presence in AI-generated answers, offer prescriptive content recommendations, and automate optimization fixes. | <ul><li>Adobe LLM Optimizer</li></ul>   |
| [Site Optimization Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/home) | Available | Maximize business impact by automatically detecting and deploying website enhancements. Using generative AI and multiple monitoring technologies, you can increase site traffic acquisition, engagement, and more | <ul><li>AEM Sites Optimizer</li></ul> | -->

## このトピックに関するその他のヘルプ

* Experience Cloudでの [AI](https://experienceleague.adobe.com/ja/docs/ai) ドキュメントホーム

[!BADGE &#x200B; 詳しくは、Adobe for Businessを参照してください &#x200B;]{type=Informative url="https://business.adobe.com/jp/products/experience-platform/agent-orchestrator.html" tooltip="Business.adobe.comに移動します"}
