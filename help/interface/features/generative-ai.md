---
title: Experience Cloud アプリケーションの AI
description: Experience Cloud アプリケーションでジェネレーティブ AI と AI アシスタントがどのように使用されるかを説明します。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
hide: false
hidefromtoc: true
index: n
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: d54af09033b1a0727e9b7aa3dbf4a9be6003a8ea
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 3%

---

# Experience Cloud アプリケーションの AI

このページは、生成 AI の概要とExperience Cloud アプリケーションで生成 AI を使用する方法を理解するのに役立ちます。 ジェネレーティブ AI と AI アシスタントを使用する製品機能はどれか、およびAdobe Fireflyがサポートされているかどうかを説明します。

## ジェネレーティブ AI と AI アシスタントについて

ジェネレーティブ AI は、単に質問に答えるだけでなく、それを実現する人工知能の一種です。 コンテンツを _作成_ し、_プロンプト_ （質問とステートメント _に対して_ 応答」します。

* **作成：** トレーニングと入力プロンプトに基づいて、新しいコンテンツ（テキスト、画像、音楽、ビデオ）をゼロから生成する AI 機能を指します。 この機能は、生成 AI の _生成_ 側面です。

* **回答：** 特定のプロンプトに対して回答や反応を提供する AI を指し、通常は知識や推論機能を利用します。

Experience Cloudを初めて使用する場合は、ジェネレーティブ AI を使用して、商品に関する知識をすばやく得ることができます。 経験豊富なユーザーであれば、数時間ではなく数秒で運用インサイトを見つけることができます。

### AI アシスタント

[AI アシスタント ](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) は、Experience Platformおよび関連アプリケーションでサポートされる対話型ツールです。 ワークフローの迅速化、製品知識の向上、問題のトラブルシューティング、情報検索に使用できます。 特定のアプリケーションでは、AI アシスタントを使用すると、運用上のインサイトをすぐに見つけることができます。

Experience Leagueからの商品のナレッジレスポンスは、検証可能であり、リンクで引用されています。 AI アシスタントを最大限に活用するための [ 目標ベースのプロンプト ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) のタイプについて説明します。

## AI をサポートする機能を備えたアプリケーション

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

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home) は機能ではなく、ジェネレーティブな AI 駆動型プラットフォームです。 そのジェネレーティブ AI 機能は、マーケティングコンテンツの作成、レビュー、共有、分析の方法を変えます。

[ 作成 ](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview) ホームでは、パフォーマンスの高いオンブランドのエクスペリエンスを作成できます。 コンテンツ生成対象：

* メール
* メタ広告
* LinkedIn 広告
* 広告の表示
* バナー

