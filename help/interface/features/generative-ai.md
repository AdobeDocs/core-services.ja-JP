---
title: Experience Cloud アプリケーションにおける AI
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
source-git-commit: 3f1065affe2665bb0867de02e4aef4c755c5f201
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 5%

---

# Experience Cloud アプリケーションにおける AI

このページでは、Experience Cloud アプリケーションで生成 AI がどのように使用されるか、およびアプリケーション固有の情報はどこで見つけられるかを理解するのに役立ちます。 質問、プロンプト、入力モデルと出力モデルのクラスについて説明します。

## ジェネレーティブ AI と AI アシスタントについて

ジェネレーティブ AI は人工知能の一種で、発言や質問（プロンプト _に対して_ 作成 _新しいコンテンツおよび_ 応答）を行うことができます。

* **作成：** トレーニングと入力プロンプトに基づいて、新しいコンテンツ（テキスト、画像、音楽、ビデオ）をゼロから生成する AI 機能を指します。 この機能は、生成 AI の _生成_ 側面です。

* **回答：** 特定の質問、ステートメント、プロンプトに対して回答または反応を提供する AI を指し、通常は知識や推理能力を活用します。

特定のExperience Cloud アプリケーションは、ジェネレーティブ AI を活用して、新規ユーザーが商品に関する知識を迅速に得られるよう支援し、経験豊富なユーザーが数時間ではなく数秒でオペレーショナルインサイトを見つけられるよう支援します。

### AI アシスタント

[AI アシスタント ](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) は、Experience Platformおよび関連アプリケーションでサポートされる対話型ツールです。 ワークフローの迅速化、製品知識の向上、問題のトラブルシューティング、情報検索に使用できます。 AI アシスタントを使用すると、数時間ではなく数秒で運用インサイトを見つけることができます。

すべての製品ナレッジアンサーは、Experience Leagueの製品ドキュメントへのリンクと共に、検証可能で引用されています。 [AI アシスタントの詳細 ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home)、および AI アシスタントを最大限に活用するための目標ベースのプロンプトのタイプについて説明します。

## AI を使用するExperience Cloud アプリケーション

>[!TIP]
>
>Subhead バージョン （開始のみ）...


