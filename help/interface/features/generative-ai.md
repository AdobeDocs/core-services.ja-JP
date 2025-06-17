---
title: Experience Cloud アプリケーションのジェネレーティブ AI
description: ジェネレーティブ AI （GenAI）と、Experience Cloud アプリケーションで GenAI および [!UICONTROL AI アシスタント &#x200B;] がどのように使用されるかについて説明します。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Artificial Intelligence
role: Admin, User
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 5c5ecaee15114ada89b317005febb39d74cf9dae
workflow-type: tm+mt
source-wordcount: '1927'
ht-degree: 5%

---

# Experience Cloud製品のジェネレーティブ AI

Experience Cloudのジェネレーティブ AI （genAI）は、クリエイティブおよび認知機能のタスクを自動化し、生産性を向上させるのに役立ちます。 ここでは、Experience Cloud アプリケーションで genAI および AI アシスタントがサポートされている場所について説明し、これらの機能の詳細に関するリンクを示します。

**genAI とは**

ジェネレーティブ AI は、オリジナルのコンテンツを作成できる AI の一種です。 例えば、ユーザーのプロンプトや要求に応じて、テキスト、画像、ビデオ、オーディオまたはソフトウェアコードを作成できます。

* **作成：** トレーニングおよび入力プロンプトに基づいて、コンテンツ（テキスト、画像、音楽、ビデオ）をゼロから生成する機能。 この機能は、生成 AI の _生成_ 側面です。

* **応答を生成：** AI は、通常、使用可能なデータとナレッジリポジトリを利用して、プロンプトに対する回答や反応を提供します。

このタイプの AI は、自律的に機能する AI を指す [Agentic AI](agentic-ai.md) （Adobeの Agentic Framework）とは対照的です。

**[!UICONTROL AI アシスタント &#x200B;] とは**

[!UICONTROL AI アシスタント &#x200B;] は、Experience Platformおよび関連アプリケーションでサポートされる対話型ツールです。 これを使用すると、サポート対象の製品で _製品の知識_ および _運用に関するインサイト_ を迅速に得ることができます。

* **商品知識：** 商品知識とは、Experience Leagueのドキュメントに基づいた概念やトピックを指します。 [!UICONTROL AI アシスタント &#x200B;] を最大限に活用するために、効果的な [ 目標ベースのプロンプト ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) を作成する方法を説明します。 Experience Leagueからの回答はすべて検証可能で、リンク付きで引用されます。

* **オペレーショナルインサイト：**&#x200B;[ オペレーショナルインサイト ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/questions#objects-questions) メタデータオブジェクト（属性、オーディエンス、データフロー、データセットなど）に関して生成される応答を参照します。 [!UICONTROL AI アシスタント &#x200B;] を使用すると、他の方法では数時間または数日かかる可能性がある作業を、数秒で完了できます。

[AI アシスタントの詳細 ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/landing)

## Experience Cloud製品での AI の可用性

GenAI、AI アシスタント、または Agentic AI を使用するExperience Cloud アプリケーションの概要を次に示します。 Adobe Fireflyとの互換性があることが示されています。

| **製品名** | **ジェネレーティブ AI** | **AI アシスタント** | **Fireflyの互換性** |
|------------------|-------------------------|------------------|---------------------------|
| [Adobe GenStudio for Performance Marketing](#gspm) | はい。<br> マーケティングチームやクリエイティブチームが、パーソナライズされたオンブランドコンテンツを作成するのに役立ちます。 | 該当なし | ○ |
| [Adobe Experience Manager Sites](#aem) | はい。<br> バリエーションを生成 [ で使用でき、入力に基づいてコンテンツのバリエーションを作成できます ](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor?lang=en)。 | 該当なし | ○ |
| [Sites Optimizer](#aem) | はい。<br> Web エクスペリエンスのパフォーマンスと有効性を分析し、向上させるのに役立ちます。 | 該当なし | × |
| [Adobe Experience Manager Assets](#aem) | はい。<br> は、[Content Hub](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview?lang=en) および AI 生成 [ スマートタグ ](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/manage/smart-tags?lang=en#ai-smart-tags) で使用できます。 | 該当なし | ○ |
| [Adobe Journey Optimizer](#journey-optimizer) | 該当なし | はい。<br> 製品に関する知識や運用に関するインサイトに利用できます。 | × |
| | | AJO PrimeおよびUltimateでは、テキストや画像に対してプロアクティブなコンテンツバリエーションの提案を行う [ コンテンツ生成 ](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative?lang=en) を提供しています。 | ○ |
| [[!DNL Adobe Journey Optimizer] B2B edition](#ajo-b2b) | 該当なし | はい。<br> 製品に関する知識の向上に役立ちます。 | × |
| [[!DNL Campaign] Managed Cloud Services](#campaign-cs) | 該当なし | はい。<br> コンテンツアクセラレーターに AI アシスタントを使用して、メール、SMS、プッシュなどのあらゆるチャネルにわたるマーケティング目標に基づいて、パーソナライズされた魅力的で効果的なコンテンツを自動生成します | ○ |
| [[!DNL Customer Journey Analytics]](#cja) | はい。GenAI<br> 次の場所で使用されます。<ul><li> [ インテリジェントキャプション ](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions?lang=en)：最も頻繁に使用されるWorkspaceのビジュアライゼーションに関するインサイト。</li><li>[Content Analytics](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/report/report?lang=en#template): アセットのメタデータを自動的に割り当てます。</li></ul> | はい。<br>AI アシスタントは、次の操作に役立ちます。<ul><li>[ 商品に関する知識 ](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant?lang=en) （Experience League）</li><li>[ 製品サポート担当者 ](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/new-features/customer-support?lang=en) </li><li>[Data Insights Agent](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai)</li></ul> | × |
| [[!DNL Real-Time CDP]](#rtcdp) | 該当なし | はい。<br>Experience Leagueの商品に関する知識。 また、運用に関するインサイト（ベータ版）も提供します。 | × |
| [[!DNL Marketo]](#marketo) | はい。<br>[Dynamic Chatで利用可能 ](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview?lang=en) および [ インタラクティブウェビナー ](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai?lang=en)。 | 該当なし | × |
| [[!DNL Workfront]](#workfront) | はい。アプリ内の情報と提案を <br> します。 [詳細情報](https://experienceleague.adobe.com/ja/docs/workfront/using/basics/ai-assistant/ai-assistant-overview?lang=en) | 該当なし | ○ |

## Experience Cloudでの GenAI の使用例 {#products}

以下の節では、特定のアプリケーションで genAI または AI Assistant を使用する方法について詳しく説明します。 詳細情報へのリンクが提供されています。

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] Managed Cloud Services](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing] は、企業のマーケティングチームが有料メディア、メール、ディスプレイ広告などのチャネルをまたいでオンブランドのキャンペーンコンテンツを作成、アクティブ化、最適化するのを支援するように設計されたジェネレーティブ AI アプリケーションです。

パフォーマンスマーケターは、自然言語プロンプトを使用して、ブランドに準拠したパーソナライズされたアセットを生成できます。 GenStudio for Performance Marketingは、キャンペーンの実行を促進し、ブランドの整合性を損なうことなくコンテンツの制作を拡張し、全体的な ROI を向上させるパフォーマンス分析を提供します。

[詳細情報](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home)

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

[詳細情報](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

### Sites Optimizer {#sites-optimizer}

AEM Sites Optimizerでは、ジェネレーティブ AI を使用して、web エクスペリエンスのパフォーマンスと効果を分析および向上させます。 これらのインサイトは、エンゲージメント、トラフィック獲得、セキュリティ態勢、サイトの正常性などの主要な商談領域にグループ化されます。 各カテゴリでは、訪問者とのやり取りを強化したり、検出性を向上させたり、セキュリティを強化したり、サイトの安定性を維持したりして、サイトを強化する特定の方法に焦点を当てます。 [詳細情報](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/opportunity-types/overview)

### Experience Manager Assets {#aem-assets}

AEM Assetsでは、**Content Hub** および **AI によって生成されたスマートタグ** で生成 AI を使用できます。

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

### コンテンツ生成用 AI アシスタント（AJOPrimeおよびUltimate） {#ajo-prime}

AJO _Prime_ および _Ultimate_ では、[ コンテンツ生成 ](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) をコンテンツ生成に使用して、テキストや画像に対するプロアクティブなコンテンツバリエーションの提案を行うことができます。

この機能は、メール、プッシュ通知、web ページ、コンテンツおよび SMS チャネルで使用できます。 プロンプトベースのテキストと画像を生成できます。 AJO PrimeおよびUltimateでのコンテンツ生成からの出力は除外されます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B editionでは、[!UICONTROL AI アシスタント &#x200B;] を使用して、商品の知識を支援します。

入力例：

* _アカウントジャーニーでメールを送信するにはどうすればよいですか？_

  製品ナレッジ出力はExperience Leagueから取り込まれます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

## [!DNL Campaign] Managed Cloud Services {#campaign-cs}

Campaign Managed Cloud Services では、コンテンツの生成に [!UICONTROL AI アシスタント &#x200B;] を使用します。 この機能を使用すると、ブランドの概要を示すスタイル、レイアウト、トーンなどに最適化されたコンテンツを使用して、マーケティング目標に基づいてパーソナライズされた魅力的で効果的なコンテンツを自動生成できます。 メール、SMS、プッシュなど、様々なチャネルで使用できます。

**メモ：** Campaign Managed Cloud Services のコンテンツ生成からの出力は除外されます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/campaign-web/v8/content/ai-assistant/generative-gs)

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analyticsでは、ジェネレーティブ AI または AI アシスタントを次のように使用できます。

* 製品に関する知識の [AI アシスタント ](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)。
* [ インテリジェントキャプション ](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)：自然言語で最も頻繁に使用されるWorkspaceのビジュアライゼーションに対して重要なインサイトを提供します。
* [Content Analytics](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/report/report#template)：すべてのアセットのメタデータを自動的に割り当てます。

**AI アシスタント**

Experience Leagueの製品に関する知識を確認します。 初めて使用する場合は、Customer Journey Analyticsの概念を素早く理解し、製品や機能のオンボーディングをおこないます。 例：

* _アカウントジャーニーでメールを送信するにはどうすればよいですか？_

経験豊富なユーザーが高度なユースケースを取得したり、タスクを迅速に実行するための戦略を学んだりします。 概念の理解、問題のトラブルシューティング、情報の検索をすばやく行うことができます。

[詳細情報](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

**インテリジェントキャプション**

[!DNL Customer Journey Analytics] で _インテリジェントキャプション_ を使用して、最も頻繁に使用されるWorkspaceのビジュアライゼーションに関する自然言語のインサイトを取得できます。 インテリジェントキャプションは、他のユーザーと共有するためにストーリーとコンテキストを必要とするアナリストに最適です。 ビジネスユーザーは、これを使用して、大まかな留意点をすばやく見つけることができます。

例：

* **入力：** CJAで、サポートされているビジュアライゼーション（折れ線グラフ、面グラフ、棒グラフ、フロー、フォールアウトを含む）を実行し、**[!UICONTROL インテリジェントキャプション]** をクリックします。

* **出力：** コンテキストと重要な留意点を示す、自動生成された自然言語キャプションの表示。 その後、生成されたデータに対して、レビュー、コピー、組織との共有などのアクションを実行できます。 [ 方法を参照 ](https://video.tv.adobe.com/v/3443139/?quality=12&learn=on#_blank&captions=jpn)

[詳細情報](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

**Content Analytics**

Content Analyticsでは、AI と GenAI を使用して、サブジェクト、シーン、前景色などのすべてのアセットメタデータを自動的に割り当てます。 属性は、アセットまたはエクスペリエンスの内容を説明する、AI によって割り当てられたメタデータタグです。

例：前景 `color: red` は、自動的に割り当てられる属性です。 ビジュアライゼーションは、アセットのどの属性がコンバージョンに最も貢献しているかを特定するのに役立ちます。 [詳細情報](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/report/report#template)

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDPでは、[!UICONTROL AI アシスタント &#x200B;] を使用して、Experience Leagueの製品情報を提供します。 また、運用に関するインサイト（ベータ版）も提供します。 [!UICONTROL AI アシスタント &#x200B;] は、AEP サンドボックス内にパーティション化された一元化された運用データを含む、顧客固有の運用インサイトデータストアをクエリします。 システムは、属性、オーディエンス、データフロー、データセット、宛先、スキーマおよびソースからのみメタデータを取り込み、サンドボックス内のデータにはアクセスしません。

例えば、オーディエンスに関するクエリを実行する場合、[!UICONTROL AI アシスタント &#x200B;] は、オーディエンスの名前および他の関連メタデータにアクセスできますが、そのオーディエンス内のプロファイルにはアクセスできません。

[詳細情報](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home)

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

Adobe Dynamic Chatのジェネレーティブ AI を活用した機能により、営業担当者の生産性を最適化し、Web サイトの訪問者の意図に関するインサイトを得て、訪問者の質問に安全な方法で対応できます。 質問、回答および会話の概要を事前承認できます。 Dynamic Chatには、無料版とプレミアム版の両方が含まれています。

[詳細情報](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

## [!DNL Workfront] {#workfront}

[!DNL Workfront] の [!UICONTROL AI アシスタント &#x200B;] は、アプリ内の情報や提案を提供することで、作業を達成するのに役立ちます。 実行できる操作は、次のとおりです。

* 一部のオブジェクトの概要を取得して、オブジェクトの意図や詳細の概要を表示します。
* 質問をしたり、[!UICONTROL AI アシスタント &#x200B;] にExperience Leagueで回答を見つけさせたりします。
* プロンプトに基づいて生成された式を取得します。 また、計算フィールドでの無効なカスタム式のエラーを解決することもできます。
* プロジェクト、タスクおよび問題を見つけます。

([詳細情報](https://experienceleague.adobe.com/ja/docs/workfront/using/basics/ai-assistant/ai-assistant-overview))

## その他のリソース

* [ トラストセンターの責任ある AI リソース ](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**免責事項：** このページの情報は、一般的な情報提供のみを目的としています。 情報が正確で最新の状態を保つように尽力する一方で、ソフトウェアやジェネレーティブ AI の機能は頻繁に変更される可能性があります。 従って、当社は常に情報の完全性、正確性、信頼性を保証するものではありません。 このコンテンツに基づいて決定を下す前に、重要な詳細を確認してください。

