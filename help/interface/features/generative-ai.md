---
title: Experience Cloud アプリケーションの AI
description: ジェネレーティブ AI と、Experience Cloud アプリケーションで genAI および AI アシスタントがどのように使用されるかについて説明します。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: b94bf94368312b3ed64a559da946a1be8ccb3c18
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 5%

---

# Experience Cloud製品における AI

ジェネレーティブ AI は、単に質問に答えるだけでなく、それを実現する人工知能の一種です。 コンテンツを _作成_ し、_プロンプト_ （質問とステートメント _に対して_ 応答」します。

* **作成：** トレーニングと入力プロンプトに基づいて、新しいコンテンツ（テキスト、画像、音楽、ビデオ）をゼロから生成する AI 機能を指します。 この機能は、生成 AI の _生成_ 側面です。

* **回答：** 特定のプロンプトに対して回答や反応を提供する AI を指し、通常は知識や推論機能を利用します。

Experience Cloudを初めて使用する場合は、ジェネレーティブ AI を使用して、商品に関する知識をすばやく得ることができます。 経験豊富なユーザーであれば、数時間ではなく数秒で運用インサイトを見つけることができます。

**AI アシスタントについて**

AI アシスタントは、Experience Platformおよび関連するアプリケーションでサポートされる対話型ツールです。 ワークフローの迅速化、製品知識の向上、問題のトラブルシューティング、情報検索に使用できます。 特定のアプリケーションでは、AI アシスタントを使用すると、運用上のインサイトをすぐに見つけることができます。

Experience Leagueからの商品のナレッジレスポンスは、検証可能であり、リンクで引用されています。 AI アシスタントを最大限に活用するための [ 目標ベースのプロンプト ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) のタイプについて説明します。

