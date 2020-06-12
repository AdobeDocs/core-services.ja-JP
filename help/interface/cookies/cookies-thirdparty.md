---
description: 様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。
keywords: cookies;privacy
seo-description: 様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。
seo-title: サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: ht
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566
workflow-type: ht
source-wordcount: '368'
ht-degree: 100%

---


# サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響 {#how-changes-to-third-party-cookie-support-impacts-customers}

様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。

サードパーティ cookie のサポートが Adobe Experience Cloud ソリューションの現在の実装環境に及ぼす影響を以下に示します。

## Adobe Analytics および Adobe Target

* [ファーストパーティ実装](/help/interface/cookies/cookies-first-party.md)をお使いのお客様への影響はほとんどありません。
* ファーストパーティ実装を使用していないお客様は、[Experience Platform ID サービス](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html)を実装して、ID cookie をファーストパーティ実装なしでファーストパーティ cookie として保存できます。

## Adobe Experience Manager

* Adobe Experience Manager はお客様のドメイン内でのみ稼動し、サードパーティ cookie とのインタラクションがほとんど発生しないので、影響はほとんどありません。

## Adobe Social

* 最新バージョンのコードを使用している限り、Social への影響はありません。

## Adobe Advertising Cloud

* 検索：

   * 検索が Adobe Analytics のデータを利用して最適化されている場合は、Adobe Analytics と同様の影響が検索にも現れます。
   * コンバージョンデータの収集への影響はありません。

* 表示：

   * 現在、表示リマーケティングは全面的にサードパーティ cookie に依存しています。
   * また、各種広告ネットワークの cookie を同期に利用できるかどうかも表示に大きく影響します。
   * 全体的な影響は不明ですが、少なくとも、表示は他のサービスよりも大きく影響を受けます。
   * 現在、アドビは社内だけでなく、広告パートナーとも協力して、広告配信に対する影響の範囲を完全に測定できるように取り組んでいます。

* ソーシャル：

   * Facebook マーケットプレイス広告への影響はありません。
   * Facebook Exchange（FBX）は表示広告配信と同じ影響を受けます。
