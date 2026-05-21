---
title: Experience CloudアプリケーションのAgentic AI
description: Agentic AIをCX Enterprise アプリケーションで利用できる場所について説明します。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
feature_v2: id: f84b2906-3ce9-4ef0-86f6-cda249273937
source-git-commit: 5b2b81c029b81b9f0689a012cb2a9ca8714c0b40
workflow-type: tm+mt
source-wordcount: 1130
ht-degree: 8%

---

# Adobe CX EnterpriseのAgentic AI

Adobe Experience Platform Agentsは、[Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home)によって強化され、CX Enterprise アプリケーション内でエージェンティック AI機能を有効にします。

これらのエージェントは、タスクの自動化、インサイトの迅速な提供、ワークフローの合理化に役立ちます。 その結果、チームはより効率的に作業し、CX Enterpriseからより多くの価値を得ることができます。

CX EnterpriseのAI エージェントへのアクセスは、次のいずれかから利用できます。

* [既存の顧客体験エンタープライズアプリケーション](#existing-apps)
* [AI ファーストの顧客体験向けエンタープライズアプリケーション](#ai-first-apps)

次の節では、CX Enterpriseでエージェンティック AIを有効にするための2つの方法について説明します。

## 既存の顧客体験エンタープライズアプリケーション {#existing-apps}

既存のアプリケーションでは、自然言語を使用して、[AI アシスタント ](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home)の会話型インターフェイスを通じてAdobe Experience Platform Agentsに指示できます。 AI アシスタントは、フルスクリーン表示と右パネル表示の両方で利用できます。

エージェントは、次のいずれかのカテゴリの既存の顧客向けCX エンタープライズアプリで有効にできます。

* Adobe Experience Platform Agents AI クレジットライセンスを購入しました
* 使用制限のある体験版に含まれています（提供される限定AI クレジット）
* Agent Orchestrator プロモーション SKU （期限付き体験版ライセンス）を取引しました

AI エージェントを使用して&#x200B;_エージェントジョブ_&#x200B;を実行すると、AI クレジットが使用されます。 エージェントのジョブとAI クレジットについて詳しくは、_[エージェントのジョブとAI クレジットの使用](/help/interface/features/ai-credit-consumption.md)_&#x200B;を参照してください。

AI エージェントは&#x200B;_あなたの_&#x200B;の入力、監視に従い、製品レベルのアクセス制御を尊重します。 ジョブの実行またはデータへのアクセスは、基盤となるCX Enterprise アプリケーションで使用する権限を持つユーザーのみが実行できます。

### 既存のCX エンタープライズアプリのAI エージェント {#existing-apps-table}

次の表に、既存のCX Enterprise アプリケーションで使用可能なExperience Platform Agentsを示します。

| エージェント名 | 機能 | サポートされているアプリケーション | ヘルスデータ / HIPAA対応 |
|---|----------|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 自然言語のプロンプトを使用して、オーディエンスを管理、最適化することで、より使いやすさ、効率、市場投入までの時間を短縮できます。 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li></ul> | |
| [Content Advisor エージェント ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-advisor/overview) | <ul><li>自然言語を使用して、企業全体で最も関連性の高いコンテンツをすばやく見つけることができ、検索時間を短縮し、より迅速な意思決定と実行を可能にします。</li><li>自然言語プロンプトを使用して、ソースアセットからビジュアルコンテンツのバリエーションを容易に作成できます。</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul><ul><li>Dynamic Media （クラウドサービス）</li></ul> | |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | データに関する疑問にすばやく回答します。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。 | <ul><li>Customer Journey Analytics（B2BおよびB2C エディション）</li></ul> | ○ |
| [Brand Experience Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/overview) | <ul><li>既存のサイトを自動的に再構築、強化、検証することで、デジタルエクスペリエンスの移行と近代化を加速させ、リスクや手作業を削減しながら、AIを利用したモダンなエクスペリエンスにすばやく移行できます。</li><li>膨大なエクスペリエンスの構築と更新をおこない、手作業やサイクルタイムを大幅に削減することで、品質や一貫性を犠牲にすることなく迅速に作業を進めることができます。</li><li>フォーム体験を自動的に生成、構造化、検証することで、ブランドに即した最適化されたフォームの作成を高速化し、手作業を最小限に抑えながら迅速にローンチし、より高品質なデータを収集できるようにします。</li><li>AEM CSの開発者と技術管理者が、Cloud Manager パイプラインでビルドステップのエラーをトラブルシューティングするために、根本原因を分析し、修正を提案します。</li></ul> | <ul><li>Adobe Experience Manager Sites Cloud Services （エクスペリエンスの近代化）</li></ul><ul><li>Adobe Experience Manager Sites （Experience Production）</li></ul><ul><li>Adobe Experience Manager Forms（フォーム作成）</li></ul><ul><li>すべてのクラウドベースのAdobe Experience Manager アプリケーション（開発サポート）</li></ul> | |
| [ ブランドガバナンスエージェント ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview) | リアルタイムガバナンスでDRMをサポートする自動化されたブランドポリシーのチェック、権限、インテリジェンスにより、ブランドの整合性とコンプライアンスを保護します。 | <ul><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Sites（ブランドポリシー）</li></ul> | |
| [Journey Agent](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent) | マルチタッチのカスタマージャーニーを迅速に分析し、大規模に最適化できるようになります。 | <ul><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li></ul> | |
| [製品サポートエージェント ](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/product-support) | ワークフローを離れることなく、サポートの問題をトラブルシューティングし、カスタマーサポートチケットを作成し、AI アシスタントを使用してケースの進捗を追跡します。 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li><li>Customer Journey Analytics（B2BおよびB2C エディション）</li><li>Adobe Experience Manager</li></ul> | |
| [Adobe Marketing Agent for Microsoft 365 Copilot](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms) | Experience PlatformをMicrosoft 365 Copilotに直接接続します。 Teams、Word、Powerpoint、ExcelなどのMicrosoft 365 アプリケーション内で、自然言語による質問をすることで、ワークフローを中断することなく、Experience Platformからマーケティングインサイトをすばやく取得できます。 | <ul><li> Adobe Agent Orchestrator （Audience Agent、Journey Agent、Customer Journey Analytics Data Insights、Experience Platform Operational Insightsをサポート）</li></ul> | |

## AI ファーストの顧客体験向けエンタープライズアプリケーション {#ai-first-apps}

AI ファーストのアプリケーションは、生成AIまたはエージェンティック AIを中心に構築されています。 主要なタスクには生成AIまたはエージェント型AIを活用しており、エージェント型の機能は既にAl ファーストのアプリケーションライセンスに含まれています。 そのため、Experience Platform Agent Orchestrator ライセンスは必要ありません。

次の表に、Al ファースト アプリケーションとして使用可能なExperience Platform Agentsを示します。 これらは、次のAl-first アプリケーションのライセンスを取得することで有効になります。

| エージェント名 | 機能 | サポートされているアプリケーション |
|---|----------|----------|
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | インサイトを自動化、分析、合成することで、手作業のプロセスを削減しながら、一元化されたワークスペースから、インパクトの大きい実験や成長機会をすばやく特定することができます。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM最適化エージェント ](https://experienceleague.adobe.com/ja/docs/llm-optimizer/using/home) | AIを活用した検索環境における可視性、正確性、影響力を強化し、AIが生成した回答のブランドプレゼンスに関するインサイトを提供し、規範的なコンテンツレコメンデーションを提供し、最適化の修正を自動化します。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/home) | web サイトの機能強化を自動的に検出して展開し、ビジネス効果を最大化します。 生成AIと複数の監視テクノロジーを使用すれば、サイトトラフィックの獲得やエンゲージメントなどを向上できます | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | 個々の好みや行動に合わせた、コンテキストに即したインテリジェントな製品発見により、コンバージョンとエンゲージメントを促進します。 | <ul><li>Adobe Brand Concierge</li></ul> |

## このトピックの詳細ヘルプ

* [担当者の業務とAIのクレジット消費](/help/interface/features/ai-credit-consumption.md)
* CX Enterpriseの[AI](https://experienceleague.adobe.com/en/docs/ai) ドキュメント ホーム
* [AEMのAgentsの概要](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE Adobe for Businessについて詳しく見る]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="Business.adobe.comにアクセスします。"}
