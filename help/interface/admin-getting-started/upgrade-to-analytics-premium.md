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
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Analytics Premium および Experience Cloud へのアップグレード

管理者は、Analytics Premium へのアップグレード時の要件と推奨事項について学習できます。また、Experience Cloud 管理者としてヘルプ情報を検索できる場所についても学習できます。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Adobe Analytics Premiumにアップグレードすると、Data Warehouse、Ad Hoc分析、Report Builder、Data Connectorsを含む、Analytics Standardで使用可能なすべての機能や製品を利用できます。 （これらの製品は、ポイントソリューションであるSiteCatalystを使用するお客様に個別に販売されていました）。

Analytics Premiumでは、次のことができます。

* 250個のコンバージョン変数(eVar)へのアクセス
* [モバイルアプリ解析](https://docs.adobe.com/content/help/ja-JP/mobile-services/using/home.html)
* Data Workbench（ビジュアルデータクエリ、ルールに基づくアトリビューション、クロスチャネル分析）

>[!NOTE]
>
>アップグレード時に移行は必要ありませんが、次の点に注意する必要があります。
>
>* eVars 76～250（SiteCatalyst）および 100～250（Standard）は、管理ツールに表示されますが、デフォルトでは無効になっています。>
>* 貢献度分析は、アドビがオンにしています。 場所は変更されません（変則性の検出ページでは引き続き使用できます）が、すべてのデータポイントの分析を開始が自動的に行うようになります。>


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

Analytics Premium Completeでは、 [Analytics Premiumのすべての機能を入手でき](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)、さらに次のアップグレードが行われます。

| 製品 | アップグレード |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[貢献度分析](https://docs.adobe.com/content/help/ja-JP/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[顧客属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)（最大 200）</li></ul> |
| Data Workbench | <ul><li>アルゴリズムアトリビューション</li><li>事前ビルドワークスペース</li></ul> |
| Analytics Platform | [Live Stream](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html) (生データ、ダッシュボード、トリガー) |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

Predictive Intelligenceにアップグレードすると、 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) に加え、次の機能を利用できます。

| 製品 | アップグレード |
|---|---|
| Reports &amp; Analytics | [貢献度分析](https://docs.adobe.com/content/help/ja-JP/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | オーディエンスの資格と予測マーケティングのための事前に作成されたワークスペース。 |
| Analytics Platform | Live Stream(ダッシュボードおよびトリガー) |

## 顧客360 {#section_3B2AC245388248688067DC9A48957AFB}

Customer 360オファー向け [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) へのアップグレードに加え、以下の機能が追加されました。

| 製品 | アップグレード |
|--- |--- |
| [顧客属性](../attributes/attributes.md) | 顧客属性（分析およびセグメント共有） |
| Data Workbench | <ul><li>派生した顧客属性</li><li>オーディエンス検出用の事前にビルドされたワークスペース</li></ul> |
| Analytics Platform | [顧客属性](../attributes/attributes.md) |

## 高度なアトリビューション {#section_9E4986A8389946CCAA7D003268343296}

高度なアトリビューションでは、[Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) へのアクセス権に加え、Data Workbench のアルゴリズムアトリビューション（契約サーバーコール数の 25％）へのアクセス権が提供されます。

## Data Workbench の要件 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

サポートされるユーザーは、クライアントライセンスを更新して Premium の機能を利用できるようにするための `dwb@adobe.com` 宛ての電子メールでリクエストします。これにより、アルゴリズムアトリビューションなどの機能が有効になります。

TechOpsは、契約内容を確認し、適切な管理インフラストラクチャ、容量の増減を決定し、アカウントマネージャやコンサルティングを通じて、お客様と協力して変更を導入します。

オンプレミスで実行しているソフトウェアは、非アクティブ化する必要があります。 これには、Sensorが含まれます。つまり、Analyticsタグを使用して適切なトラッキングを行う必要があります。

## Experience Cloud - ユーザーと製品の管理 {#section_6471C54454024301B2E0B687F79F6738}

Analytics Standard と Premium のユーザーは Experience Cloud およびコアサービスを利用できます。ただし、「[はじめに - コアサービスのソリューションを有効にする](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)」に記載されている実装の最新化に従っていることが前提です（このプロセスにより、実装を最新化できます。また、Experience Cloud の管理者になることもできます）。

After you join the Experience Cloud, you can log in via the Experience Cloud at [!DNL experiencecloud.adobe.com] and begin using core services (including Customer Attributes, Audiences, and Mobile app analytics).

### ユーザーとグループの管理

ユーザー管理は、 [Adobe管理コンソール](https://helpx.adobe.com/enterprise/help/aedash.html) （製品リンク）で行います。

Adobe管理コンソールで作成したグループとソリューショングループ（Adobe Analyticsなど）の1対1のマッピングを設定できます。 その後、マッピングされた管理コンソールグループに追加された新しいユーザーには、Analyticsソリューションアカウントが自動的に作成され、ユーザーのAdobe IDにリンクされます。 （既存のユーザーは、ソリューションアカウント資格情報を手動でリンクして、Experience Cloudログインを介してソリューションにアクセスする必要があります）。

>[!NOTE]
>
>いくつかのソリューショングループを 1 つの Admin Console グループにマッピングできます。ただし、1対1のマッピングをお勧めします。 事前にグループをマッピングしておくと、CSVをアップロードして、複数のユーザーを招待、作成、権限および追加できます。
