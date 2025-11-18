---
title: Experience CloudアプリケーションにおけるエージェントAI
description: Experience CloudアプリケーションでエージェントAIが利用できる場所について説明します。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: 7f0563f5b44d4abb06bc042553d624ec16fbcdc4
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 7%

---

# Experience CloudでのエージェントExperience Platform

更新日: **2025年11月17日**

Adobe Systems [!DNL Experience Platform] [エージェント オーケストレータ](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home) および Adobe Experience Platform エージェントは、Experience Cloud アプリケーション内でエージェント機能を有効にします。

これらのエージェント機能にアクセスするには、次のいずれかを使用します。

* [既存アプリ [!DNL Experience Cloud] &#x200B;](#existing-apps): これらのアプリケーションは単独で機能しますが、エージェント オーケストレーターとエージェントを有効にするとExperience Platformこれらのアプリケーションで実行される既存のジョブとワークフローの効率が向上し、それらを活用するチームの生産性が向上します。現在ライセンスを取得しているExperience Cloudアプリケーションでこれらのエージェント機能を有効にするには、エージェントオーケストレーターライセンス版も購入する必要があります。

* [AI ファースト [!DNL Experience Cloud] アプリ](#ai-first-apps): これらのアプリケーションは、生成型またはエージェント型の AI をコアとして構築されています。 主要なタスクには生成型またはエージェント型 AI を使用し、エージェント機能は AI ファースト アプリケーション ライセンス版に既に含まれており、エージェント オーケストレーターライセンス版は必要ありません。

## 既存の [!DNL Experience Cloud] アプリケーション

既存の エクスペリエンス クラウド アプリケーションで使用でき、ライセンス エージェント オーケストレーターによって有効になる Experience Platform エージェントのリストを次に示します。

| エージェント名 | 対象 | 機能 | サポートされているアプリケーション |
|---|----------|----------|----------|
| [オーディエンスエージェント](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 利用できる | チームが自然言語プロンプトを使用してオーディエンスを作成、管理、最適化し、より簡単、効率的、迅速にマーケットできるようにします。 | <ul><li>Real-時間 CDP(B2B および B2C の追加)</li><li>Adobe Systemsジャーニーオプティマイザー(B2BおよびB2Cの追加)</li></ul> |
| [データInsightsエージェント](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | 利用できる | データに関するデータの質問にすばやく回答します。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。 | <ul><li>Customer Journey Analytics</li></ul> |
| [ジャーニーエージェント](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | 利用できる | チームがマルチタッチ顧客ジャーニーを大規模にすばやく作成、分析、最適化できるようにします。 | <ul><li>Adobe Systemsジャーニーオプティマイザー(B2BおよびB2Cの追加)</li></ul> |
| [製品サポートエージェント](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support) | 利用できる | ワークフローを離れることなくサポートの問題トラブルシューティング、顧客サポートチケットを作成し、AI Assistantを使用してケースの進捗状況を追跡します。 | <ul><li>Real-時間 CDP(B2B および B2C の追加)</li><li>Adobe Systemsジャーニーオプティマイザー(B2BおよびB2Cの追加)</li><li>Adobe Journey Optimizer B2B Edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

<!-- Product Advisor Agent: Troubleshoot issues, create support tickets, and track progress with AI Assistant. 

<ul><li>Adobe Experience Platform</li><li>Real-Time CDP (B2B and B2C additions)</li><li>Adobe Journey Optimizer (B2B and B2C additions)</li><li>Adobe Journey Optimizer B2B Edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> 

Site Advisory Agent: Troubleshoot issues, create support tickets, and track progress with AI Assistant. 

<ul><li>Adobe Experience Platform</li><li>Real-Time CDP (B2B and B2C additions)</li><li>Adobe Journey Optimizer (B2B and B2C additions)</li><li>Adobe Journey Optimizer B2B Edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul>  -->

<!-- Draft AEM or upcoming agents: release 11/20

Production Agent
Discovery Agent
Development Agent
-->

## AIファーストExperience Cloudアプリケーション

以下は、AI-Firstアプリケーションで利用でき、これらのAI-fFirstアプリケーションのライセンスによって有効になるExperience Platformエージェントのリストです。

| エージェント名 | 対象 | 機能 | サポートされているアプリケーション |
|---|----------|----------|----------|
| [実験エージェント](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | 利用できる | インサイトを自動化、分析、統合することで、手作業によるプロセスを削減しながら、一元化されたワークスペースから影響の大きい実験や成長機会をすばやく特定できます。 | <ul><li>AJO 実験アクセラレータ</li></ul> |
| [LLM 最適化エージェント](https://experienceleague.adobe.com/ja/docs/llm-optimizer/using/home) | 利用できる | AI主導の検索環境での可視性、精度、影響力を強化し、AIが生成した回答におけるブランドの存在に関する洞察を提供し、規範的な内容の推奨事項オファー、最適化の修正を自動化します。 | <ul><li>Adobe Systems LLMオプティマイザー</li></ul> |
| [サイト最適化エージェント](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/home) | 利用できる | ウェブサイトの機能強化を自動的に検出して展開することで、ビジネスへの影響を最大化します。 ジェネレーティブAIと複数の監視テクノロジーを使用して、サイトトラフィック獲得、エンゲージメントなどを増やすことができます | <ul><li>AEM Sitesオプティマイザー</li></ul> |

<!-- | Agent name  | Availability | Capabilities | Supported applications   |
|---|----------|----------|----------|
| **Content Optimization Agent** | November 21, 2025 | Simplify creating visual content variants from source assets using natural language prompts.|  <ul><li>Adobe Experience Manager (with [Dynamic Media with OpenAPI](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview))</li></ul>  |
| **Development Agent** | November 21, 2025 | Helps AEM CS developers and technical administrators troubleshoot build-step failures in the Cloud Manager pipeline by analyzing the root cause and suggesting fixes.|  <ul><li>AI Assistant in AEM Cloud Service and Adobe Managed Services</li></ul>  |
| **Discovery Agent** | November 21, 2025 | Speed authoring and boost discovery with simplified natural-language prompts to instantly find and surface Experience Manager content across images, videos, text-based documents, content fragments, and forms.|  <ul><li>Adobe Experience Manager Cloud Services</li></ul>  |
| **Experience Production Agent** | November 21, 2025 | Automates high-effort and high-volume tasks in the CMS. This agent turns manual, lengthy processes into fast, AI-assisted workflows that keep every experience current and consistent, helping your business achieve your goals.|  <ul><li>Adobe Experience Manager Cloud Services and Edge Delivery Services</li></ul>  |
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | Available | Automate, analyze, and synthesize insights, so you can quickly identify high-impact experiments and growth opportunities from a centralized workspace — all while reducing manual processes.  | <ul><li>AJO Experimentation Accelerator</li></ul>   |
| **Governance Agent** | November 21, 2025 | Safeguard brand integrity and compliance by enforcing security, regulatory, and brand policies across Experience Manager. This agent applies brand governance to maintain visual and messaging standards. It uses granular permissions to manage access and content changes, and incorporates DRM to uphold licensing and usage constraints. |  <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms </li></ul>  |
| [LLM Optimization Agent](https://experienceleague.adobe.com/en/docs/llm-optimizer/using/home) | Available | Enhance visibility, accuracy, and influence in AI-driven search environments, provide insights into brand presence in AI-generated answers, offer prescriptive content recommendations, and automate optimization fixes. | <ul><li>Adobe LLM Optimizer</li></ul>   |
| [Site Optimization Agent](https://experienceleague.adobe.com/en/docs/experience-manager-sites-optimizer/content/home) | Available | Maximize business impact by automatically detecting and deploying website enhancements. Using generative AI and multiple monitoring technologies, you can increase site traffic acquisition, engagement, and more | <ul><li>AEM Sites Optimizer</li></ul> | -->

## このトピックに関するヘルプ詳細

* [AI in Experience Cloud](https://experienceleague.adobe.com/ja/docs/ai) ドキュメンテーションのホーム

[!BADGE 法人向けAdobe Systemsについて詳しくは、こちらをご覧ください。]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="Business.adobe.com に移動"}