* [パフォーマンスマーケティング用の GenStudio](#gspm)
* [Experience Manager Sites（Cloud Service）](#aem-sites)
* その他の予定…

### パフォーマンスマーケティング用の GenStudio {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home) は、ジェネレーティブ AI 駆動型プラットフォームです。 マーケティングコンテンツの作成、確認、共有、分析の方法を変換する生成 AI 機能をコンテンツ作成ライフサイクルに組み込みます。

_GenStudio for Performance Marketing Create_ は、Adobe GenAI の機能を活用して、マーケターや分散型チームが高パフォーマンスのオンブランドエクスペリエンスを作成できるようにします。 コンテンツ生成対象：

* メール
* メタ広告
* LinkedIn 広告
* 広告の表示
* バナー

例、お客様のペルソナや商品の説明、ブランドガイドラインを使用して、ブランドに関するGenStudio for Performance Marketingのトレーニングを実施できます。 [詳細情報](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)。

**Adobe Fireflyとの互換性：予定**

### Experience Manager Sites {#aem-sites}

AEM Sitesでは [ バリエーションの生成 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations) を使用します。 バリエーションを生成では、生成 AI を使用して、プロンプトに基づくコンテンツのバリエーションを作成します。 これらのプロンプトは、[Adobeによって提供されるか ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started)[users](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt) によって作成および管理されます。

バリエーションを作成した後、Web サイトでコンテンツを使用し、Edge Delivery Servicesの実験機能を使用して、その成功を測定できます。

**入力：** 入力フィールドは次のとおりです。

* 生成するバリエーションの数
* オーディエンス Source
* Audience Target
* 追加のコンテキスト
* 顧客主導のプロンプト

**出力：** 生成されたコンテンツ/市場コピー。 また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。

[ 画像の生成 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image) を参照してください。

**Adobe Fireflyとの互換性：** はい

## Adobe Journey Optimizer

Journey Optimizerでは、[AI アシスタント ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) を次の 2 つのクラスの質問と共に使用します。

**製品知識** – 製品insight用のAdobe データストア（Experience League製品ドキュメントなど）をクエリします。 この出力は、顧客に依存しません。 例：

* 1 つの Adobe Journey Optimizer サンドボックスにライブアクティビティをいくつ含めることができますか？

**オペレーショナルインサイト（Beta）** - ジャーニーに関する一元的なオペレーショナルデータを含み、顧客のサンドボックスでパーティション化された、顧客固有のオペレーショナルインサイトデータストアをクエリします。 ビジネスオブジェクトからメタデータのみを取り込み、サンドボックス内のデータにはアクセスしません。

* 過去 7 日間に作成されたジャーニーの数

オペレーショナルインサイトの出力は、顧客のビジネスオブジェクトから取り込まれたメタデータに依存します。

ジャーニーはJourney Optimizerの AI アシスタントで使用できる唯一のオブジェクトであり、メタデータは現在のサンドボックスから取り込まれます。

詳しくは [AI アシスタントの操作 ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) および [ フィールド対応 ](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) を参照してください。

**Adobe Fireflyとの互換性：** いいえ



## AI を使用するExperience Cloud アプリケーション

>[!TIP]
>
>テーブル バージョン…


Experience Cloud アプリケーションでジェネレーティブ AI または AI アシスタントを使用する方法と、Adobe Fireflyがサポートされているかどうかを説明します。

| アプリケーション | ジェネレーティブ AI の使用方法 | 例 | Adobe Firefly? |
|----------|------------|-----------|----------------|
| パフォーマンスマーケティング用の GenStudio | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home) は、ジェネレーティブ AI 駆動型プラットフォームです。 マーケティングコンテンツの作成、確認、共有、分析の方法を変換する生成 AI 機能をコンテンツ作成ライフサイクルに組み込みます。<br> 例、お客様のペルソナや商品の説明、ブランドガイドラインを使用して、ブランドに関するGenStudio for Performance Marketingのトレーニングを実施できます。 | _GenStudio for Performance Marketing作成_ を使用すると、メール、メタ広告、LinkedIn 広告、ディスプレイ広告、バナー用のコンテンツを生成できます。 <br>**入力：** <ul><li>テンプレートを使用して、コンテンツ作成プロセスを開始します。 </li><li>ブランド、製品、ペルソナ（ガイドライン）やコンテンツ（アセット）などのパラメーターを追加して、生成されたエクスペリエンスを形成します。 </li><li>生成するコンテキストまたはエクスペリエンスを説明する説明プロンプトを入力します。 [詳細情報...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> | ○ |
| Adobe Experience Manager Sites（Cloud Service） | AEM Sitesでは [ バリエーションの生成 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations) を使用します。 <br> バリエーションを生成は、生成 AI を使用して、プロンプトに基づくコンテンツのバリエーションを作成します。 これらのプロンプトは、Adobeから提供されるか、ユーザーが作成および管理します。 | バリエーションを作成した後、Web サイトでコンテンツを使用し、Edge Delivery Servicesの実験機能を使用して、その成功を測定できます。 <br>**入力：** 入力フィールドには、生成するバリエーションの数、Audience Source/Audience Target、追加のコンテキストおよび顧客主導のプロンプトが含まれます。 <ul><li>[Adobe プロンプト テンプレート ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[ ユーザーが生成したプロンプト ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **出力：** 生成されたコンテンツ/市場コピー。 また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。 [ 画像の生成 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image) を参照してください。 | ○ |
| Adobe Journey Optimizer | Journey Optimizerでは、[AI アシスタント ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) を次の 2 つのクラスの質問と共に使用します。<ul><li>**製品知識** – 製品insight用のAdobe データストア（Experience League製品ドキュメントなど）をクエリします。 この出力は、顧客に依存しません。 </li><li>**オペレーショナルインサイト（Beta）** - ジャーニーに関する一元的なオペレーショナルデータを含み、顧客のサンドボックスでパーティション化された、顧客固有のオペレーショナルインサイトデータストアをクエリします。 ビジネスオブジェクトからメタデータのみを取り込み、サンドボックス内のデータにはアクセスしません。</li></ul> | <ul><li>**製品知識に関する入力：** 1 つのAdobe Journey Optimizer サンドボックス内に持つことのできるライブアクティビティの数</li><li>**製品ナレッジ出力：** 製品ナレッジは、Experience League（公開ドキュメント）から取り込みます。 </li><li>**オペレーショナルインサイトの入力：** 過去 7 日間に作成されたジャーニーの数 </li><li>**Operational Insights の出力：** Operational Insights の出力は、顧客のビジネスオブジェクトから取り込まれたメタデータに依存します。 AJOで使用できる唯一のオブジェクトはジャーニーで、メタデータは現在のサンドボックスから取得されます。 </li></ul> [AI アシスタントの操作 ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) および [ フィールド対応 ](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) を参照してください。 | × |
| Journey Optimizer: _Prime_ および _Ultimate_ | [ コンテンツアクセラレーター用 AI アシスタント ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) は、テキストおよび画像に対するプロアクティブなコンテンツバリエーションの提案を提供します。 メール、プッシュ、web および SMS チャネルで使用できます。 この新しい機能は、プロンプトベースのテキストと画像の生成を提供します。 | <ul><li> **メール** – 完全なメール、テキストのみ、または画像のみを生成します。 [詳細情報...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **プッシュ通知** - テキストのみまたは画像のみの完全なプッシュ通知を生成します。 [詳細情報...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** – 完全な SMS を生成するか、テキストのみを生成します。 [詳細情報](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Web ページ** - Web ページの画像またはテキストを生成します。 [詳細情報...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **コンテンツ** – 様々なメッセージキャンペーンのコンテンツを生成します。 [詳細情報...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **メモ：** AJO PrimeおよびUltimateのコンテンツアクセラレーターからの出力は除外されます | ○ |
| Journey Optimizer B2B エディション | [AI アシスタント ](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) を使用し、次の 1 つのクラスの質問を行います。<br> **製品知識** – 製品insight用のAdobe データストア（Experience League製品ドキュメントなど）をクエリします。 この出力は、顧客に依存しません。 | <ul><li>**入力：** アカウントジャーニーでメールを送信するにはどうすればよいですか？</li><li>**出力：** Experience League（公開ドキュメント）から製品知識を取り込みます。 [詳細情報...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul> | × |
| Campaign Managed Cloud Services | [ コンテンツアクセラレーター用 AI アシスタント ](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) は、メール、SMS、プッシュなどのチャネル全体でブランドの概要スタイル、レイアウト、トーンなどに最適化されたコンテンツを使用して、マーケティング目標に基づいて、パーソナライズされた魅力的で効果的なコンテンツを自動生成します。 | <ul><li> **メール** – 完全なメール、テキストのみ、または画像のみを生成します。 [詳細情報](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** – 完全な SMS またはテキストのみを生成します。 [詳細情報...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **プッシュ** – 魅力的なメッセージを作成し、コンテンツを生成します。 [詳細情報...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **メモ：** Campaign Managed Cloud Services のコンテンツアクセラレーターからの出力は除外されます。 | ○ |
| Customer Journey Analytics | CJAでは、[AI アシスタント ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) を使用して、Experience Leagueから製品知識やインサイトを発見できます。 <br> 例えば、新規ユーザーはこのツールを使用してCustomer Journey Analyticsの概念を学習し、なじみのない製品や機能に自分をオンボーディングできます。 <br> 経験豊富なユーザーが AI アシスタントを使用して、より高度なユースケースやヒントやテクニックを紹介し、迅速にタスクを実行できます。 概念の理解、問題のトラブルシューティング、情報の検索。 [詳細情報...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**製品ナレッジ入力：** 計算指標を作成するにはどうすればよいですか？ </li><li> **製品ナレッジ出力：** 製品ナレッジは、Experience League（公開ドキュメント）から取り込みます。 </li></ul> | × |
| Customer Journey Analytics | [ インテリジェントキャプション ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) は、Workspaceのビジュアライゼーションで折れ線グラフのビジュアライゼーションに自然言語のインサイトを提供します。 | <ul><li>**入力：** 折れ線グラフのビジュアライゼーション。 キャプションは、「**インテリジェントキャプション**」をクリックすると、このような折れ線グラフのビジュアライゼーションに基づいて自動生成されます。 </li><li> **出力：** 自動生成された自然言語キャプション。</li></ul> | × |
| Real-Time CDP | [AI アシスタント ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) を使用して、Experience Leagueから製品知識やインサイトを発見できます。 データベースにクエリを実行し、データベースのデータを人間が読み取れる回答に変換します。 2 つのクラスの質問：<br> **製品知識** – 製品insight用のAdobe データストア（Experience League製品ドキュメントなど）をクエリします。 この出力は、顧客に依存しません。<br> **オペレーショナルインサイト（Beta）** – お客様のAEP サンドボックスでパーティション化された、一元化されたオペレーショナルデータを含む、お客様固有のオペレーショナルインサイトデータストアをクエリします。 属性、オーディエンス、データフロー、データセット、宛先、スキーマおよびソースからのみメタデータを取り込み、サンドボックス内のデータにはアクセスしません。 <br> 例えば、オーディエンスに関するクエリの場合、オーディエンスの名前および他の関連す [!DNL AI Assistant] メタデータにアクセスできますが、オーディエンス内のプロファイルにアクセスすることはできません。 | <ul><li>**製品ナレッジ入力：** プロファイル充実度はどのように計算されますか？ </li><li>**製品ナレッジ出力：** 製品ナレッジは、Experience League（公開ドキュメント）から取り込みます。 </li><li> **Operational Insights の入力：** データセットはいくつありますか？ </li><li> **オペレーショナルインサイトの出力：** オペレーショナルインサイトの出力は、顧客のビジネスオブジェクト（属性、オーディエンス、データフロー、データセット、宛先、スキーマ、ソース）から取り込まれたメタデータに依存し、クエリされたデータを含む特定の UI ページへのリンクを含みます。 </li></ul>例については、Experience Platformの _AI アシスタントの_ Product Knowledge _入力テーブルおよび [Operational Insights_ 入力テーブルを参照してください ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) | × |
| Marketo | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) は、カスタマイズされた承認済みの質問と回答、および会話の概要を使用して、AI による会話を作成します | <ul><li> **質問の生成：** コンテンツを抽出して質問/回答の生成に使用する URL を指定します。 </li><li> **会話の概要：** チャット会話の概要を生成します。 </li></ul> [詳細情報...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library) | × |
| Workfront | Workfrontの [AI アシスタント ](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) を使用すると、自然言語での会話でアプリ内の情報や提案を提供することで、作業を完了できます。 AI アシスタントは次の機能を提供します：プロジェクト/タスク/イシュー/ドキュメントをまとめ、Experience LeagueのWorkfront ドキュメントから取り込んだ手順や参照情報を提供し、計算カスタムフィールドの式を生成または絞り込みます。 | <ul><li>**プロジェクト入力の要約：** このプロジェクトの要約 </li><li> **プロジェクト出力の要約：** プロジェクトの目的と状態に関する簡単な説明を返し、完了したタスクとまだ保留中のタスクの例を示し、追加の詳細とメモも提供します。</li><li> **数式の入力を生成/調整：** 「この式を書き換えて、無効な式エラーを削除します。」 </li><li> **フォーミュラの生成/調整の出力：** 生成または調整されたフォーミュラ </li></ul>**メモ：** AI アシスタントでは、式のサイズと複雑さに応じて、改訂された式を生成するのに数分かかる場合があります。 | × |
