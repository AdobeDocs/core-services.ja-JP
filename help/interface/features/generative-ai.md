---
title: Experience Cloud アプリケーションの AI
description: ジェネレーティブ AI と、Experience Cloud アプリケーションで genAI および  [!DNL AI Assistant] がどのように使用されるかについて説明します。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 4676c606f132ab835e0d1f8cdbc81d932e358028
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 3%

---

# Experience Cloud製品における AI

このページでは、生成 AI や [!DNL AI Assistant] をサポートする製品と、Adobe Fireflyに互換性があるかどうかを確認します。 また、Experience Cloudでの AI の使用方法に関する製品固有のヘルプリソースへのリンクもあります。

**生成 AI について**

ジェネレーティブ AI は、単に質問に答えるだけでなく、それを実現する人工知能の一種です。 _作成_ コンテンツおよび _応答_ を、質問やステートメント（「_プロンプト_」と呼ばれます）に対して実行できます。

* **作成：** トレーニングと入力プロンプトに基づいて、新しいコンテンツ（テキスト、画像、音楽、ビデオ）をゼロから生成する AI 機能。 この機能は、生成 AI の _生成_ 側面です。

* **回答：** AI は、通常、知識や推論能力を活用して、プロンプトに対する回答や反応を提供します。

ジェネレーティブ AI を使用すると、Experience Cloudを初めて使用する場合でも、製品に関する知識をすばやく得ることができます。 熟練したユーザーが、数時間ではなく数秒でオペレーショナルインサイトを見つけることができます。

**[!DNL AI Assistant] とは？**

[!DNL AI Assistant] は、Experience Platformおよび関連アプリケーションでサポートされる対話型ツールです。 これらのアプリケーションは同様に使用しますが、製品固有の利点があります。 ワークフローの迅速化、製品知識の向上、問題のトラブルシューティング、情報検索に使用できます。 特定のアプリケーションでは、[!DNL AI Assistant] を使用すると、運用に関するインサイトを即座に見つけることができます。

Experience Leagueからの商品のナレッジレスポンスは、検証可能であり、リンクで引用されています。 [!DNL AI Assistant] を最大限に活用するための [ 目標ベースのプロンプト ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) のタイプについて説明します。