また、例、お客様のペルソナや商品の説明、ブランドガイドラインを使用して、ブランドに関するGenStudio for Performance Marketingのトレーニングを行うこともできます。 [詳細情報...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**Adobe Fireflyとの互換性：** 予定

### Experience Manager Sitesでのバリエーションの生成 {#aem-sites}

AEM Sitesの [ バリエーションを生成 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations) では、生成 AI を使用して、プロンプトに基づくコンテンツのバリエーションを作成します。 これらのプロンプトは、[Adobeによって提供されるか ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started)[users](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt) によって作成および管理されます。

バリエーションを作成した後、Web サイトでコンテンツを使用し、Edge Delivery Servicesの実験機能を使用して、その成功を測定できます。

### 入力フィールドと出力フィールド

**入力：** 入力フィールドは次のとおりです。

* 生成するバリエーションの数
* オーディエンス Source
* Audience Target
* 追加のコンテキスト
* 顧客主導のプロンプト

**出力：** 生成されたコンテンツ/市場コピー。 また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。

詳しくは、[ 画像の生成 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image) を参照してください。

**Adobe Firefly対応：** はい

## Journey Optimizer の AI アシスタント {#journey-optimizer}

Journey Optimizerでは、AI アシスタントを使用すると、製品に関する知識や運用に関するインサイトを得ることができます。

**製品知識：** AI アシスタントは、製品insightのAdobe データストア（Experience League製品ドキュメントなど）に対してクエリを実行します。 出力は、顧客に依存しません。

例：

* _1 つのAdobe Journey Optimizer サンドボックスに含めることができるライブアクティビティの数_

**オペレーショナルインサイト（Beta）** - AI アシスタントは、顧客のサンドボックスで分割された、ジャーニーに関する一元化されたオペレーショナルデータを含む、顧客固有のオペレーショナルインサイトデータストアに対してクエリを実行します。 この機能は、ビジネスオブジェクトからメタデータのみを取り込み、サンドボックス内のデータにはアクセスしません。

プロンプトの例：

* _過去 7 日間に作成されたジャーニーの数_

オペレーショナルインサイトの出力は、顧客のビジネスオブジェクトから取り込まれたメタデータに依存します。 この出力は、顧客に依存しません。

_ジャーニー_ はJourney Optimizerの AI アシスタントで使用できる唯一のオブジェクトであり、メタデータは現在のサンドボックスから取り込まれます。 [詳細情報...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)。

**Adobe Firefly対応：** いいえ

## Journey Optimizer PrimeおよびUltimateの AI アシスタント {#ajo-prime-ultimate}

Journey Optimizer PrimeとUltimateでは、[ コンテンツアクセラレーターの AI アシスタント ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) を使用して、テキストや画像に対するプロアクティブなコンテンツバリエーションの提案を行います。

この機能は、[ メール ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email)、[ プッシュ通知 ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push)、[web ページ ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web)、[ コンテンツ ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)、[SMS](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) の各チャネルで使用できます。 プロンプトベースのテキストと画像を生成できます。

**メモ：** AJO PrimeおよびUltimateのコンテンツアクセラレーターからの出力は除外されます

**Adobe Firefly対応：** はい

## Journey Optimizer B2B editionの AI アシスタント {#ajo-b2b}

Journey Optimizer B2B editionでは、製品ナレッジプロンプトに基づいて、[AI アシスタント ](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview) を使用して製品のナレッジサポートを提供します。

**製品知識** – 製品insight用のAdobe データストア（Experience League製品ドキュメントなど）をクエリします。 この出力は、顧客に依存しません。

* **入力：** アカウントジャーニーでメールを送信するにはどうすればよいですか？

* **出力：** Experience League（公開ドキュメント）から製品知識を取り込みます。 [詳細情報...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/question-guidance)

**Adobe Firefly対応：** いいえ

## Campaign Managed Cloud Services の AI アシスタント {#campaign-cs}

Campaign Managed Cloud Services では、[ コンテンツアクセラレーター用 AI アシスタント ](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) を使用します。 この機能を使用すると、ブランドの概要を示すスタイル、レイアウト、トーンなどに最適化されたコンテンツを使用して、マーケティング目標に基づいてパーソナライズされた魅力的で効果的なコンテンツを自動生成できます。 [ メール ](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content)、[SMS](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms)、[ プッシュ ](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) など複数のチャネルで使用できます。

**メモ：** Campaign Managed Cloud Services のコンテンツアクセラレーターからの出力は除外されます。

**Adobe Firefly対応：** はい

## Customer Journey Analyticsの AI アシスタント {#cja}

Customer Journey Analyticsでは、[AI アシスタント ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) を使用して、Experience Leagueから製品知識やインサイトを発見できます。

**プロンプトの例：** 計算指標を作成するにはどうすればよいですか？

新規ユーザーは、このツールを使用してCustomer Journey Analyticsの概念を学習し、なじみのない製品や機能に自分をオンボーディングできます。

経験豊富なユーザーは、AI アシスタントを使用して、より高度なユースケースやヒントやテクニックを提示し、迅速にタスクを実行できます。 概念の理解、問題のトラブルシューティング、情報の検索。 [詳細情報...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge)

**Adobe Firefly対応：** いいえ

## Customer Journey Analyticsのインテリジェントキャプション {#cja-captions}

Customer Journey Analyticsの [ インテリジェントキャプション ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) では、最も頻繁に使用されるWorkspaceのビジュアライゼーションに対して自然言語のインサイトが提供されます。

**Adobe Firefly対応：** いいえ

## Real-Time CDPの AI アシスタント {#rtcdp}

Real-Time CDPでは、[AI アシスタント ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) を使用して、Experience Leagueから製品知識やインサイトを発見できます。 質問する際の [ ヒントを得る ](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions)。

また、運用に関するインサイト（ベータ版）も提供します。 AI アシスタントが、顧客のAEP サンドボックスで分割された、一元化された運用データを含む、顧客固有の運用インサイトデータストアに対してクエリを実行します。 属性、オーディエンス、データフロー、データセット、宛先、スキーマおよびソースからのみメタデータを取り込み、サンドボックス内のデータにはアクセスしません。

例えば、オーディエンスに関するクエリの場 [!DNL AI Assistant]、オーディエンスの名前および他の関連メタデータにアクセスできますが、そのオーディエンス内のプロファイルにはアクセスできません。

例：

* 入力：_持っているデータセットの数は？_

* 応答：_オペレーショナルインサイトの出力は、顧客のビジネスオブジェクト（属性、オーディエンス、データフロー、データセット、宛先、スキーマ、ソース）から取り込まれたメタデータに依存し、クエリされたデータを含む特定の UI ページへのリンクを含みます。_

その他の例については、Experience Platformの _AI アシスタントの_ Product Knowledge _および [Operational Insights_ 入力テーブルを参照してください ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home)

**Fireflyとの互換性：** いいえ

## MarketoのDynamic Chat {#marketo}

[Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) は、カスタマイズされた承認済みの質問と回答、および会話の概要を使用して、AI による会話を作成します |<ul><li> **質問の生成：** コンテンツを抽出して質問/回答の生成に使用する URL を指定します。 </li><li> **会話の概要：** チャット会話の概要を生成します。 </li></ul> [ 詳細情報…](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  |いいえ |

## Workfrontの AI アシスタント {#workfront}

Workfrontの [AI アシスタント ](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) を使用すると、自然言語での会話でアプリ内の情報や提案を提供することで、作業を完了できます。 AI アシスタントは次の機能を提供します：プロジェクト/タスク/イシュー/ドキュメントをまとめ、Experience LeagueのWorkfront ドキュメントから取り込んだ手順や参照情報を提供し、計算カスタムフィールドの式を生成または絞り込みます。  | <ul><li>**プロジェクト入力の要約：** このプロジェクトの要約 </li><li> **プロジェクト出力の要約：** プロジェクトの目的と状態に関する簡単な説明を返し、完了したタスクとまだ保留中のタスクの例を示し、追加の詳細とメモも提供します。</li><li> **数式の入力を生成/調整：** 「この式を書き換えて、無効な式エラーを削除します。」 </li><li> **フォーミュラの生成/調整の出力：** 生成または調整されたフォーミュラ </li></ul>**メモ：** AI アシスタントでは、式のサイズと複雑さに応じて、改訂された式を生成するのに数分かかる場合があります。 |いいえ  |


<!-- ## Experience Cloud applications that use AI

Learn how Experience Cloud applications use generative AI or AI Assistant, and whether Adobe Firefly is supported. 

| Application | How Generative AI Is Used | Examples | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) is a generative AI-driven platform. It infuses the content creation lifecycle with generative AI capabilities that transform how marketing content is created, reviewed, shared, and analyzed.<br>You can train GenStudio for Performance Marketing on your brand using examples, descriptions of customer personas and products, and brand guidelines. |_GenStudio for Performance Marketing Create_ lets you generate content for emails, Meta ads, LinkedIn ads, display ads, and banners. <br>**Inputs:** <ul><li>Use templates to start the content creation process. </li><li>Add parameters like Brands, Products, and Personas (guidelines) and Content (assets) to shape the generated experience. </li><li>Enter descriptive prompts that describe the context or experience you intend to generate. [Learn more...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> |Yes |
|Adobe Experience Manager Sites (Cloud Service)  | AEM Sites uses [Generate Variations](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generate Variations uses generative AI to create content variations based on prompts. These prompts are either provided by Adobe or created and managed by users. |After creating variations, you can use the content on your website and measure its success using the Experimentation functionality of Edge Delivery Services. <br>**Input:** Input fields include Number of Variations to generate; Audience Source / Audience Target; Additional Context, and customer-driven prompts. <ul><li>[Adobe prompt template](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[User generated prompt](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Output:** Generated Content / Market Copy. You also have the option to generate images in Adobe Express using the generative AI capabilities of Firefly. See [Generate Image](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Yes|
| Adobe Journey Optimizer |Journey Optimizer uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) with two classes of questions:<ul><li>**Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. </li><li>**Operational Insights (Beta)** - queries a customer-specific operational insights data store that contains centralized operational data about Journeys, partitioned by the customer's sandbox. Pulls metadata only from business objects and does not access data within the sandbox.</li></ul>|<ul><li>**Product Knowledge Input:** How many live activities can I have in one Adobe Journey Optimizer sandbox?</li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li>**Operational Insights Input:** How many Journeys have been created in the last seven days? </li><li>**Operational Insights Output:** Operational Insights output depends on metadata pulled from customer's business objects. Journeys is the only object available in AJO, and metadata is pulled from the current sandbox. </li></ul> See [Work with the AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) and [Field Readiness](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ and _Ultimate_  | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) brings proactive content variation suggestions for text and images. It is available for email, push, web and SMS channels. This new capability provides prompt-based text and image generation. |<ul><li> **Email** - generate a full email, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Push Notification** - Generate a full push notification, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Generate a full SMS, or text only. [Learn more](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Webpage** - Generate web page images or web page text. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Content** - Generate content for various messaging campaigns. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Note:** Output from Content Accelerator in AJO Prime and Ultimate is indemnified. | Yes   |
| Journey Optimizer B2B Edition  | Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) with one class of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. | <ul><li>**Input:** How do I send an email in an account journey?</li><li>**Output:** Product Knowledge pulls from Experience League (public documentation). [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | No   |
| Campaign Managed Cloud Services | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) auto-generates personalized, engaging, and effective content based on the marketing objective with content optimized for brand outlined styles, layouts, tone, and more across channels like Email, SMS, Push. |<ul><li> **Email** - Generate a full email, text only or image only. [Learn more](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Generate full SMS or text only. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push** - Craft compelling messaging and generate content. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Note:** Output from Content Accelerator in Campaign Managed Cloud Services is indemnified. | Yes  |
| Customer Journey Analytics   | CJA uses [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) to help you discover product knowledge and insights from Experience League. <br>For example, new users can use it to learn Customer Journey Analytics concepts and onboard yourself to products and features that you are unfamiliar with. <br>Experienced users can use AI Assistant to present more advanced use cases or tips and tricks and perform tasks at a fast pace. Understand concepts, troubleshoot problems, or search for information. [Learn more...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Product Knowledge Input:** How do I build a calculated metric? </li><li> **Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li></ul> | No |
| Customer Journey Analytics    | [Intelligent Captions](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) provides natural-language insights for line visualizations in Workspace visualizations.| <ul><li>**Input:** Line visualizations. Captions are auto-generated based on such line visualizations when you click **Intelligent captions**. </li><li> **Output:** Auto-generated natural-language captions.</li></ul>  | No             |
| Real-Time CDP |Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) to help you discover product knowledge and insights from Experience League. It queries a database and translates data from the database into a human-readable answer. Two classes of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. <br> **Operational Insights (Beta)** - Queries a customer-specific operational insights data store that contains centralized operational data, partitioned by the customer's AEP sandbox. Pulls metadata only from Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources, and does not access data within the sandbox. <br>For example, for a query about an audience [!DNL AI Assistant] can access the name of the audience and other associated metadata but cannot access the profiles within that audience. | <ul><li>**Product Knowledge Input:** How is profile richness calculated? </li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li> **Operational Insights Input:** How many datasets do I have? </li><li> **Operational Insights Output:** Operational Insights output depends on metadata pulled from Customer's business objects (Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources), and includes a link to specific UI page containing queried data. </li></ul>For examples, see the _Product Knowledge_ and _Operational Insights_ input tables in [AI Assistant in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)  | No |
| Marketo  | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) creates AI-assisted conversations with customized and pre-approved questions and answers, as well as conversation summary |<ul><li> **Generate Questions:** Provide URLs from which content is extracted and used to generate questions / responses. </li><li> **Conversation Summary:** Generates a summary of a chat conversation. </li></ul> [Learn more...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |
| Workfront | [AI Assistant](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront helps you accomplish your work by offering in-app information and suggestions in a natural-language conversation. AI Assistant offers the following functionality: Summarizes projects/tasks/issues/documents, provides instructions or reference information pulled from the Workfront documentation on Experience League, generates or refines formulas for calculated custom fields.  | <ul><li>**Summarize Project Input:** Summarize this project </li><li> **Summarize Project Output:** Returns brief descriptions of the project's purpose and status, gives examples of tasks that are completed and that are still pending, and provides some additional details and notes.</li><li> **Generate/Refine Formula Input:** "Rewrite this formula to remove the invalid expression error." </li><li> **Generate/Refine Formula Output:** Generated or refined formula. </li></ul>**Note:** AI Assistant may take a few moments to generate the revised formula, depending on the size and complexity of the formula. | No  | -->
