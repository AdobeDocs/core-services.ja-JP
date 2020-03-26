---
description: 様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。
keywords: cookies;privacy
seo-description: 様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。
seo-title: サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# How changes to third-party cookie support impact customers{#how-changes-to-third-party-cookie-support-impacts-customers}

様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。

次に、サードパーティcookieのサポートがAdobe Experience Cloudソリューションの現在の実装に与える影響の概要を示します。

## Adobe Analytics および Adobe Target

* [ファーストパーティ実装](/help/interface/cookies/cookies-first-party.md)をお使いのお客様への影響はほとんどありません。
* Customers that are not using first-party implementation can implement the [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html) to store the ID cookie as a first-party cookie without a first-party implementation.

## Adobe Experience Manager

* Adobe Experience Manager はお客様のドメイン内でのみ稼動し、サードパーティ cookie とのインタラクションがほとんど発生しないので、影響はほとんどありません。

## Adobe Social

* 最新バージョンのコードを使用している限り、Social への影響はありません。

## Adobe Advertising Cloud

* 検索：

   * Adobe Analyticsデータに基づいて検索が最適化される場所では、Adobe Analyticsと同じ方法で検索に影響が及びます。
   * コンバージョンデータの収集は影響を受けません。

* 表示：

   * 今日のディスプレイの再マーケティングは、サードパーティcookieの使用に完全に依存しています。
   * 表示は、様々な広告ネットワークcookieを同期に使用できるかどうかに大きく依存しています。
   * 全体的な影響は不明です。 ただし、最初のポイントでは、表示は他のサービスよりも影響を受けます。
   * アドビは社内および広告パートナーと協力して、広告配信への影響の全範囲を評価しています。

* ソーシャル：

   * Facebookマーケットプレイス広告には影響しません。
   * Facebook Exchange(FBX)は、ディスプレイ広告配信と同じ影響を受けます。
