---
description: Adobe Experience Cloud の Adobe Analytics の Cookie について説明します。
solution: Experience Cloud,Analytics,Target
title: Adobe Analyticsの cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: 2691f0dc91e48a8f817467e334d9028f2e506e70
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 16%

---

# Adobe Analyticsの cookie

Adobe Analytics では、異なるブラウザーからのリクエストを区別する目的と、アプリケーションによって後で使用されることがある有用な情報を保存する目的で cookie を使用します。また、ブラウジング情報を顧客レコードに関連付けるためにも使用できます。

Analytics では、新しい訪問者を匿名で定義する手段、クリックストリームデータ分析の参考情報、その web サイトにおける行動履歴（特定のキャンペーンに対する反応、販売サイクルの長さなど）の追跡手段として Cookie を使用します。

| cookie 名 | 有効期限 | サイズ | ロケーション | 説明 |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 2 年。 | 45 バイト。 | ファーストパーティ | Experience CloudID （ECID）または MID を格納します。 HTTP 応答で設定します。 MID は、に保存されます。 `s_ecid=MCMID` 形式。 クライアントが AMCV cookie を設定した後にを設定します。 これにより、永続的なファーストパーティ ID のトラッキングが可能になり、AMCV cookie の有効期限が切れた場合に参照 ID として使用されます。 この cookie は、サードパーティ cookie 実装には適用されません。 `SameSite` は「Lax」に設定されています。 |
| **`s_cc`** | Session | 4 バイト。 | ファーストパーティ | Cookie が有効かどうかを判断します。 JavaScript で設定。 |
| **`s_sq`** | Session | 100～200 バイト | ファーストパーティ | Activity Mapが使用します。 訪問者がクリックした前のリンクに関する情報が含まれます。 JavaScript で設定。 |
| **`s_vi`** | 2 年。 | 44 バイト。 | ファーストパーティ `*.omtrdc.net` （サードパーティ） | ユニーク訪問者 ID とタイムスタンプを格納します。 HTTP 応答で設定します。 各訪問者 ID は、Adobeサーバーの訪問者プロファイルに関連付けられます。 訪問者プロファイルは、訪問者 ID cookie の有効期限に関係なく、1 年間無操作状態が続くと削除されます。 この `Secure` フラグが設定されるのは、 `SameSite` は「なし」、接続は HTTPS です。 `SameSite` は、ファーストパーティ cookie の場合、デフォルトでは「Lax」です。 `SameSite` 次に示すようなサードパーティ cookie を使用している場合は「なし」になります `omtrdc.net` または `2o7.net`. を設定 `SameSite` 1 つの CNAME を使用して複数のドメインまたはプロパティを追跡する場合は、「なし」に設定します。 |
| **`s_fid`** | 2 年。 | 33 バイト。 | ファーストパーティ | フォールバックユニーク訪問者 ID とタイムスタンプを格納します。 規格が次の場合は JavaScript で設定 `s_vi` サードパーティ cookie の制限により、cookie を設定できない。 ファーストパーティ cookie の実装には使用されません。 |

{style="table-layout:auto"}

## プラグインで設定される cookie

一部の実装ではプラグインを利用します。プラグインは、Analytics に追加機能を提供するコードのスニペットです。 これらのプラグインは、上記に記載されていない Cookie を設定できます。 参照： [Analytics プラグインの概要](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins) 使用可能なプラグインのリストと、そのプラグインで設定されている cookie について説明します。
