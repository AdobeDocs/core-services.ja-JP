---
description: 管理者は、Analytics Premium へのアップグレード時の要件と推奨事項について学習できます。また、Experience Cloud 管理者としてヘルプ情報を検索できる場所についても学習できます。
keywords: upgrading
seo-description: 管理者は、Analytics Premium へのアップグレード時の要件と推奨事項について学習できます。また、Experience Cloud 管理者としてヘルプ情報を検索できる場所についても学習できます。
seo-title: Analytics Premium および Experience Cloud へのアップグレード
solution: Experience Cloud
title: Analytics Premium および Experience Cloud へのアップグレード
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Analytics Premium および Experience Cloud へのアップグレード

管理者は、Analytics Premium へのアップグレード時の要件と推奨事項について学習できます。また、Experience Cloud 管理者としてヘルプ情報を検索できる場所についても学習できます。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Adobe Analytics Premiumにアップグレードすると、Data Warehouse、Ad Hoc分析、Report Builder、Data Connectorsを含む、Analytics Standardで使用可能なすべての機能や製品を利用できます。 （これらの製品は、ポイントソリューションであるSiteCatalystを使用するお客様に対して別途販売されていました）。

Analytics Premiumでは、次の機能を利用できます。

* 250個のコンバージョン変数(eVar)へのアクセス
* [モバイルアプリ解析](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)
* Data Workbench（ビジュアルデータクエリ、ルールに基づくアトリビューション、クロスチャネル分析）

>[!NOTE]
>
>アップグレード時に移行は必要ありませんが、次の点に注意する必要があります。
>
>* eVars 76～250（SiteCatalyst）および 100～250（Standard）は、管理ツールに表示されますが、デフォルトでは無効になっています。>
>* 貢献度分析は、アドビによってオンにされています。 場所は変更されません（変則性の検出ページで引き続き使用できます）が、すべてのデータポイントの開始分析が自動的に行われます。>


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

Analytics Premium Completeでは、 [Analytics Premiumのすべての機能に加え](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)、次のアップグレードが可能です。

| 製品 | アップグレード |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[貢献度分析](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[顧客属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)（最大 200）</li></ul> |
| Data Workbench | <ul><li>アルゴリズムアトリビューション</li><li>事前ビルドワークスペース</li></ul> |
| Analyticsプラットフォーム | [ライブストリーム](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html) (生データ、ダッシュボード、トリガー) |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

Predictive Intelligenceにアップグレードすると、 [Analytics Premiumに加え](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 、次の機能を利用できます。

| 製品 | アップグレード |
|---|---|
| Reports &amp; Analytics | [貢献度分析](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | 事前に作成されたワークスペース。オーディエンスの資格や予測マーケティングに使用します。 |
| Analyticsプラットフォーム | ライブストリーム(ダッシュボードとトリガー) |

## お客様360 {#section_3B2AC245388248688067DC9A48957AFB}

Customer 360 Analytics Premiumへのアップグレ [ード](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) :

| 製品 | アップグレード |
|--- |--- |
| [顧客属性](../attributes/attributes.md) | 顧客属性（分析およびセグメント共有） |
| Data Workbench | <ul><li>派生顧客属性</li><li>事前にビルドされたワークスペースによるオーディエンスの検出</li></ul> |
| Analyticsプラットフォーム | [顧客属性](../attributes/attributes.md) |

## 高度なアトリビューション {#section_9E4986A8389946CCAA7D003268343296}

高度なアトリビューションでは、[Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) へのアクセス権に加え、Data Workbench のアルゴリズムアトリビューション（契約サーバーコール数の 25％）へのアクセス権が提供されます。

## Data Workbench の要件 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

サポートされるユーザーは、クライアントライセンスを更新して Premium の機能を利用できるようにするための `dwb@adobe.com` 宛ての電子メールでリクエストします。これにより、アルゴリズムアトリビューションなどの機能が有効になります。

TechOpsは、契約内容を確認し、適切な管理インフラストラクチャを決定し、容量を増やしたり減らしたりします。その後、アカウントマネージャやコンサルティングを通じて、お客様と協力し、変更を導入します。

オンプレミスで実行しているソフトウェアは、非アクティブ化する必要があります。 これには、Sensorが含まれます。つまり、Analyticsタグを使用して適切な追跡を行う必要があります。

## Experience Cloud - ユーザーと製品の管理 {#section_6471C54454024301B2E0B687F79F6738}

Analytics Standard と Premium のユーザーは Experience Cloud およびコアサービスを利用できます。ただし、「[はじめに - コアサービスのソリューションを有効にする](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)」に記載されている実装の最新化に従っていることが前提です（このプロセスにより、実装を最新化できます。また、Experience Cloud の管理者になることもできます）。

Experience Cloud に加入したら、[!DNL experiencecloud.adobe.com] から Experience Cloud にログインして、コアサービス（顧客属性、オーディエンスおよびモバイルアプリ分析を含む）の利用を開始することができます。

### ユーザーとグループの管理

ユーザー管理は、 [Adobe Admin Console](https://helpx.adobe.com/enterprise/help/aedash.html) （製品リンク）で行います。

Adobe Admin Consoleで作成したグループとソリューショングループ（Adobe Analyticsなど）の1対1のマップを設定できます。 その後、マッピングされた管理コンソールグループに追加された新しいユーザーには、Analyticsソリューションアカウントが自動的に作成され、ユーザーのAdobe IDにリンクされます。 （既存のユーザーは、Experience Cloudのログインを通じてソリューションにアクセスするには、ソリューションアカウントの資格情報を手動でリンクする必要があります）。

>[!NOTE]
>
>いくつかのソリューショングループを 1 つの Admin Console グループにマッピングできます。ただし、1:1のマッピングを推奨します。 事前にグループをマッピングすると、CSVをアップロードして、複数のユーザーを招待、作成、権限および追加できます。