[詳細情報](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## Experience Cloud製品での AI の可用性

Experience Cloud製品でのジェネレーティブ AI または [!DNL AI Assistant] のサポートと、Adobe Fireflyがサポートされているかどうかを説明します。

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [バリエーションを生成  [!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL AI Assistant] in [!DNL Journey Optimizer]](#journey-optimizer)
* [ [!DNL Journey Optimizer] PrimeおよびUltimateの [!DNL AI Assistant]](#ajo-prime-ultimate)
* [ [!DNL Journey Optimizer] B2B editionの [!DNL AI Assistant]](#ajo-b2b)
* [[!DNL AI Assistant] in [!DNL Campaign] v8 Web ユーザーインターフェイス](#campaign-cs)
* [[!DNL AI Assistant] in [!DNL Customer Journey Analytics]](#cja)
* [ [!DNL Customer Journey Analytics] のインテリジェントキャプション](#cja-captions)
* [[!DNL AI Assistant] in [!DNL Real-Time CDP]](#rtcdp)
* [Dynamic Chat [!DNL Marketo]](#marketo)
* [[!DNL AI Assistant] in [!DNL Workfront]](#workfront)

## パフォーマンスマーケティング用の GenStudio {#gspm}

[!DNL GenStudio for Performance Marketing] は、ブランド標準に準拠し、企業ポリシーに準拠したマーケティングコンテンツを生成および管理できるようにする AI 駆動型プラットフォームです。 メール、メタ広告、LinkedIn 広告、ディスプレイ広告およびバナーのコンテンツを生成します。

また、例、お客様のペルソナや商品の説明、ブランドガイドラインを使用して、ブランドに関するGenStudio for Performance Marketingのトレーニングを行うこともできます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home)

Adobe Fireflyとの互換性：**予定**

## [!DNL Experience Manager Sites] でのバリエーションの生成 {#aem-sites}

AEM Sitesの [!UICONTROL  バリエーションを生成 ] では、生成 AI を使用して、プロンプトに基づくコンテンツのバリエーションを作成します。 これらのプロンプトは、Adobeから提供されるか、ユーザーが作成および管理します。

バリエーションを作成した後、Web サイトでコンテンツを使用し、Edge Delivery Servicesの実験機能を使用して、その成功を測定できます。 また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。

[詳細情報](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)

Adobe Fireflyとの互換性：**はい**

## [!DNL Journey Optimizer] の AI アシスタント {#journey-optimizer}

[!DNL Journey Optimizer] では、[!DNL AI Assistant] を使用して、製品に関する知識や運用に関するインサイトを得ます。 例えば、_1 つのJourney Optimizer サンドボックスにいくつのライブアクティビティを持つことができますか？_ Experience Leagueや他のAdobe データストアからすぐに回答が得られます。

また、[!DNL AI Assistant] はオペレーショナルインサイト（ベータ版）にも役立ちます。 例えば、過去 7 日間に作成されたジャーニーの数をすばやく把握できます。

運用インサイトの場合、[!DNL AI Assistant] は顧客固有のデータストアをクエリします。 データストアには、[!UICONTROL ジャーニー] に関する一元化された運用データが含まれています。 この機能は顧客に依存せず、ビジネスオブジェクトからのみメタデータを取り込みます。 サンドボックス内のデータにはアクセスしません。

[詳細情報](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)

Adobe Fireflyとの互換性：**いいえ**

## PrimeおよびUltimate[!DNL Journey Optimizer]AI アシスタント {#ajo-prime-ultimate}

PrimeとUltimateで [!DNL Journey Optimizer]、[!DNL AI Assistant] for Content Accelerator を使用して、テキストや画像に対するプロアクティブなコンテンツバリエーションの提案を提供します。

この機能は、メール、プッシュ通知、web ページ、コンテンツおよび SMS チャネルで使用できます。 プロンプトベースのテキストと画像を生成できます。 AJO PrimeおよびUltimateのコンテンツアクセラレーターの出力は保証されません

[詳細情報](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Adobe Fireflyとの互換性：**はい**

## [!DNL Journey Optimizer B2B Edition] の AI アシスタント {#ajo-b2b}

Journey Optimizer B2B editionでは、[!DNL AI Assistant] を使用して商品の知識を支援します。

[詳細情報](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Campaign] v8 Web UI の AI アシスタント {#campaign-cs}

Campaign Managed Cloud Services は、コンテンツアクセラレーターに [!DNL AI Assistant] を使用します。 この機能を使用すると、ブランドの概要を示すスタイル、レイアウト、トーンなどに最適化されたコンテンツを使用して、マーケティング目標に基づいてパーソナライズされた魅力的で効果的なコンテンツを自動生成できます。 メール、SMS、プッシュなど、様々なチャネルで使用できます。

**メモ：** Campaign Managed Cloud Services のコンテンツアクセラレーターからの出力は除外されます。

[詳細情報](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Adobe Fireflyとの互換性：**はい**

## [!DNL Customer Journey Analytics] の AI アシスタント {#cja}

Customer Journey Analyticsでは、[!DNL AI Assistant] を使用して、Experience Leagueから商品に関する知識やインサイトを得ることができます。 初めて使用する場合は、Customer Journey Analyticsの概念を素早く理解し、製品や機能のオンボーディングをおこないます。

経験豊富なユーザーが高度なユースケースを取得したり、タスクを迅速に実行するための戦略を学んだりします。 概念の理解、問題のトラブルシューティング、情報の検索。

[詳細情報](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Customer Journey Analytics] のインテリジェントキャプション {#cja-captions}

[!DNL Customer Journey Analytics] のインテリジェントキャプションは、最も頻繁に使用されるWorkspaceのビジュアライゼーションに対して自然言語のインサイトを提供します。 インテリジェントキャプションは、他のユーザーと共有するためにストーリーとコンテキストを必要とするアナリストに最適です。 ビジネスユーザーは、これを使用して、大まかな留意点をすばやく見つけることができます。

[詳細情報](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Real-Time CDP] の AI アシスタント {#rtcdp}

Real-Time CDPでは、Experience Leagueの製品知識の取得を支援するために [!DNL AI Assistant] を使用しています。 また、運用に関するインサイト（ベータ版）も提供します。 [!DNL AI Assistant] は、AEP サンドボックス内にパーティション化された、一元化された運用データを含む、顧客固有の運用インサイトデータストアをクエリします。 システムは、属性、オーディエンス、データフロー、データセット、宛先、スキーマおよびソースからのみメタデータを取り込み、サンドボックス内のデータにはアクセスしません。

例えば、オーディエンスに関するクエリを実行する場 [!DNL AI Assistant]、オーディエンスの名前および他の関連メタデータにアクセスできますが、そのオーディエンス内のプロファイルにはアクセスできません。

[詳細情報](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Marketo] のDynamic Chat {#marketo}

Adobe Dynamic Chatのジェネレーティブ AI を活用した機能により、営業担当者の生産性を最適化し、Web サイトの訪問者の意図に関するインサイトを得て、訪問者の質問に安全な方法で対応できます。 質問、回答および会話の概要を事前承認できます。

[詳細情報](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Workfront] における [!DNL AI Assistant] {#workfront}

[!DNL Workfront] の [!DNL AI Assistant] は、アプリ内情報や提案を提供することで、作業を完了するのに役立ちます。 実行できる操作は、次のとおりです。

* 一部のオブジェクトの概要を取得して、オブジェクトの意図や詳細の概要を表示します。
* Experience Leagueに関する質問や回答の検索 [!DNL AI Assistant] 行います。
* プロンプトに基づいて生成された式を取得します。 また、計算フィールドでの無効なカスタム式のエラーを解決することもできます。
* プロジェクト、タスクおよび問題を見つけます。

[詳細情報](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Adobe Fireflyとの互換性：**いいえ**
