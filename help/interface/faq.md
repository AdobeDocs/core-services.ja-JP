---
description: ブラウザーのサポートについて説明し、Adobe Experience Cloud の管理者向けに回答されたよくある質問を取得します。
keywords: コアサービス、Experience Cloud、Experience Platform、Analytics、Target、ユーザー管理。
solution: Experience Cloud
title: 'Experience Cloud に関するよくある質問 '
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 062576da-328e-4b46-9e71-5a25733d607a
source-git-commit: 84d33be461ef26c8aadba8f47bd93875356d3ad4
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 93%

---

# Experience Cloud に関するよくある質問

Experience Cloud 管理者向けのブラウザーサポート、よくある質問および回答について説明します。

## Experience Cloud でサポートされているブラウザーは何ですか。

* Microsoft® Edge（最新バージョンおよび最新バージョンの 2 つ前までのバージョン）
* Google Chrome（最新バージョン、および最新バージョンの 2 つ前までのバージョン）
* Mozilla Firefox（最新バージョン、および最新バージョンの 2 つ前までのバージョン）
* Safari（最新バージョン、および最新バージョンの 2 つ前までのバージョン）
* Opera（最新バージョン、および最新バージョンの 2 つ前までのバージョン）

## アプリケーションでコアサービスが有効になっているかどうかを確認するにはどうすればよいですか？

実装がコアサービス用にプロビジョニングされていない場合は、その方法について説明した[アプリケーションをコアサービス用に有効化する](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)を参照してください。

1. [Experience Cloud に加入して管理者になる](core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [Experience Platform Launch を利用して Experience Cloud ID サービスを実装する](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=ja)。
1. [レポートスイートを Experience Cloud 組織にマッピングする](core-services.md#concept_apg_zq2_rw)
1. [（Analytics のみ）Analytics AppMeasurement コードを最新化する](core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [（Adobe Target のみ）Adobe Target の実装を最新化する](core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [実装の検証](core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [ユーザーと製品を管理する](core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [コアサービスの使用を開始する](core-services.md#section_960C06093623462E8EA247B3E97274A1)

さらにサポートが必要な場合は、[アドビサポートにお問い合わせください](https://experienceleague.adobe.com/?support-solution=General&amp;lang=ja#support)。

## Experience Cloud にアクセスするには料金がかかりますか。

いいえ。Experience Cloud の利用に追加料金はかかりません。ただし、コアサービスによっては追加コストがかかる場合があります。

## Experience Cloud インターフェイスを利用してログインしなければならないのはなぜですか。

Experience Cloud インターフェイスが提供する機能は、ビジネスに新しい価値をもたらします。これは、今後アプリケーションにアクセスするための標準パスでもあり、最終的には他の個々のアプリケーションのログインフローに取って代わります。Experience Cloud を利用してログインすると、今後の移行をよりスムーズにおこなうことができます。

## 移行に関する問題を解決するにはどのようにしますか。

[アドビサポートに問い合わせてください](https://experienceleague.adobe.com/?support-solution=General#support)。

## 方法 [!DNL Adobe Support] 問題のトラブルシューティングを行うには、Adobeクラウド環境にアクセスしますか？

[!DNL Adobe Support] は、明示的な認証を求めるAdobeブランドの電子メール（以下の例）を受け取る偽装リクエストを送信できます。 アクセス権は、限られた時間に対して付与されます。 一旦許可されると、ユーザーはいつでもアクセスを取り消すことができます。 Adobeは、Adobe担当者が実行したすべてのアクションを記録します。

![](/help/interface/admin-getting-started/assets/support-email.png)

## _プロビジョニング_&#x200B;の特長について教えてください。

Experience Cloud でのプロビジョニングは、次のことを意味します。

* ユーザーは、[!DNL Experience Cloud] へのログインとアプリケーションのリンクを開始できます。
* 人物など、Experience Cloud で利用できる機能を使い始めることができます。
* アプリケーション固有のログインプロセスを終了する準備ができます。
* アプリケーションへのアクセス制御を保持できます。

## ユーザーや製品プロファイルを管理するにはどうすればよいですか。

* 詳しくは、[Admin Console ユーザーガイド](https://helpx.adobe.com/jp/enterprise/admin-guide.html)を参照してください。

* ユーザーの使用権限と製品の管理は [Adobe Admin Console](https://adminconsole.adobe.com/enterprise)（製品リンク）でおこないます。

* **重要：** Analytics 管理ツールから Admin Console へのユーザー ID の移行に関する Analytics 管理者向けの詳細情報については、[Admin Console での Analytics ユーザーの管理](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/migrate-users/c-migration-tool.html?lang=ja)を参照してください。

## ユーザーが Experience Cloud にログインできない場合、管理者はどのように対処しますか。

Admin Console 管理者はユーザーにアクセス権を付与できます。ユーザーにはログイン手順が記載された電子メールが送信されます。

会社としてのプロビジョニングが完了していることを確認するために、[アドビサポートへの問い合わせ](https://experienceleague.adobe.com/?support-solution=General#support)が必要になる場合もあります。

## アカウントのリンクはどこで管理できますか。

一部のユーザーは、アプリケーション（Analytics）アカウントを Adobe ID または Enterprise ID へリンクする必要が生じる場合があります。

[アプリケーションアカウントを Adobe ID にリンクする](organizations.md#task_FD389E78640848919E247AC5E95B8369)を参照してください。

## ユーザーアカウントプロファイルと組織を管理するにはどうすればよいですか。

[ユーザーアカウントの管理](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)を参照してください。

## 組織とは

*組織*&#x200B;は、管理者がグループおよびユーザーの設定や、Experience Cloud でのシングルサインオンの制御を行なえるエンティティです。この組織は、Experience Cloud のすべての製品とアプリケーションにまたがるログイン会社のように機能します。ほとんどの場合、組織は勤務先の会社名です。ただし、1 つの会社が多くの組織を持つことができます。

## IMS 組織 ID はどこにありますか。

詳しくは、[組織 ID の検索](organizations.md)を参照してください。

組織 ID は、Experience Cloud ランディングページおよび[Admin Console ランディングページ](https://adminconsole.adobe.com)に表示されます。

また、管理者が特定の組織の Admin Console（[https://adminconsole.adobe.com](https://adminconsole.adobe.com) に移動）にログインすれば、その URL で IMS 組織 ID を確認できます。

例として、次の URL を見てみましょう。

`https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

ID は次のとおりです。

`C538193582390300A495CC9@AdobeOrg`

## ユーザーの 1 人が会社を辞めた場合はどうすればよいですか？

そのユーザーのアクセスは、アプリケーション自体から削除する必要があります。アクセス権を削除されたユーザーは、その製品に対して Experience Cloud からのアクセスも、直接ログインによるアクセスもできなくなります。また、そのユーザーを Experience Cloud レベルで削除する必要もあります。

## Adobe ID とは何ですか。

[ID タイプ](https://helpx.adobe.com/jp/enterprise/using/identity.html)を参照してください。

## ユーザーのアプリケーションアカウントをリンクできますか？

いいえ。ユーザーは、自分のアプリケーションを自分のユーザー名とパスワードでリンクさせる必要があります。

## Social を利用していないのに Social と表示されるのはなぜですか。

Adobe Social は、Analytics と共に購入できる製品です。そのため、Analytics を使用している場合は、このアプリケーションが表示されますが、購入しない限りアクセスできません。
