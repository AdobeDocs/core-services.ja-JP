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
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 59%

---

# サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響 {#how-changes-to-third-party-cookie-support-impacts-customers}

サードパーティcookieのサポートは、ブラウザーをまたいで制限されるようになりました。 そのため、Adobeは、顧客の要件と、Experience Cloudのアプリケーション全体でプライバシーを保護する消費者の権利とのバランスを慎重にとる新しいソリューションに取り組んでいます。

サードパーティcookieのサポートがExperience Cloudアプリケーションの現在の実装に及ぼす影響を以下に示します。

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
   * Adobeは、広告配信に対する影響の範囲を完全に評価するために、社内およびアドビの広告パートナーと協力して作業を進めています。
