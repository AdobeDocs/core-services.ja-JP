---
description: Experience Cloudの新機能と更新について
solution: Experience Cloud
title: Experience Cloud の新機能
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 98%

---


# Experience Cloud の新機能

Experience Cloud の新機能と更新の概要を示します。

## 2018 年 8 月 {#section_7388CDAB723B49809AABEFEE85CF6378}

2018 年 8 月の修正点と機能強化です。

* Creative Cloud と Experience Cloud のアセットのコメントの同期を強化しました。（CORE-15971）


* Experience Cloud と Creative Cloud のアセットの同期を制御する機能フラグを追加しました。（CORE-15938）


* 検索およびリスト表示の改善を含む、オーディエンスセグメントの作成を強化しました。（CORE-5833、CORE-14278）
* Experience Cloud から Creative Cloud へのフォルダーの共有をブロックする、優先度の高い問題を修正しました。（CORE-16677）

## 2018 年 7 月 19 日（PT） {#section_EBB549EBABB7480884A180237ADCCD02}

2018 年 7 月の修正点と機能強化です。

* Experience Cloud と AEM、Experience Cloud と Creative Cloud 間のアセット共有を制御するバックエンド機能を導入しました。（CORE-14386）


* 一部の環境において新規テナントのプロビジョニングを妨げていた問題を修正しました。（CORE-15509）


* [!DNL experiencecloud.adobe.com]（保護された接続）ではなく [!DNL experiencecloud.adobe.com] で [!DNL http] にアクセスすると、ユーザーが [!DNL https] にリダイレクトされる問題を修正しました。（CORE-15587）
* 一部の新規テナントに対する通知を妨げていた問題を修正しました。（CORE-15240）

## 2018 年 6 月 14 日 {#section_7ABC327992CB46B0B8E4A631B8B68899}

2018 年 6 月の修正点と機能強化です。

* 管理者のメニューに GDPR アクセスへのリンクを追加しました。（CORE-11731）
* フィードバックに添付できるファイルタイプが制限されるよう、ベータフィードバック機能が更新されました。（CORE-10474）


* オーディエンスライブラリからオーディエンスを削除する際に発生していた問題を修正しました。（CORE-12792）


* Federated ID を使用してワークスペースのリンクへアクセスすると画面が空白になっていた問題を修正しました。（CORE-11620）



## 2018 年 5 月 11 日 {#section_498AF78DA17C4720AA0F32B51493E550}

[!DNL Adobe Experience Cloud] インターフェイスの新機能および修正点です。

| 機能 | 説明 |
|--- |--- |
| 新しい管理用ランディングページ | Experience Cloud にログインして「管理」ページに移動すると、Experience Cloud アプリケーションやコアサービスにすばやくアクセスするのに役立つ、新しい直感的なインターフェイスが利用できます。 |

{style=&quot;table-layout:auto&quot;}

**修正点**

* Scene7 アップデートが原因で画像のアップロードが失敗する問題を修正しました。（CORE-12746）
* TLS 1.0 プロトコルのサポートが廃止されました。このことは、セキュリティの脆弱性除去を目的に PCI によって義務付けられています。（CORE-7695）

## 2017 年 10 月 27 日 {#section_11195859B4094177A939C0561428B525}

**既知の問題**

通知用のダイジェスト電子メールに、定期メンテナンス／製品アップデートに関するメンテナンス通知の多くが記載されていません。すべてのメンテナンス通知がダイジェストメールに確実に記載されるよう、アドビでは現在対応を進めております。

## 2017 年 8 月 9 日 {#section_2313A875454044F490B418506DD24593}

| 機能 | 説明 |
|--- |--- |
| 通知 - 詳細設定 | [顧客属性](attributes.md)のアップロードアクティビティに関する通知など、製品およびアプリケーションのイベントとアクティビティの通知を有効にできます。 |
| 通知 - メンテナンス通知 | 通知設定で、製品およびアプリケーションのメンテナンス通知を有効にできます。 |
| Experience Cloud ソリューション向け Admin Console | Experience Cloud の新規のお客様は、Admin Console を利用することで組織全体にわたってアドビ製品の使用権限を一元的に管理できます。<br>Admin Console へのユーザー管理の移行は段階的に進められます。移行が必要になると、アドビからお客様（システム管理者の皆様）に連絡させていただきます。<br>Analytics 管理者向けの情報については、[Analytics の移行](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=ja)を参照してください。 |

{style=&quot;table-layout:auto&quot;}

## 2017 年 5 月 22 日（PT） {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| 機能 | 説明 |
|--- |--- |
| レポートスイートの一括マッピング | 管理／レポートスイートのマッピングで、複数のレポートスイートを選択して、1 つの組織にマッピングできるようになりました（以前は、個別にマッピングする必要がありました）。<br>[レポートスイートを単一の組織にマッピング](core-services.md)すると、Experience Cloud のクロスアプリケーション機能とサービスを有効にするのに役立ちます。 |
| Experience Cloud オーディエンスの更新 | **レポートスイートの適用**<br>&#x200B;すべての[オーディエンスルール](t-audience-create.md)にレポートスイートを適用できるようになりました（以前は、ルール定義ごとにレポートスイートを指定する必要がありました）。<br>**Prop と変数**<br>（eVar およびイベント変数に加えて）リアルタイムオーディエンスに Analytics の prop およびデフォルト変数を含めることができるようになりました。 |

{style=&quot;table-layout:auto&quot;}

## 2016 年 11 月 8 日（PT）- 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| 機能 | 説明 |
|--- |--- |
| プロファイルおよびパスワードの更新 | ユーザーはプロファイルを編集／プロファイルおよびパスワードの「個人の詳細情報」で IMS ユーザープロファイル情報を編集できなくなりました。代わりに、ユーザーは `accounts.adobe.com` にリダイレクトされます。この更新は、すべての ID タイプ（Adobe ID、Enterprise ID、Federated ID）に適用されます。 |

{style=&quot;table-layout:auto&quot;}

**修正点**

* Creative Cloud と Experience Cloud でのフォルダー共有時にエラーが発生する原因となっていた、パスワードに関する技術的な問題が修正されました。（MAC-31067、MAC-32014）
* 10 月のリリース後に Assets Core Service で発見された、特定のファイルタイプ（PDF など）のアップロードに関する問題が修正されました。（MAC-32517）


