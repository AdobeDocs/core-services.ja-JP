---
description: ブラウザーでサードパーティ cookie のサポートがますます制限されるようになっている状況について説明します。
keywords: cookie;プライバシー
solution: Experience Cloud,Analytics,Target
title: 'サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響  '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookie
topic: 管理
role: Admin
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: ht
source-wordcount: '267'
ht-degree: 100%

---

# サードパーティ cookie のサポートに対する変更がお客様に及ぼす影響 {#how-changes-to-third-party-cookie-support-impacts-customers}

サードパーティ cookie のサポートは、ブラウザーをまたいでさらに制限されるようになりました。そのため、アドビは、Experience Cloud アプリケーション全体で顧客の要件と消費者のプライバシーの権利のバランスを慎重にとる新しいソリューションに取り組んでいます。

サードパーティ cookie のサポートが Experience Cloud アプリケーションの現在の実装環境に及ぼす影響を以下に示します。

## Adobe Analytics および Adobe Target

* 同じサイトアクティビティはファーストパーティ cookie のみに依存しているため、Analytics と Target はほとんど影響を受けません。複数のドメインをまたいだユーザーアクティビティを理解するには、サードパーティ cookie が必要です。サードパーティ cookie がブロックされているブラウザーの場合、cookie を使用したクロスドメイントラッキングはできません。

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
   * アドビは、社内およびアドビの広告パートナーと協力して、広告配信に対する影響の範囲を完全に評価できるように取り組んでいます。
