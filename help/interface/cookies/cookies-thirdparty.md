---
description: ブラウザーでサードパーティ Cookie のサポートがますます制限されるようになっている状況について説明します。
keywords: cookie;プライバシー
solution: Experience Cloud,Analytics,Target
title: 'サードパーティ Cookie のサポートに対する変更が顧客に与える影響 '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: ef6196c3096ac7b26633eb4b1b9b2db26237732a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 84%

---

# サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響 {#how-changes-to-third-party-cookie-support-impacts-customers}

様々なブラウザーでサードパーティ cookie のサポートが制限され始めている状況を受け、アドビでは Adobe Experience Cloud ソリューション全体にわたり、お客様のニーズとプライバシーのバランスを慎重に考慮した新しいソリューションの開発に取り組んでいます。

サードパーティ cookie のサポートが Adobe Experience Cloud ソリューションの現在の実装環境に及ぼす影響を以下に示します。

## Adobe Analytics および Adobe Target

* 同じサイトアクティビティがファーストパーティcookieのみに依存するので、AnalyticsとTargetはほとんど影響を受けません。 複数のドメインにわたるユーザーアクティビティを理解するには、サードパーティCookieが必要です。 サードパーティCookieがブロックされているブラウザーの場合、Cookieを使用したクロスドメイントラッキングはできません。

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
