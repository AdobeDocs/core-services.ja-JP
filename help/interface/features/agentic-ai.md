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
TQID: https://experienceleague.adobe.com/pjC1VIudoJcKjT26T9WpdWEGESQi-1QLc4KlyAqewq8
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: f84b2906-3ce9-4ef0-86f6-cda249273937id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: cda95149-19e1-4cfa-a57e-751283a32378id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 40fe0fa11458ed5da6182f0c0ca3f3d2c6ab796b
workflow-type: tm+mt
source-wordcount: 890
ht-degree: 4%

---

# Adobe Experience Cloudの Agentic AI

更新日：**2026 年 3 月 4 日**

Adobe Experience Platform Agents は、[Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home) を活用して、Experience Cloud アプリケーション内で Agentic AI 機能を有効にします。

これらのエージェントは、タスクの自動化、インサイトの迅速な提供、ワークフローの合理化に役立ちます。 その結果、チームはより効率的に作業し、Experience Cloudからより多くの価値を得ることができます。

Experience Cloudの AI エージェントには、次のいずれかでアクセスできます。

* [既存のExperience Cloud アプリケーション](#existing-apps)
* [AI ファーストのExperience Cloudアプリケーション](#ai-first-apps)

以下の節では、Experience Cloudで Agentic AI を有効にする 2 つの方法について説明します。

## 既存のExperience Cloud アプリケーション {#existing-apps}

既存のアプリケーションでは、自然言語を使用して、[AI アシスタント ](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home) の対話型インターフェイスを通じてAdobe Experience Platform Agents に指示できます。 AI アシスタントは、全画面表示と右パネル表示の両方で使用できます。

次のいずれかのカテゴリに属するお客様は、既存のExperience Cloud アプリでエージェントを有効にすることができます。

* Adobe Experience Platform Agents AI クレジットライセンスを購入した
* 使用量に制限された体験版に含まれています（AI クレジットは限定的です）
* Agent Orchestrator プロモ SKU （時間限定トライアルライセンス）をトランザクションしました

AI エージェントを使用して _エージェントジョブ_ を実行すると、AI クレジットが消費されます。 エージェントジョブと AI クレジットについて詳しくは、_[エージェントジョブと AI クレジットの消費](/help/interface/features/ai-credit-consumption.md)_ を参照してください。

AI エージェントは _あなたの_ 入力、監督に従い、製品レベルのアクセス制御を尊重します。 ジョブの実行や、基になるExperience Cloud アプリケーションで使用する権限のあるデータへのアクセスのみ可能です。

### 既存のExperience Cloud アプリ内の AI エージェント {#existing-apps-table}

次の表に、既存のExperience Platform アプリケーションで使用できるExperience Cloud エージェントを示します。

| エージェント名 | 機能 | サポートされるアプリケーション |
| --- | ---------- | ---------- |
| [Audience Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 自然言語プロンプトを使用してオーディエンスを作成、管理および最適化し、より簡単で効率の高い、市場投入までの時間を短縮する権限をチームに与えます。 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> |
| [ コンテンツ アドバイザーエージェント ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-advisor/overview) | <ul><li>は、チームが自然言語を使用して企業全体で最も関連性の高いコンテンツをすばやく見つけるのに役立ち、検索に費やす時間を短縮し、迅速な決定と実行を可能にします。</li><li>自然言語プロンプトを使用して、ソースアセットから視覚的なコンテンツのバリアントを簡単に作成できます。</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul><ul><li>Dynamic Media （クラウドサービス）</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | データに関する質問にすばやく回答します。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。 | <ul><li>Customer Journey Analytics（B2B と B2C のエディション）</li></ul> |
| [Brand Experience Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/overview) | <ul><li>既存のサイトを自動的に再構築、強化、検証することで、デジタルエクスペリエンスの移行と最新化を促進し、チームがリスクと手動の労力を軽減しながら、最新の AI 対応エクスペリエンスにすばやく移行できるようにします。</li><li>大量のエクスペリエンスの作成と更新を実行し、手作業とサイクル時間を大幅に削減することで、チームは品質と一貫性を犠牲にすることなく迅速に作業を進めることができます。</li><li>フォームエクスペリエンスを自動的に生成、構造化、検証することで、最適化されたオンブランドのフォームをすばやく作成できます。これにより、チームは最小限の手動の労力で、より迅速に開始し、より高品質なデータを取得できます。</li><li>は、AEM CS 開発者と技術管理者が、根本原因を分析して修正を提案することで、Cloud Manager パイプラインのビルドステップエラーをトラブルシューティングするのに役立ちます。</li></ul> | <ul><li>Adobe Experience Manager Sites Cloud Services （Experience Modernization）</li></ul><ul><li>Adobe Experience Manager Sites（Experience Production）</li></ul><ul><li>Adobe Experience Manager Forms（フォームの作成）</li></ul><ul><li>すべてのクラウドベースのAdobe Experience Manager アプリケーション（開発サポート）</li></ul> |
| [ ガバナンス機関 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview)* | <ul><li>ブランドの整合性と自動ブランドポリシーのチェック、権限、インテリジェンスへのコンプライアンスを保護し、リアルタイムガバナンスを備えた DRM をサポートします。</li> | <ul><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Sites（ブランドポリシー）</li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | チームがマルチタッチのカスタマージャーニーを大規模にすばやく作成、分析、最適化できるようにします。 | <ul><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li></ul> |
| [ 製品サポート担当者 ](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support) | ワークフローを離れることなくサポートの問題をトラブルシューティングしたり、カスタマーサポートチケットを作成したり、AI アシスタントを使用してケースの進行状況を追跡したりできます。 | <ul><li>Real-Time CDP（B2B、B2C、B2P の各エディション）</li><li>Adobe Journey Optimizer（B2B と B2C のエディション）</li><li>Customer Journey Analytics（B2B と B2C のエディション）</li><li>Adobe Experience Manager</li></ul> |

アスタリスク （*）：このエージェントは、エクスプローラープログラムを使用しているお客様がアクセスできます。 エクスプローラープログラムは、Adobeの最新の高度な機能に早期にアクセスできるようにする招待専用プログラムです。 詳しくは、アカウント担当者にお問い合わせください。

## AI ファーストのExperience Cloudアプリケーション {#ai-first-apps}

AI ファーストのアプリケーションは、ジェネレーティブまたはアジェンティック Al をコアとして構築されています。 彼らは主要なタスクにジェネレーティブまたは Agentic Al を使用し、Agentic 機能はすでに Al-first アプリケーションライセンスに含まれています。 そのため、Experience Platform Agent Orchestrator ライセンスは必要ありません。

次の表に、Al-first アプリケーションとして使用できるExperience Platform エージェントを示します。 これらは、次の Al-first アプリケーションのライセンスを取得することで有効になります。

| エージェント名 | 機能 | サポートされるアプリケーション |
| --- | ---------- | ---------- |
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | インサイトの自動化、分析、統合を行い、影響の大きい実験や成長の機会を一元的なワークスペースからすばやく特定できます。しかも、手動プロセスを削減できます。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM 最適化エージェント ](https://experienceleague.adobe.com/ja/docs/llm-optimizer/using/home) | AI 駆動型検索環境での可視性、正確性、影響力を強化し、AI で生成された回答のブランドプレゼンスに対するインサイトを提供し、規範的なコンテンツのレコメンデーションを提供し、最適化の修正を自動化します。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/home) | Web サイトの機能強化を自動的に検出およびデプロイすることで、ビジネスへの影響を最大限に高めます。 生成 AI と複数の監視テクノロジーを使用すると、サイトトラフィックの獲得やエンゲージメントなどを増やすことができます | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | 個々の好みや行動に合わせてカスタマイズされた、インテリジェントでコンテキストに対応した製品検出により、コンバージョンとエンゲージメントを強化します。 | <ul><li>AdobeBrand Concierge</li></ul> |

## このトピックに関するその他のヘルプ

* [エージェントジョブと AI クレジット消費](/help/interface/features/ai-credit-consumption.md)
* Experience Cloudでの [AI](https://experienceleague.adobe.com/en/docs/ai) ドキュメントホーム
* [AEMにおけるエージェントの概要 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE  詳しくは、Adobe for Businessを参照してください ]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="Business.adobe.comに移動します"}

