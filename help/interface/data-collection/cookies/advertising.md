---
description: 広告エンゲージメントイベントをコンバージョンイベントにマッピングし、その情報を広告の入札を最適化するために使用するためのAdobe Advertising Cookieについて説明します。
title: Adobe Advertising Cookie
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
TQID: https://experienceleague.adobe.com/lbDHQNLf--xowxe4ZVZsGptwKyEzvT1wQV0QTFJyKpk
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 15%

---

# Adobe Advertising の cookie

Adobe Advertising（旧Adobe Advertising Cloud）は、Cookieを使用して広告エンゲージメントイベントをコンバージョンイベントにマッピングし、その情報を使用して広告入札を最適化しています。

>[!NOTE]
>
>[Adobe CX Enterprise ID （ECID） サービス &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja)を使用するベータ版Adobe Advertising Javascript タグは、Adobe Advertising Cookieではなく、ファーストパーティ [CX Enterprise](experience-cloud.md) `s_ecid`Cookieを作成します。

| cookie 名 | 有効期限 | サイズ | ロケーション | 説明 |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 分 | 52 バイト | `everesttech.net` | 表示クリックのIDとタイムスタンプを保存します。 ディスプレイ広告のクリックイベントがAdobe Analytics ヒットに適用されるかどうかを指定します。 |
| **`_tmae`** | 1 年 | 1 KB | `everesttech.net` | DSP トラッキングを使用して、広告エンゲージメント用にエンコードされたIDとタイムスタンプを保存します。 最後に閲覧した広告などの、広告に対するユーザーエンゲージメントが含まれます |
| **`_tmid`** | 1 年 | ～ 20 バイト | `everesttech.net` | Adobe Advertising Demand Side Platform（DSP） IDを格納します。 `everest_g_v2` Cookieの訪問者IDに対応します。 |
| **`adcloud`** | 1 年 | 50 ～ 150 バイト | ファーストパーティ | 訪問者の最後のweb サイトへの訪問と、訪問者の最後の検索クリックのタイムスタンプ。 訪問者が広告をクリックしたときに作成された`ef_id`も保存します。 訪問者IDを、関連するオーディエンスセグメントとコンバージョンに関連付けます。 Adobeに対する不要なリクエストを避けることで、ページの読み込み時間を最適化できます。 |
| **`ev_sync_*`** |  | 8 バイト。 | `everesttech.net` | 同期が`yyymmdd`形式で実行される日付。 Adobe Advertising訪問者IDをパートナー広告の交換と同期します。 新しい訪問者用に作成され、有効期限が切れると同期リクエストを送信します。 Cookie `ev_sync_ax`、`ev_sync_bk`、`ev_sync_dd`、`ev_sync_fs`、`ev_sync_ix`、`ev_sync_nx`、`ev_sync_ox`、`ev_sync_pm`、`ev_sync_rc`、`ev_sync_tm`および`ev_sync_yh`が含まれます。 |
| **`everest_g_v2`** | 1 年 | ～ 27 バイト | `everesttech.net` | ブラウザーと訪問者IDを保存します。 ユーザーが広告を最初にクリックした後に作成されます。 現在および以降のクリックを、web サイト上の他のイベントとマッピングするために使用します。 |
| **`everest_session_v2`** | Session | ～ 16 バイト | `everesttech.net` | 現在のセッション IDを保存します。 |
| **`id_adcloud`** | 91 日 | 16 バイト | ファーストパーティ | 訪問者IDを保存します。 |

{style="table-layout:auto"}

