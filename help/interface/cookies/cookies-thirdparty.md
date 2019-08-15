---
description: 様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。
keywords: cookie;プライバシー
seo-description: 様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。
seo-title: サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響
solution: Marketing Cloud、Analytics、Target、Social
title: サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響
uuid: 27332e0d-6932-4a6e- b97b-0decomed0b050
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f59badcd3423ada51a3fe0c605158a009d5b1d64

---


# サードパーティcookieのサポートに対するお客様への変更の影響{#how-changes-to-third-party-cookie-support-impacts-customers}

様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。

サードパーティ cookie のサポートが Adobe Experience Cloud ソリューションの現在の実装環境に及ぼす影響を以下に示します。

## Adobe AnalyticsおよびAdobe Target

* [ファーストパーティの導入](/help/interface/cookies/cookies-first-party.md) をお持ちのお客様は、ほとんど影響を受けません。
* Customers that are not using first-party implementation can implement the [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html) to store the ID cookie as a first-party cookie without a first-party implementation.

## Adobe Experience Manager

* Adobe Experience Managerは顧客のドメイン内で完全に動作するので、サードパーティcookieとのやり取りが最小限になり、影響を最小限に抑えることができます。

## Adobe Social

* 最新バージョンのコードを使用している限り、Social への影響はありません。

## Adobe Advertising Cloud

* 検索:

   * 検索が Adobe Analytics のデータを利用して最適化されている場合は、Adobe Analytics と同様の影響が検索にも現れます。
   * コンバージョンデータの収集への影響はありません。

* 表示:

   * 現在、表示リマーケティングは全面的にサードパーティ cookie に依存しています。
   * また、各種広告ネットワークの cookie を同期に利用できるかどうかも表示に大きく影響します。
   * 全体的な影響は不明ですが、少なくとも、表示は他のサービスよりも大きく影響を受けます。
   * 現在、アドビは社内だけでなく、広告パートナーとも協力して、広告配信に対する影響の範囲を完全に測定できるように取り組んでいます。

* Social:

   * Facebook マーケットプレイス広告への影響はありません。
   * Facebook Exchange（FBX）は表示広告配信と同じ影響を受けます。

