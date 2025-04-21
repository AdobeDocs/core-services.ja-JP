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
source-git-commit: c6285bb87885d020275c6c0b4c003e912026ad20
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 4%

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

入力フィールドは次のとおりです。

* 生成するバリエーションの数
* オーディエンス Source
* Audience Target
* 追加のコンテキスト
* 顧客主導のプロンプト

出力は、生成されたコンテンツや市場コピーです。

また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。 [詳細情報...](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)

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

Customer Journey Analyticsでは、[AI アシスタント ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) を使用して、Experience Leagueから製品知識やインサイトを発見できます。

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

* 応答：オペレーショナルインサイトの出力は、顧客のビジネスオブジェクト（属性、オーディエンス、データフロー、データセット、宛先、スキーマ、ソース）から取り込まれたメタデータに依存し、クエリされたデータを含む特定の UI ページへのリンクが含まれます。

その他の例については、Experience Platformの _AI アシスタントの_ Product Knowledge _および [Operational Insights_ 入力テーブルを参照してください ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home)

**Fireflyとの互換性：** いいえ

## MarketoのDynamic Chat {#marketo}

Adobe Dynamic Chatのジェネレーティブ AI を活用した機能により、営業担当者の生産性を最適化し、Web サイトの訪問者の意図に関するインサイトを得て、訪問者の質問に安全な方法で対応できます。 質問、回答および会話の概要を事前承認できます。 [詳細情報...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

**Fireflyとの互換性：** いいえ

## Workfrontの AI アシスタント {#workfront}

Workfrontの AI アシスタントは、アプリ内の情報や提案を提供することで、作業を達成するのに役立ちます。 実行できる操作は、次のとおりです。

* 一部のオブジェクトの概要を取得して、オブジェクトの意図や詳細の概要を表示します。
* Experience Leagueに関する質問や回答の検索 [!DNL AI Assistant] 行います。
* プロンプトに基づいて生成された式を取得します。 また、計算フィールドでの無効なカスタム式のエラーを解決することもできます。
* プロジェクト、タスクおよび問題を見つけます。

[詳細情報...](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

**Fireflyとの互換性：** いいえ
