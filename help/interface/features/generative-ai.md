---
title: Experience Cloud アプリケーションのジェネレーティブ AI
description: ジェネレーティブ AI （GenAI）と、Experience Cloud アプリケーションで GenAI および  [!DNL AI Assistant] がどのように使用されるかについて説明します。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: c7cea04619bdf74c4037bef0de9a1c22596e41cb
workflow-type: tm+mt
source-wordcount: '1640'
ht-degree: 3%

---

# Experience Cloud製品のジェネレーティブ AI

Experience Cloudのジェネレーティブ AI （genAI）は、クリエイティブおよび認知機能のタスクを自動化し、生産性を向上させるのに役立ちます。 ここでは、Experience Cloud アプリケーションで genAI および AI アシスタントがサポートされている場所について説明し、これらの機能の詳細に関するリンクを示します。

**genAI とは**

ジェネレーティブ AI は、オリジナルのコンテンツを作成できる AI の一種です。 例えば、ユーザーのプロンプトや要求に応じて、テキスト、画像、ビデオ、オーディオまたはソフトウェアコードを作成できます。

* **作成：** トレーニングおよび入力プロンプトに基づいて、コンテンツ（テキスト、画像、音楽、ビデオ）をゼロから生成する機能。 この機能は、生成 AI の _生成_ 側面です。

* **応答を生成：** AI は、通常、使用可能なデータとナレッジリポジトリを利用して、プロンプトに対する回答や反応を提供します。

**[!DNL AI Assistant] とは？**

[!DNL AI Assistant] は、Experience Platformおよび関連アプリケーションでサポートされる対話型ツールです。 これを使用すると、サポート対象の製品で _製品の知識_ および _運用に関するインサイト_ を迅速に得ることができます。

* **商品知識：** 商品知識とは、Experience Leagueのドキュメントに基づいた概念やトピックを指します。 [!DNL AI Assistant] を最大限に活用するために、効果的な [ 目標ベースのプロンプト ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) を作成する方法を説明します。 Experience Leagueからの回答はすべて検証可能で、リンク付きで引用されます。

* **オペレーショナルインサイト：**&#x200B;[ オペレーショナルインサイト ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/questions#objects-questions) メタデータオブジェクト（属性、オーディエンス、データフロー、データセットなど）に関して生成される応答を参照します。 [!DNL AI Assistant] を使用すると、他の方法では数時間や数日かかることがある作業を、数秒で完了できます。

* **カスタマーサポート**: [ 製品サポートエージェント ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/new-features/customer-support) は、Experience Platformの機能とアプリケーションに使用できる、[!DNL AI Assistant] のセルフサービスデバッグ機能とトラブルシューティング機能です。 ワークフローを離れることなくサポートの問題をトラブルシューティングしたり、カスタマーサポートチケットを作成したり、AI アシスタントを使用してケースの進行状況を追跡したりできます。

  **メモ：** この機能はAlphaにあり、組織で使用できない可能性があります。 Alpha プログラムに参加してこの機能にアクセスするには、Adobe アカウントチームにお問い合わせください。

[AI アシスタントの詳細 ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/landing)

## Experience Cloud製品での GenAI の可用性 {#products}

次のExperience Cloud アプリケーションは、生成 AI または [!DNL AI Assistant] をサポートしています。 Adobe Fireflyのサポートも製品ごとに示されます。

