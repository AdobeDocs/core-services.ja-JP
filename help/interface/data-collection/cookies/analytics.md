---
description: Adobe Experience Cloud の Adobe Analytics の Cookie について説明します。
solution: Analytics
title: Adobe Analyticsの cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: d3a559ca2f7963256d48a25cd51099edb5e3fe76
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 11%

---

# Adobe Analyticsの cookie

Adobe Analytics では、異なるブラウザーからのリクエストを区別する目的と、アプリケーションによって後で使用されることがある有用な情報を保存する目的で cookie を使用します。また、ブラウジング情報を顧客レコードに関連付けるためにも使用できます。

Analytics では、新しい訪問者を匿名で定義する手段、クリックストリームデータ分析の参考情報、その web サイトにおける行動履歴（特定のキャンペーンに対する反応、販売サイクルの長さなど）の追跡手段として Cookie を使用します。

| cookie 名 | 有効期限 | サイズ | ロケーション | 説明 |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 13 か月 | 45 バイト。 | ファーストパーティ | Experience Cloud ID （ECID）または MID を格納します。 HTTP 応答で設定します。 MID は `s_ecid=MCMID` 形式で保存されます。 クライアントが AMCV cookie を設定した後にを設定します。 これにより、永続的なファーストパーティ ID のトラッキングが可能になり、AMCV cookie の有効期限が切れた場合に参照 ID として使用されます。 `SameSite` は「Lax」に設定されています。 Web SDKを使用してAdobe Analyticsを実装する場合、cookie の有効期限は 2 年に設定されますが、ほとんどのブラウザーでは有効期限が 13 か月に切り捨てられます。 |
| **`s_cc`** | Session | 4 バイト。 | ファーストパーティ | Cookie が有効かどうかを判断します。 JavaScriptで設定。 |
| **`s_sq`** | Session | 100～200 バイト | ファーストパーティ | Activity Mapで使用されます。 訪問者がクリックした前のリンクに関する情報が含まれます。 JavaScriptで設定。 |
| **`s_vi`** | 2 年。 | 44 バイト。 | ファーストパーティまたは `*.omtrdc.net` （サードパーティ） | ユニーク訪問者 ID とタイムスタンプを格納します。 HTTP 応答で設定します。 各訪問者 ID は、Adobe サーバーの訪問者プロファイルに関連付けられます。 訪問者プロファイルは、訪問者 ID cookie の有効期限に関係なく、1 年間無操作状態が続くと削除されます。 `Secure` フラグは、`SameSite` が「なし」で、接続が HTTPS の場合に設定されます。 フ `SameSite` ーストパーティ cookie の場合、デフォルトは「Lax」です。 `SameSite` や `omtrdc.net` など、サードパーティ Cookie を使用する場合、`2o7.net` れは「なし」です。 単一の CNAME を使用して複数のドメインまたはプロパティを追跡する場合は、「`SameSite`」を「なし」に設定します。 |
| **`s_fid`** | 2 年。 | 33 バイト。 | ファーストパーティ | フォールバックユニーク訪問者 ID とタイムスタンプを格納します。 サードパーティ cookie の制限により標準 `s_vi` cookie を設定できない場合は、JavaScriptによって設定されます。 ファーストパーティ cookie の実装には使用されません。 |
| **`s_ac`** | 即時 | 1 バイト | ファーストパーティ | AppMeasurement Cookie を設定する正しいドメインを判断するのに役立ちます。 静的な値 `"1"` が含まれます。 この cookie は、設定されると直ちに削除されます。 |

## プラグインで設定される cookie

一部の実装ではプラグインを利用します。プラグインは、Analytics に追加機能を提供するコードのスニペットです。 これらのプラグインは、上記に記載されていない Cookie を設定できます。 使用可能なプラグインのリストと設定対象の Cookie については、[Analytics プラグインの概要 ](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins) を参照してください。

## Analytics cookie 削除の結果

訪問者が Analytics の Cookie を削除する場合は、次の点を考慮してください。

* **訪問者の識別が失われます：** Cookie が削除されると、Adobe Analyticsは再訪問者を認識できません。 次回ユーザーがサイトを訪問すると、新規訪問者としてカウントされます。 [ クロスデバイス分析 ](https://experienceleague.adobe.com/en/docs/analytics/components/cda/overview) を使用すると、この影響を軽減できます。
* **セッションの連続性が失われます：** セッションベースまたは複数訪問の分析（アトリビューションやコンバージョントラッキングなど）が中断されます。 Cookie の削除後に発生するイベントと変換は、同じユーザーが以前のアクティビティに結び付けることはできません。
* **Personalizationとセグメント化が影響を受けます：** 以前のデータが現在の訪問と関連付けられなくなるため、訪問者の履歴や行動に基づいてセグメントやパーソナライズされたエクスペリエンスがリセットされます。
* **クロスドメイントラッキングが中断される：** サードパーティ Cookie の場合、それらを削除すると、Adobe Analyticsは所有する複数のドメイン間でユーザーアクティビティをリンクできなくなります。
