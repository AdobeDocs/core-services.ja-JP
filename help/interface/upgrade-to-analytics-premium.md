---
description: Analytics Premium にアップグレードする際の要件と予想される処理について説明します。
keywords: Adobe Analytics Premium へのアップグレード
solution: Experience Cloud
title: 'Analytics Premium および Experience Cloud へのアップグレード '
topic: 管理
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
feature: Admin Console
role: Administrator
level: Experienced
exl-id: 746d396d-9629-42db-8c55-07d2d24e4611
source-git-commit: 145040facf70c6bde5c6c3fae9c7ed7f520c188d
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 72%

---

# Analytics Premium および Experience Cloud へのアップグレード

管理者は、Analytics Premium へのアップグレード時の要件と推奨事項について学習できます。また、Experience Cloud 管理者としてヘルプ情報を検索できる場所についても学習できます。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Adobe Analytics Premium にアップグレードすると、Data Warehouse、Ad Hoc Analysis、Report Builder および Data Connectors を含む、Analytics Standard で使用できるすべての機能と製品を入手できます

Analytics Premium では、次のことができます。

* 250 個のコンバージョン変数（eVars）へのアクセス
* [モバイルアプリ分析](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=ja)
* Data Workbench（ビジュアルデータクエリ、ルールに基づくアトリビューション、クロスチャネル分析）

>[!NOTE]
>
>アップグレードの際に移行は必要ありませんが、以下の注意事項があります。
>
>* eVar 76 ～ 250および100 ～ 250（標準）は、管理ツールに表示されますが、有効になっていません。
>* 貢献度分析は、オンになっています。場所は変更されません（まだ異常値検出ページで使用できます）が、すべてのデータポイントの分析が自動的に開始されます。


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

Analytics Premium Complete では、[Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) のすべての機能を入手できることに加え、次のアップグレードがおこなわれます。

| 製品 | アップグレード |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[貢献度分析](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en)</li><li>[顧客属性](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)（最大 200）</li></ul> |
| Data Workbench | <ul><li>アルゴリズムアトリビューション</li><li>事前定義済みワークスペース</li></ul> |
| Analytics Platform | [Live Stream](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/index.md)（生データ、ダッシュボード、トリガー） |

{style=&quot;table-layout:auto&quot;}

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

Predictive Intelligence へのアップグレードにより、[Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) に加え、以下を利用できます。

| 製品 | アップグレード |
|---|---|
| Reports &amp; Analytics | [貢献度分析](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en) |
| Data Workbench | オーディエンスの資格と予測マーケティングのためのワークスペース |
| Analytics Platform | Live Stream（ダッシュボードとトリガー） |

{style=&quot;table-layout:auto&quot;}

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

Customer 360 へのアップグレードにより、[Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) に加え、以下を利用できます。

| 製品 | アップグレード |
|--- |--- |
| [顧客属性](attributes.md) | 顧客属性（分析およびセグメント共有） |
| Data Workbench | <ul><li>派生顧客属性</li><li>オーディエンス検出用の事前定義済みワークスペース</li></ul> |
| Analytics Platform | [顧客属性](attributes.md) |

{style=&quot;table-layout:auto&quot;}

## 高度なアトリビューション {#section_9E4986A8389946CCAA7D003268343296}

高度なアトリビューションでは、[Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) へのアクセス権に加え、Data Workbench のアルゴリズムアトリビューション（契約サーバーコール数の 25％）へのアクセス権が提供されます。

## Data Workbench の要件 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

サポートされるユーザーは、クライアントライセンスを更新して Premium の機能を利用できるようにするための `dwb@adobe.com` 宛ての電子メールでリクエストします。この更新により、アルゴリズムアトリビューションなどの機能が有効になりました。

TechOpsは、契約内容を確認し、適切な管理インフラストラクチャを決定し、容量を増減し、アカウントマネージャーやコンサルティングを通じて調整し、変更を導入します。

オンプレミスで実行しているソフトウェアは、非アクティブ化する必要があります。このソフトウェアには、[!DNL Analytics]タグを介して適切な追跡を行う必要があるSensorが含まれています。

## Experience Cloud - ユーザーと製品の管理 {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloudとコアサービスは、[はじめに — コアサービスのソリューションを有効にする](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)に記載されている実装の最新化に従っている場合、Analytics StandardおよびPremiumのユーザーが利用できます。 （このプロセスにより、実装を最新化できます。また、Experience Cloud の管理者になることもできます）。

Experience Cloud に加入したら、[!DNL experience.adobe.com] から Experience Cloud にログインして、コアサービス（顧客属性、Audiences およびモバイルアプリ分析を含む）の利用を開始することができます。

### ユーザーとグループの管理

ユーザーの管理は [Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)（製品リンク）でおこないます。

Adobe Admin Console で作成したグループとソリューショングループ（Adobe Analytics など）の 1 対 1 でのマッピングを設定できます。その後、マッピングされたAdmin Consoleグループに追加された新しいユーザーには、Analyticsソリューションアカウントが自動的に作成され、ユーザーのAdobe IDにリンクされます。 （既存のユーザーは、ソリューションのアカウント資格情報を手動でリンクして、Experience Cloud ログインを介してソリューションにアクセスする必要があります）。

>[!NOTE]
>
>いくつかのソリューショングループを 1 つの Admin Console グループにマッピングできます。ただし、1 対 1 のマッピングをお勧めします。事前にグループをマッピングしておくと、CSV をアップロードすることで、複数のユーザーを招待、作成、承認および追加できます。