更新日：**2025 年 6 月 4 日**

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] Managed Cloud Services](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## パフォーマンスマーケティング用の GenStudio {#gspm}

[!DNL GenStudio for Performance Marketing] は、企業のマーケティングチームが有料メディア、メール、ディスプレイ広告などのチャネルをまたいでオンブランドのキャンペーンコンテンツを作成、アクティブ化、最適化するのを支援するように設計されたジェネレーティブ AI アプリケーションです。

パフォーマンスマーケターは、自然言語プロンプトを使用して、ブランドに準拠したパーソナライズされたアセットを生成できます。 GenStudio for Performance Marketingは、キャンペーンの実行を促進し、ブランドの整合性を損なうことなくコンテンツの制作を拡張し、全体的な ROI を向上させるパフォーマンス分析を提供します。

[詳細情報](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home)

Adobe Fireflyとの互換性：**はい**

## [!DNL Experience Manager] {#aem}

次の節では、AEM アプリケーションのジェネレーティブ AI について簡単に説明します。

### Experience Manager Sites

AEM Sitesでは、「バリエーションを生成 _[!UICONTROL を使用でき]_ す。 この機能は、ジェネレーティブな人工知能を使用して、入力プロンプトに基づくコンテンツのバリエーションを作成します。 プロンプトは、Adobeから提供されるか、ユーザーが作成および管理します。

バリエーションを作成した後、Web サイトでコンテンツを使用し、Edge Delivery Servicesの [ 実験 ](https://www.aem.live/docs/experimentation) 機能を使用して、その成功を測定できます。 また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。

**入力と出力の例**

入力フィールドは次のとおりです。

* 生成するバリエーションの数
* オーディエンス Source
* Audience Target
* 追加のコンテキスト
* 顧客主導のプロンプト

出力は、生成されたコンテンツや市場コピーです。

Adobe Fireflyとの互換性：**はい**

[詳細情報](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

### Experience Manager Assets

AEM Assetsでは、**Content Hub** および **AI によって生成されたスマートタグ** で生成 AI を使用できます。

Adobe Fireflyとの互換性：**はい**

**Content Hub**

[!UICONTROL Content Hub] は、組織やビジネスパートナーがブランド上のコンテンツにアクセスすることを民主化するための [!DNL Experience Manager Assets as a Cloud Service] の一部として利用できます。 大規模なアクティベーション用のアセットの配布と、マーケティングの俊敏性を向上させるためのオンブランドコンテンツバリアントの作成に重点を置いています。

Content Hubでは、Adobe Expressを使用してコンテンツを作成できます（Adobe Expressの使用権限がある場合）。 シンプルなツールで既存のコンテンツを編集し、テンプレートやブランド要素を使用してオンブランドのバリエーションを作成し、[!DNL Adobe Firefly] から最新の GenAI 機能を使用してコンテンツを作成できます。 [詳細情報](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview)

**スマートタグ**

AI では、手動入力に依存するのではなく、デジタルアセットに説明的なタグを自動的に割り当てることができます。 これらの AI で生成されるタグは、メタデータの品質を向上させ、アセットの検索、分類およびレコメンデーションを容易にします。

例えば、アセットが画像の場合、AI はオブジェクト、シーン、感情、さらにはブランドロゴを識別できます。 _sunset_、_beach_、_vacation_、_smiling_ などの関連するタグを生成できます。 [詳細情報](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/manage/smart-tags#ai-smart-tags)

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

[!DNL Journey Optimizer] （AJO）では、[AI アシスタント ](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/ai-assistant) を使用して _製品に関する知識_ および _運用に関するインサイト_ （ベータ版）を取得できます。

### AJOでの AI アシスタントの使用例

製品知識の入力例を次に示します。

* _1 つのJourney Optimizer サンドボックスに含めることができるライブアクティビティの数_

  出力は、Experience Leagueおよびその他のAdobe データストアから生成されます。

次に、運用インサイトに対する入力の例を示します。

* _過去 7 日間に作成されたジャーニーの数_

  出力用に、AI アシスタントが顧客固有のデータ ストアに対してクエリを実行します。 データストアには、[!UICONTROL ジャーニー] に関する一元化された運用データが含まれています。 この機能は顧客に依存せず、ビジネスオブジェクトからのみメタデータを取り込みます。 サンドボックス内のデータにはアクセスしません。

[詳細情報](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/ai-assistant)

Adobe Fireflyとの互換性：**いいえ**

### コンテンツ生成用 AI アシスタント（AJOPrimeおよびUltimate） {#ajo-prime}

AJO _Prime_ および _Ultimate_ では、[ コンテンツ生成 ](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) をコンテンツ生成に使用して、テキストや画像に対するプロアクティブなコンテンツバリエーションの提案を行うことができます。

この機能は、メール、プッシュ通知、web ページ、コンテンツおよび SMS チャネルで使用できます。 プロンプトベースのテキストと画像を生成できます。 AJO PrimeおよびUltimateでのコンテンツ生成からの出力は除外されます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Adobe Fireflyとの互換性：**はい**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B editionでは、[!DNL AI Assistant] を使用して商品の知識を支援します。

入力例：

* _アカウントジャーニーでメールを送信するにはどうすればよいですか？_

  製品ナレッジ出力はExperience Leagueから取り込まれます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Campaign] Managed Cloud Services {#campaign-cs}

Campaign Managed Cloud Services は、コンテンツ生成に [!DNL AI Assistant] を使用します。 この機能を使用すると、ブランドの概要を示すスタイル、レイアウト、トーンなどに最適化されたコンテンツを使用して、マーケティング目標に基づいてパーソナライズされた魅力的で効果的なコンテンツを自動生成できます。 メール、SMS、プッシュなど、様々なチャネルで使用できます。

**メモ：** Campaign Managed Cloud Services のコンテンツ生成からの出力は除外されます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Adobe Fireflyとの互換性：**はい**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analyticsでは、生成 AI を次のように使用できます。

* 製品に関する知識の [!DNL AI Assistant]
* AI アシスタントの [!DNL Product Support Agent] （現在はAlpha）
* Workspaceのビジュアライゼーションでの [!UICONTROL &#x200B; インテリジェントキャプション &#x200B;]
* [!DNL Content Analytics] で各アセットメタデータを自動的に割り当てる AI および GenAI

Adobe Fireflyとの互換性：**いいえ**

**AI アシスタント**

Experience Leagueの製品に関する知識を確認します。 初めて使用する場合は、Customer Journey Analyticsの概念を素早く理解し、製品や機能のオンボーディングをおこないます。 例：

* _アカウントジャーニーでメールを送信するにはどうすればよいですか？_

経験豊富なユーザーが高度なユースケースを取得したり、タスクを迅速に実行するための戦略を学んだりします。 概念の理解、問題のトラブルシューティング、情報の検索をすばやく行うことができます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

**インテリジェントキャプション**

[!DNL Customer Journey Analytics] で _インテリジェントキャプション_ を使用して、最も頻繁に使用されるWorkspaceのビジュアライゼーションに関する自然言語のインサイトを取得できます。 インテリジェントキャプションは、他のユーザーと共有するためにストーリーとコンテキストを必要とするアナリストに最適です。 ビジネスユーザーは、これを使用して、大まかな留意点をすばやく見つけることができます。

例：

* **入力：** CJAで、サポートされているビジュアライゼーション（折れ線グラフ、面グラフ、棒グラフ、フロー、フォールアウトを含む）を実行し、**[!UICONTROL インテリジェントキャプション]** をクリックします。

* **出力：** コンテキストと重要な留意点を示す、自動生成された自然言語キャプションの表示。 その後、生成されたデータに対して、レビュー、コピー、組織との共有などのアクションを実行できます。 [ 方法を参照 ](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[詳細情報](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

**Content Analytics**

Content Analyticsでは、AI と GenAI を使用して、サブジェクト、シーン、前景色などのすべてのアセットメタデータを自動的に割り当てます。 属性は、アセットまたはエクスペリエンスの内容を説明する、AI によって割り当てられたメタデータタグです。

例：前景 `color: red` は、自動的に割り当てられる属性です。 ビジュアライゼーションは、アセットのどの属性がコンバージョンに最も貢献しているかを特定するのに役立ちます。 [詳細情報](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/report/report#template)

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDPでは、Experience Leagueの製品知識の取得を支援するために [!DNL AI Assistant] を使用しています。 また、運用に関するインサイト（ベータ版）も提供します。 [!DNL AI Assistant] は、AEP サンドボックス内にパーティション化された、一元化された運用データを含む、顧客固有の運用インサイトデータストアをクエリします。 システムは、属性、オーディエンス、データフロー、データセット、宛先、スキーマおよびソースからのみメタデータを取り込み、サンドボックス内のデータにはアクセスしません。

例えば、オーディエンスに関するクエリを実行する場 [!DNL AI Assistant]、オーディエンスの名前および他の関連メタデータにアクセスできますが、そのオーディエンス内のプロファイルにはアクセスできません。

[詳細情報](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Marketo] {#marketo}

Marketoでは、インタラクティブ Web セミナーやDynamic Chatでジェネレーティブ AI を利用できます。

**インタラクティブウェビナー**

録画したウェビナーのチャプターと概要を自動的に生成し、オーディエンスがアクセスしやすく、簡単に移動できるようにします。 次のような機能があります。

* チャプターの自動生成
* AI 生成テキストの概要
* 編集可能なコンテンツ – 生成されたチャプターと概要を変更
* 簡単な統合 – 選択した web ページエディターにHTML コードをコピーして、ランディングページに章や概要を追加できます

[詳細情報](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai)

**Dynamic Chat**

Adobe Dynamic Chatのジェネレーティブ AI を活用した機能により、営業担当者の生産性を最適化し、Web サイトの訪問者の意図に関するインサイトを得て、訪問者の質問に安全な方法で対応できます。 質問、回答および会話の概要を事前承認できます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Adobe Fireflyとの互換性：**いいえ**

## [!DNL Workfront] {#workfront}

[!DNL Workfront] の [!DNL AI Assistant] は、アプリ内情報や提案を提供することで、作業を完了するのに役立ちます。 実行できる操作は、次のとおりです。

* 一部のオブジェクトの概要を取得して、オブジェクトの意図や詳細の概要を表示します。
* Experience Leagueに関する質問や回答の検索 [!DNL AI Assistant] 行います。
* プロンプトに基づいて生成された式を取得します。 また、計算フィールドでの無効なカスタム式のエラーを解決することもできます。
* プロジェクト、タスクおよび問題を見つけます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Adobe Fireflyとの互換性：**いいえ**

## その他のリソース

* [ トラストセンターの責任ある AI リソース ](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**免責事項：** このページの情報は、一般的な情報提供のみを目的としています。 当社は正確かつ最新の情報を提供することを目指していますが、ソフトウェアや AI の機能は頻繁に変更される可能性があります。 当社は、情報の完全性または信頼性を常に保証するものではありません。 このコンテンツに基づいて決定を下す前に、重要な詳細を再確認してください。
