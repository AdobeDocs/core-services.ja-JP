---
description: 広告エンゲージメントイベントをコンバージョンイベントにマッピングし、その情報を使用して広告入札を最適化する場合のAdobe Advertising Cookie について説明します。
title: Adobe Advertisingの cookie
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
TQID: https://experienceleague.adobe.com/lbDHQNLf--xowxe4ZVZsGptwKyEzvT1wQV0QTFJyKpk
product_v2: id: e1971122-7081-4556-9222-8a31bd71800c
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 12%

---

# Adobe Advertising の cookie

Adobe Advertising（旧称 Adobe Advertising Cloud）では、広告エンゲージメントイベントをコンバージョンイベントにマッピングしたり、その情報を使用して広告入札を最適化するために、cookie が使用されます。

>[!NOTE]
>
>[Adobe Experience Cloud ID （ECID） サービスを使用するベータ版Adobe Advertising JavaScript タグは ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja)Adobe Advertising Cookie ではなく、[Experience Cloud](experience-cloud.md) `s_ecid` Cookie を作成します。

| cookie 名 | 有効期限 | サイズ | ロケーション | 説明 |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 分 | 52 バイト | `everesttech.net` | 表示クリックの ID とタイムスタンプを保存します。 ディスプレイ広告のクリックイベントがAdobe Analytics ヒットに適用されるかどうかを指定します。 |
| **`_tmae`** | 1 年 | 1 KB | `everesttech.net` | DSP トラッキングを使用して広告エンゲージメントのエンコードされた ID とタイムスタンプを保存します。 広告（最後に閲覧された広告など）のユーザーエンゲージメントを含めます |
| **`_tmid`** | 1 年 | ～ 20 バイト | `everesttech.net` | Adobe Advertising Demand Side Platform（DSP） ID を格納します。 `everest_g_v2` cookie の訪問者 ID に対応します。 |
| **`adcloud`** | 1 年 | 50～150 バイト | ファーストパーティ | 訪問者が最後に web サイトに訪問して検索をクリックしたときのタイムスタンプ。 は、訪問者が広告をクリックしたときに作成された `ef_id` も格納します。 訪問者 ID を関連するオーディエンスセグメントおよびコンバージョンと結び付けます。 Adobeへの不要なリクエストを回避して、ページの読み込み時間を最適化できます。 |
| **`ev_sync_*`** |  | 8 バイト。 | `everesttech.net` | `yyymmdd` 形式で同期が実行された日付。 Adobe Advertising訪問者 ID をパートナー広告交換と同期します。 新規訪問者向けに作成され、有効期限が切れると同期リクエストを送信します。 `ev_sync_ax`、`ev_sync_bk`、`ev_sync_dd`、`ev_sync_fs`、`ev_sync_ix`、`ev_sync_nx`、`ev_sync_ox`、`ev_sync_pm`、`ev_sync_rc`、`ev_sync_tm` および `ev_sync_yh` の Cookie が含まれます。 |
| **`everest_g_v2`** | 1 年 | ～ 27 バイト | `everesttech.net` | ブラウザーと訪問者 ID を格納します。 ユーザーが最初に広告をクリックした後に作成されます。 現在および後続のクリックと web サイト上の他のイベントとのマッピングに使用します。 |
| **`everest_session_v2`** | Session | ～ 16 バイト | `everesttech.net` | 現在のセッション ID を格納します。 |
| **`id_adcloud`** | 91 日 | 16 バイト | ファーストパーティ | 訪問者 ID を格納します。 |

{style="table-layout:auto"}