[詳細情報](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## Experience Cloud製品での AI の可用性

Experience Cloud製品でのジェネレーティブ AI または AI アシスタントのサポートと、Adobe Fireflyがサポートされているかどうかを説明します。

* [パフォーマンスマーケティング用の GenStudio](#gspm)
* [AEM Sites（Cloud Service）でのバリエーションの生成](#aem-sites)
* [Journey Optimizer の AI アシスタント](#journey-optimizer)
* [Adobe Journey Optimizer PrimeとUltimate](#ajo-prime-ultimate)
* [Journey Optimizer B2B エディション](#ajo-b2b)
* [Journey Optimizer PrimeおよびUltimateの AI アシスタント](#ajo-prime-ultimate)
* [Journey Optimizer B2B editionの AI アシスタント](#ajo-b2b)
* [Campaign Managed Cloud Services の AI アシスタント](#campaign-cs)
* [Customer Journey Analyticsの AI アシスタント](#cja)
* [Customer Journey Analyticsのインテリジェントキャプション](#cja-captions)
* [Real-Time CDPの AI アシスタント](#rtcdp)
* [MarketoのDynamic Chat](#marketo)
* [Workfrontの AI アシスタント](#workfront)

### パフォーマンスマーケティング用の GenStudio {#gspm}

GenStudio for Performance Marketingは、ブランド標準に準拠し、エンタープライズポリシーに準拠したマーケティングコンテンツを生成および管理できるようにする AI 駆動型プラットフォームです。 メール、メタ広告、LinkedIn 広告、ディスプレイ広告およびバナーのコンテンツを生成します。

また、例、お客様のペルソナや商品の説明、ブランドガイドラインを使用して、ブランドに関するGenStudio for Performance Marketingのトレーニングを行うこともできます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home)

Adobe Fireflyとの互換性：**予定**

### Experience Manager Sitesでのバリエーションの生成 {#aem-sites}

AEM Sitesのバリエーションを生成では、生成 AI を使用して、プロンプトに基づくコンテンツのバリエーションを作成します。 これらのプロンプトは、Adobeから提供されるか、ユーザーが作成および管理します。

バリエーションを作成した後、Web サイトでコンテンツを使用し、Edge Delivery Servicesの実験機能を使用して、その成功を測定できます。 また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。

[詳細情報](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)

Adobe Fireflyとの互換性：**はい**

## Journey Optimizer の AI アシスタント {#journey-optimizer}

Journey Optimizerでは、AI アシスタントを使用して、製品に関する知識と運用に関するインサイトを得ます。 例えば、_1 つのJourney Optimizer サンドボックスにいくつのライブアクティビティを持つことができますか？_ Experience Leagueや他のAdobe データストアからすぐに回答が得られます。

また、AI アシスタントは、運用インサイト（ベータ版）にも役立ちます。 例えば、過去 7 日間に作成されたジャーニーの数をすばやく把握できます。

運用上のインサイトを得るために、AI アシスタントは顧客固有のデータ ストアに対してクエリを実行します。 データストアには、[!UICONTROL ジャーニー] に関する一元化された運用データが含まれています。 この機能は顧客に依存せず、ビジネスオブジェクトからのみメタデータを取り込みます。 サンドボックス内のデータにはアクセスしません。

[詳細情報](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)

Adobe Fireflyとの互換性：**いいえ**

## Journey Optimizer PrimeおよびUltimateの AI アシスタント {#ajo-prime-ultimate}

Journey Optimizer PrimeおよびUltimateでは、コンテンツアクセラレーター用の AI アシスタントを使用して、テキストおよび画像に対するプロアクティブなコンテンツバリエーションの提案を行います。

この機能は、メール、プッシュ通知、web ページ、コンテンツおよび SMS チャネルで使用できます。 プロンプトベースのテキストと画像を生成できます。 AJO PrimeおよびUltimateのコンテンツアクセラレーターの出力は保証されません

[詳細情報](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Adobe Fireflyとの互換性：**はい**

## Journey Optimizer B2B editionの AI アシスタント {#ajo-b2b}

Journey Optimizer B2B editionでは、AI アシスタントを使用して、商品の知識を支援します。

[詳細情報](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Adobe Fireflyとの互換性：**いいえ**

## Campaign Managed Cloud Services の AI アシスタント {#campaign-cs}

Campaign Managed Cloud Services では、コンテンツアクセラレーターに AI アシスタントを使用します。 この機能を使用すると、ブランドの概要を示すスタイル、レイアウト、トーンなどに最適化されたコンテンツを使用して、マーケティング目標に基づいてパーソナライズされた魅力的で効果的なコンテンツを自動生成できます。 メール、SMS、プッシュなど、様々なチャネルで使用できます。

**メモ：** Campaign Managed Cloud Services のコンテンツアクセラレーターからの出力は除外されます。

[詳細情報](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Adobe Fireflyとの互換性：**はい**

## Customer Journey Analyticsの AI アシスタント {#cja}

Customer Journey Analyticsでは、AI アシスタントを使用して、Experience Leagueから製品に関する知識やインサイトを得ることができます。 初めて使用する場合は、Customer Journey Analyticsの概念を素早く理解し、製品や機能のオンボーディングをおこないます。

経験豊富なユーザーが高度なユースケースを取得したり、タスクを迅速に実行するための戦略を学んだりします。 概念の理解、問題のトラブルシューティング、情報の検索。

[詳細情報](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

Adobe Fireflyとの互換性：**いいえ**

## Customer Journey Analyticsのインテリジェントキャプション {#cja-captions}

Customer Journey Analyticsのインテリジェントキャプションは、最も頻繁に使用されるWorkspace ビジュアライゼーションに対して自然言語のインサイトを提供します。 インテリジェントキャプションは、他のユーザーと共有するためにストーリーとコンテキストを必要とするアナリストに最適です。 ビジネスユーザーは、これを使用して、大まかな留意点をすばやく見つけることができます。

[詳細情報](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

Adobe Fireflyとの互換性：**いいえ**

## Real-Time CDPの AI アシスタント {#rtcdp}

Real-Time CDPでは、AI アシスタントを使用して、Experience Leagueの製品知識を提供します。 また、運用に関するインサイト（ベータ版）も提供します。 AI アシスタントが、AEP サンドボックス内にパーティション化された、一元化された運用データを含む、顧客固有の運用インサイトデータストアに対してクエリを実行します。 システムは、属性、オーディエンス、データフロー、データセット、宛先、スキーマおよびソースからのみメタデータを取り込み、サンドボックス内のデータにはアクセスしません。

例えば、オーディエンスに関するクエリを実行する場 [!DNL AI Assistant]、オーディエンスの名前および他の関連メタデータにアクセスできますが、そのオーディエンス内のプロファイルにはアクセスできません。

[詳細情報](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home)

Adobe Fireflyとの互換性：**いいえ**

## MarketoのDynamic Chat {#marketo}

Adobe Dynamic Chatのジェネレーティブ AI を活用した機能により、営業担当者の生産性を最適化し、Web サイトの訪問者の意図に関するインサイトを得て、訪問者の質問に安全な方法で対応できます。 質問、回答および会話の概要を事前承認できます。

[詳細情報](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Adobe Fireflyとの互換性：**いいえ**

## Workfrontの AI アシスタント {#workfront}

Workfrontの AI アシスタントは、アプリ内の情報や提案を提供することで、作業を達成するのに役立ちます。 実行できる操作は、次のとおりです。

* 一部のオブジェクトの概要を取得して、オブジェクトの意図や詳細の概要を表示します。
* Experience Leagueに関する質問や回答の検索 [!DNL AI Assistant] 行います。
* プロンプトに基づいて生成された式を取得します。 また、計算フィールドでの無効なカスタム式のエラーを解決することもできます。
* プロジェクト、タスクおよび問題を見つけます。

[詳細情報](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Adobe Fireflyとの互換性：**いいえ**
