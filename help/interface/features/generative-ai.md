---
title: Experience Cloud アプリケーションのジェネレーティブ AI
description: Experience Cloud アプリケーションの AI を活用した機能を活用できる場所を大まかに見てみましょう。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Artificial Intelligence
role: Admin, User
level: Beginner, Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 4ce6b7ae75b8fdad478384fbd6d3400c4b852bf3
workflow-type: tm+mt
source-wordcount: '2430'
ht-degree: 9%

---

# Experience Cloudのジェネレーティブ AI

Experience Cloudのジェネレーティブ AI （genAI）は、クリエイティブおよび認知機能のタスクを自動化し、生産性を向上させるのに役立ちます。 このページは、Experience Cloud アプリケーションが genAI および AI アシスタントをサポートする場所を理解するのに役立ち、これらの機能の詳細を学ぶためのリンクを提供します。

>[!IMPORTANT]
>
>Experience Cloudのジェネレーティブ AI 機能を使用する前に、[Adobe Experience Cloud ジェネレーティブ AI ユーザーガイドライン &#x200B;](https://www.adobe.com/jp/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) を理解し、従う必要があります。

**genAI とは**

ジェネレーティブ AI は、オリジナルのコンテンツを作成できる AI の一種です。 例えば、ユーザーのプロンプトや要求に応じて、テキスト、画像、ビデオ、オーディオまたはソフトウェアコードを作成できます。

* **作成：** トレーニングおよび入力プロンプトに基づいて、コンテンツ（テキスト、画像、音楽、ビデオ）をゼロから生成する機能。 この機能は、生成 AI の _生成_ 側面です。

* **応答を生成：** AI は、通常、使用可能なデータとナレッジリポジトリを利用して、プロンプトに対する回答や反応を提供します。

[!BADGE 詳細情報]{type=Informative url="https://business.adobe.com/ai/adobe-genai.html" tooltip="Adobeの GenAI"}

**[!UICONTROL AI アシスタント &#x200B;] とは**

[!UICONTROL AI アシスタント &#x200B;] は、多くのExperience Cloud アプリケーションでサポートされている対話型の genAI ツールです。 これを使用すると、使用しているアプリケーションに応じて _製品の知識_ および _運用に関するインサイト_ を素早く得ることができます。

* **商品知識：** 商品知識とは、Experience Leagueに関するExperience Cloud商品ドキュメントに基づく概念とトピックを指します。 例えば、[&#x200B; 目的ベースのプロンプト &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) を使用して、Experience Platformについて素早く知ることができます。 Experience Leagueからの回答はすべて検証可能で、リンク付きで引用されます。

* **オペレーショナルインサイト：** 例えば、Experience Platformの [&#x200B; オペレーショナルインサイト &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/questions#objects-questions) は、メタデータオブジェクト（属性、オーディエンス、データフロー、データセットなど）に関して生成された応答を参照します。 [!UICONTROL AI アシスタント &#x200B;] を使用すると、他の方法では数時間または数日かかる可能性がある作業を、数秒で完了できます。

>[!NOTE]
>
>多くのExperience Cloud アプリケーションでは、（以下に説明するように）機能名として _AI アシスタント_ を使用します。 ただし、この機能は、使用している特定のアプリケーションに関する情報のみを取り込みます。 例えば、AEMの AI アシスタントは、AEMに関連する関連性の高い有用な情報を提供します。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/landing" tooltip="AI アシスタントに移動"}

[!BADGE &#x200B; プライバシー、セキュリティ、ガバナンス &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/privacy" tooltip="Adobeの GenAI"}

## サポートされている genAI 機能は何ですか？ {#ai-roundup}

生成 AI 機能と AI アシスタントを使用する [!DNL Experience Cloud] アプリケーションの概要を次に示します。 ジェネレーティブ AI 機能には [0&rbrace;Adobe Firefly&rbrace; との互換性が示されています。](https://business.adobe.com/products/firefly-business/firefly-ai-approach.html)

### 生成 AI

<!-- | Product | Key AI features | Firefly Compatibility |
|----------------|-----------------|---------|
| GenStudio for Performance Marketing | Create personalized, on-brand content | Yes |
| Adobe Experience Manager (AEM CS) | Generate Variations, Sites Optimizer GenAI, Content Hub, Smart Tags | Yes |
| Adobe Experience Manager 6.5 | AI Assistant support | Yes |
| Adobe Experience Manager 6.5 LTS | AI Assistant support | Yes |
| Adobe Experience Platform | AI Assistant for product knowledge and operational insights | No |
| Adobe Journey Optimizer | AI Assistant, content generation (Prime/Ultimate) | Yes |
| Adobe Journey Optimizer B2B Edition | AI Assistant for product knowledge | No |
| Campaign Managed Cloud Services | Content Accelerator for cross-channel personalization | Yes |
| Customer Journey Analytics | AI Assistant, Intelligent Captions, Content Analytics | No |
| Real-Time CDP | AI Assistant for product knowledge and operational insights | No |
| Marketo | Email Designer, Dynamic Chat, Interactive Webinars | Yes |
| Workfront | AI Assistant for work management and recommendations | Yes | -->

| **製品名** | **GenAI の主な機能** | **Fireflyの互換性** |
|------------------|-------------------------|-------------------|
| [Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home) | genAI を使用して、パーソナライズされたオンブランドコンテンツを作成します。 | ○ |
| [Adobe Experience Manager as a Cloud Service（AEM CS） &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/overview) | GenAI は、次の場所で利用できます。<ul><li>[2&rbrace;AEM Sites](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor){ バリエーションを生成 **&#x200B;**</li><li>[2}Sites Optimizer](https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/opportunity-types/overview) の &lbrace;GenAI **&#x200B;**</li><li>[Content Hub](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview?lang=en) および [&#x200B; スマートタグ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/manage/smart-tags?lang=en#ai-smart-tags) （**AEM Assets**）</li></ul> 以下の AI アシスタント： <ul><li>Experience Hubの概要ページ<li>Edge 配信サービス</li><li>サイト</li><li>アセット</li><li>フォーム</li><li>Dynamic Media</li><li>Cloud Manager</li></ul> | ○ |
| [Adobe Experience Manager 6.5](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/ai-assistant/ai-assistant-in-aem) | 以下の AI アシスタント： <ul><li>Experience Hubの概要ページ<li>Edge 配信サービス</li><li>サイト</li><li>アセット</li><li>フォーム</li><li>Dynamic Media</li><li>Cloud Manager</li></ul> | ○ |
| [Adobe Experience Manager 6.5 LTS](https://experienceleague.adobe.com/ja/docs/experience-manager-65-lts/content/ai-assistant/ai-assistant-in-aem) | 以下の AI アシスタント： <ul><li>Experience Hubの概要ページ<li>Edge 配信サービス</li><li>サイト</li><li>アセット</li><li>フォーム</li><li>Dynamic Media</li><li>Cloud Manager</li></ul> | ○ |
| [Adobe Experience Platform](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/landing) | 製品に関する知識と運用に関するインサイトのための AI アシスタント。 | × |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/ai-assistant) | 製品に関する知識と運用に関するインサイトのための AI アシスタント。 | × |
| | _AJO Prime_ および _Ultimate_ では、テキストおよび画像に対してプロアクティブなコンテンツバリエーションの提案を提供する [&#x200B; コンテンツ生成 &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative?lang=en) を提供しています。 | ○ |
| [Adobe Journey OptimizerB2B edition](https://experienceleague.adobe.com/ja/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview) | 製品の知識のための AI アシスタント。 | × |
| [[!DNL Campaign] Managed Cloud Services](https://experienceleague.adobe.com/ja/docs/campaign-web/v8/content/ai-assistant/generative-gs) | E メール、SMS、プッシュなどのあらゆるチャネルにわたるマーケティング目標に基づいて、パーソナライズされた魅力的で効果的なコンテンツを自動生成するコンテンツアクセラレーター用 AI アシスタント。 | ○ |
| **[!DNL Customer Journey Analytics]** | GenAI は以下で使用されます。<ul><li> [&#x200B; インテリジェントキャプション &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions?lang=en)：最も頻繁に使用されるWorkspaceのビジュアライゼーションに関するインサイト。</li><li>[Content Analytics](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/report/report?lang=en#template): アセットのメタデータを自動的に割り当てます。</li></ul> 以下の AI アシスタント：<ul><li>[&#x200B; 製品に関する知識 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant?lang=en) </li><li>[&#x200B; 製品サポート担当者 &#x200B;](agentic-ai.md) </li><li>[Data Insights Agent](agentic-ai.md)</li></ul> | × |
| [Real-Time CDP](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home) | Experience Leagueの製品に関するナレッジの AI アシスタント。 また、運用に関するインサイトも提供します。 | × |
| **[!DNL Marketo]** | GenAI は、電子メールDesigner（Fireflyを使用）、[Dynamic Chat](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview?lang=en)、（インタラクティブウェビナー [&#x200B; で利用 &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai?lang=en) きます。 Marketo Engage用 <br> AI アシスタント [&#x200B; メールDesigner](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-designer/ai-assistant) | ○ |
| [Workfront](https://experienceleague.adobe.com/ja/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) | アプリ内の情報と提案のための AI アシスタント。 | ○ |

**メモ：**&#x200B;[!DNL Experience Platform Agents] については、[Experience Cloudの AI エージェント &#x200B;](agentic-ai.md) を参照してください。

## Experience Cloudでジェネレーティブ AI を使用するにはどうすればよいですか？ {#products}

以下の節では、特定のアプリケーションで genAI または AI Assistant を使用する方法について詳しく説明します。 詳細情報へのリンクが提供されています。

### GenStudio for Performance Marketing {#gspm}

+++詳細

[!DNL GenStudio for Performance Marketing] は、企業のマーケティングチームが有料メディア、メール、ディスプレイ広告などのチャネルをまたいでオンブランドのキャンペーンコンテンツを作成、アクティブ化、最適化するのを支援するように設計されたジェネレーティブ AI アプリケーションです。

パフォーマンスマーケターは、自然言語プロンプトを使用して、ブランドに準拠したパーソナライズされたアセットを生成できます。 GenStudio for Performance Marketingは、キャンペーンの実行を促進し、ブランドの整合性を損なうことなくコンテンツの制作を拡張し、全体的な ROI を向上させるパフォーマンス分析を提供します。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home" tooltip="GenStudio for Performance Marketingに移動"}

+++

### [!DNL Experience Manager] {#aem}

+++詳細

次の節では、AEM アプリケーションのジェネレーティブ AI について簡単に説明します。

#### AEM as a Cloud Serviceのジェネレーティブ AI

Adobe Experience Manager（AEM）as a Cloud ServiceのAdobe生成 AI を使用すると、編集インターフェイス内でコピーと画像の生成の両方を行い、高いパフォーマンスのエクスペリエンスを作成できます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/generative-ai/generative-ai-in-aem" tooltip="AEM CS の GenAI に移動"}

#### AEM CS の AI アシスタント

[!DNL Experience Manager as a Cloud Service] の AI アシスタントを使用すると、AEM製品に関連する質問に即座に回答したり（すべてのユーザーが利用可能）、サポートチケットを自動的に作成したり（サポート管理者が利用可能）できます。

AI アシスタントは、次の場所でAEM as a Cloud Serviceをサポートします。

* Experience Hubの概要ページ
* Edge 配信サービス
* サイト
* アセット
* フォーム
* Dynamic Media
* Cloud Manager

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-assistant/ai-assistant-in-aem" tooltip="AEMの AI アシスタントに移動"}

#### Experience Manager Sites

AEM Sitesでは、「バリエーションを生成 _[!UICONTROL を使用でき]_ す。 この機能は、ジェネレーティブな人工知能を使用して、入力プロンプトに基づくコンテンツのバリエーションを作成します。 プロンプトは、Adobeから提供されるか、ユーザーが作成および管理します。

バリエーションを作成した後、Web サイトでコンテンツを使用し、Edge Delivery Servicesの [&#x200B; 実験 &#x200B;](https://www.aem.live/docs/experimentation) 機能を使用して、その成功を測定できます。 また、Fireflyの生成 AI 機能を使用して、Adobe Expressで画像を生成することもできます。

**入力と出力の例**

入力フィールドは次のとおりです。

* 生成するバリエーションの数
* オーディエンス Source
* Audience Target
* 追加のコンテキスト
* 顧客主導のプロンプト

出力は、生成されたコンテンツや市場コピーです。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor" tooltip="Experience Leagueでバリエーションを生成に移動"}

#### Sites Optimizer {#sites-optimizer}

AEM Sites Optimizerでは、ジェネレーティブ AI を使用して、web エクスペリエンスのパフォーマンスと効果を分析および向上させます。 これらのインサイトは、エンゲージメント、トラフィック獲得、セキュリティ態勢、サイトの正常性などの主要な商談領域にグループ化されます。 各カテゴリでは、訪問者とのやり取りを強化したり、検出性を向上させたり、セキュリティを強化したり、サイトの安定性を維持したりして、サイトを強化する特定の方法に焦点を当てます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-manager-sites-optimizer/content/opportunity-types/overview" tooltip="Experience LeagueのSites Optimizerに移動"}

#### Experience Manager Assets {#aem-assets}

AEM Assetsでは、**Content Hub** および **AI によって生成されたスマートタグ** で生成 AI を使用できます。

**Content Hub**

[!UICONTROL Content Hub] は、組織やビジネスパートナーがブランド上のコンテンツにアクセスすることを民主化するための [!DNL Experience Manager Assets as a Cloud Service] の一部として利用できます。 大規模なアクティベーション用のアセットの配布と、マーケティングの俊敏性を向上させるためのオンブランドコンテンツバリアントの作成に重点を置いています。

Content Hubでは、Adobe Expressを使用してコンテンツを作成できます（Adobe Expressの使用権限がある場合）。 シンプルなツールで既存のコンテンツを編集し、テンプレートやブランド要素を使用してオンブランドのバリエーションを作成し、[!DNL Adobe Firefly] から最新の GenAI 機能を使用してコンテンツを作成できます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview" tooltip="Experience LeagueのContent Hubに移動"}

**スマートタグ**

AI では、手動入力に依存するのではなく、デジタルアセットに説明的なタグを自動的に割り当てることができます。 これらの AI で生成されるタグは、メタデータの品質を向上させ、アセットの検索、分類およびレコメンデーションを容易にします。

例えば、アセットが画像の場合、AI はオブジェクト、シーン、感情、さらにはブランドロゴを識別できます。 _sunset_、_beach_、_vacation_、_smiling_ などの関連するタグを生成できます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/manage/smart-tags#ai-smart-tags" tooltip="スマートタグについて学ぶ"}

+++

### Experience Platform

+++詳細

Adobe Experience Platformの AI アシスタントは、Adobe アプリケーションでの作業を高速化するのに役立つチャットツールです。 これを使用して、次のことができます。

* 製品の仕組みを学ぶ
* 問題解決の手助けを得る
* データおよび設定に関する情報やインサイトを検索します

AI アシスタントは、Experience Platform、Real-Time Customer Data Platform、Adobe Journey Optimizer、Customer Journey Analyticsで使用できます。 （後述）

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/landing" tooltip="Adobe Experience Platformの AI アシスタント"}

+++

### Adobe [!DNL Journey Optimizer] {#journey-optimizer}

+++詳細

[!DNL Journey Optimizer] （AJO）では、[AI アシスタント &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/ai-assistant) を使用して _製品に関する知識_ および _運用に関するインサイト_ （ベータ版）を取得できます。

#### AJOでの AI アシスタントの使用例

製品知識の入力例を次に示します。

* _1 つのJourney Optimizer サンドボックスに含めることができるライブアクティビティの数_

  出力は、Experience Leagueおよびその他のAdobe データストアから生成されます。

次に、運用インサイトに対する入力の例を示します。

* _過去 7 日間に作成されたジャーニーの数_

  出力用に、AI アシスタントが顧客固有のデータ ストアに対してクエリを実行します。 データストアには、[!UICONTROL ジャーニー] に関する一元化された運用データが含まれています。 この機能は顧客に依存せず、ビジネスオブジェクトからのみメタデータを取り込みます。 サンドボックス内のデータにはアクセスしません。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/ai-assistant" tooltip="AJOの AI アシスタントについて説明します"}

#### コンテンツ生成用 AI アシスタント（AJOPrimeおよびUltimate） {#ajo-prime}

AJO _Prime_ および _Ultimate_ では、[&#x200B; コンテンツ生成 &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) をコンテンツ生成に使用して、テキストや画像に対するプロアクティブなコンテンツバリエーションの提案を行うことができます。

この機能は、メール、プッシュ通知、web ページ、コンテンツおよび SMS チャネルで使用できます。 プロンプトベースのテキストと画像を生成できます。 AJO PrimeおよびUltimateでのコンテンツ生成からの出力は除外されます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative" tooltip="AJOの AI アシスタントについて説明します"}

+++

### [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

+++詳細

Journey Optimizer B2B editionでは、[!UICONTROL AI アシスタント &#x200B;] を使用して、商品の知識を支援します。

入力例：

* _アカウントジャーニーでメールを送信するにはどうすればよいですか？_

  製品ナレッジ出力はExperience Leagueから取り込まれます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview" tooltip="AJOの AI アシスタントについて説明します"}

+++

### [!DNL Customer Journey Analytics] {#cja}

+++詳細

Customer Journey Analyticsでは、ジェネレーティブ AI または AI アシスタントを次のように使用できます。

* 製品に関する知識の [AI アシスタント &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)。
* [&#x200B; インテリジェントキャプション &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)：自然言語で最も頻繁に使用されるWorkspaceのビジュアライゼーションに対して重要なインサイトを提供します。
* [Content Analytics](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/report/report#template)：すべてのアセットのメタデータを自動的に割り当てます。

**AI アシスタント**

Experience Leagueの製品に関する知識を確認します。 初めて使用する場合は、Customer Journey Analyticsの概念を素早く理解し、製品や機能のオンボーディングをおこないます。 例：

* _アカウントジャーニーでメールを送信するにはどうすればよいですか？_

経験豊富なユーザーが高度なユースケースを取得したり、タスクを迅速に実行するための戦略を学んだりします。 概念の理解、問題のトラブルシューティング、情報の検索をすばやく行うことができます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant" tooltip="CJAの AI アシスタントについて説明します"}

**インテリジェントキャプション**

_で_ インテリジェントキャプション [!DNL Customer Journey Analytics] を使用して、最も頻繁に使用されるWorkspaceのビジュアライゼーションに関する自然言語のインサイトを取得できます。 インテリジェントキャプションは、他のユーザーと共有するためにストーリーとコンテキストを必要とするアナリストに最適です。 ビジネスユーザーは、これを使用して、大まかな留意点をすばやく見つけることができます。

例：

* **入力：** CJAで、サポートされているビジュアライゼーション（折れ線グラフ、面グラフ、棒グラフ、フロー、フォールアウトを含む）を実行し、**[!UICONTROL インテリジェントキャプション]** をクリックします。

* **出力：** コンテキストと重要な留意点を示す、自動生成された自然言語キャプションの表示。 その後、生成されたデータに対して、レビュー、コピー、組織との共有などのアクションを実行できます。 [&#x200B; 方法を参照 &#x200B;](https://video.tv.adobe.com/v/3443139/?quality=12&learn=on#_blank&captions=jpn)

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions" tooltip="インテリジェントキャプションについて"}

**Content Analytics**

Content Analyticsでは、AI と GenAI を使用して、サブジェクト、シーン、前景色などのすべてのアセットメタデータを自動的に割り当てます。 属性は、アセットまたはエクスペリエンスの内容を説明する、AI によって割り当てられたメタデータタグです。

例：前景 `color: red` は、自動的に割り当てられる属性です。 ビジュアライゼーションは、アセットのどの属性がコンバージョンに最も貢献しているかを特定するのに役立ちます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/report/report#template" tooltip="Content Analyticsについて"}

+++

### [!DNL Real-Time CDP] {#rtcdp}

+++詳細

Real-Time CDPでは、[!UICONTROL AI アシスタント &#x200B;] を使用して、Experience Leagueの製品情報を提供します。 また、運用に関するインサイト（ベータ版）も提供します。 [!UICONTROL AI アシスタント &#x200B;] は、AEP サンドボックス内にパーティション化された一元化された運用データを含む、顧客固有の運用インサイトデータストアをクエリします。 システムは、属性、オーディエンス、データフロー、データセット、宛先、スキーマおよびソースからのみメタデータを取り込み、サンドボックス内のデータにはアクセスしません。

例えば、オーディエンスに関するクエリを実行する場合、[!UICONTROL AI アシスタント &#x200B;] は、オーディエンスの名前および他の関連メタデータにアクセスできますが、そのオーディエンス内のプロファイルにはアクセスできません。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/home" tooltip="Real-Time CDPについて"}

+++

### [!DNL Campaign] Managed Cloud Services {#campaign-cs}

+++詳細

Campaign Managed Cloud Services では、コンテンツの生成に [!UICONTROL AI アシスタント &#x200B;] を使用します。 この機能を使用すると、ブランドの概要を示すスタイル、レイアウト、トーンなどに最適化されたコンテンツを使用して、マーケティング目標に基づいてパーソナライズされた魅力的で効果的なコンテンツを自動生成できます。 メール、SMS、プッシュなど、様々なチャネルで使用できます。

**メモ：** Campaign Managed Cloud Services のコンテンツ生成からの出力は除外されます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/campaign-web/v8/content/ai-assistant/generative-gs" tooltip="AJOの AI アシスタントについて説明します"}

+++

### [!DNL Marketo] {#marketo}

+++詳細

Marketoでは、インタラクティブ Web セミナーやDynamic Chatでジェネレーティブ AI を利用できます。 AI アシスタントは、メールDesignerで利用できます。

**インタラクティブウェビナー**

録画したウェビナーのチャプターと概要を自動的に生成し、オーディエンスがアクセスしやすく、簡単に移動できるようにします。 次のような機能があります。

* チャプターの自動生成
* AI 生成テキストの概要
* 編集可能なコンテンツ – 生成されたチャプターと概要を変更
* 簡単な統合 – 選択した web ページエディターにHTML コードをコピーして、ランディングページに章や概要を追加できます

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai" tooltip="インタラクティブウェビナーについて"}

**Dynamic Chat**

Adobe Dynamic Chatのジェネレーティブ AI を活用した機能により、営業担当者の生産性を最適化し、Web サイトの訪問者の意図に関するインサイトを得て、訪問者の質問に安全な方法で対応できます。 質問、回答および会話の概要を事前承認できます。 Dynamic Chatには、無料版とプレミアム版の両方が含まれています。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview" tooltip="Dynamic Chatについて"}

**E メールデザイナー**

Marketo Engageの [!UICONTROL AI アシスタント &#x200B;][!UICONTROL &#x200B; メールDesigner] を使用すると、現代的でパフォーマンスの高い直感的なメールを作成できます。 これを実現するには、アドビの生成 AI テクノロジーやプロンプトライブラリおよび特定のペルソナ／購入グループ、マーケティングジャーニーステージ、コミュニケーション戦略、トーンなどに適したコンテンツの作成を支援する画像生成用の Firefly を使用します。また、特定のブランドアセットを利用してコンテンツを作成することもできます。

[!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-designer/ai-assistant" tooltip="Dynamic Chatについて"}

**GenStudio for Performance Marketing**

MarketoとGenStudio for Performance Marketingの統合

+++

### [!DNL Workfront] {#workfront}

+++詳細

[!UICONTROL &#x200B; の &#x200B;]AI アシスタント [!DNL Workfront] は、アプリ内の情報や提案を提供することで、作業を達成するのに役立ちます。 実行できる操作は、次のとおりです。

* 一部のオブジェクトの概要を取得して、オブジェクトの意図や詳細の概要を表示します。
* 質問をしたり、[!UICONTROL AI アシスタント &#x200B;] にExperience Leagueで回答を見つけさせたりします。
* プロンプトに基づいて生成された式を取得します。 また、計算フィールドでの無効なカスタム式のエラーを解決することもできます。
* プロジェクト、タスクおよび問題を見つけます。

([!BADGE 詳細情報]{type=Informative url="https://experienceleague.adobe.com/ja/docs/workfront/using/basics/ai-assistant/ai-assistant-overview" tooltip="Workfrontの AI アシスタントについて説明します"})

+++

## その他のリソース

+++詳細

* [&#x200B; トラストセンターの責任ある AI リソース &#x200B;](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

+++

**免責事項：** このページの情報は、一般的な情報提供のみを目的としています。 情報が正確で最新の状態を保つように尽力する一方で、ソフトウェアやジェネレーティブ AI の機能は頻繁に変更される可能性があります。 従って、当社は常に情報の完全性、正確性、信頼性を保証するものではありません。 このコンテンツに基づいて決定を下す前に、重要な詳細を確認してください。

