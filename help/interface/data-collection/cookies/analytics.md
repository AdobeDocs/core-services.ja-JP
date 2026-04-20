---
description: Adobe CX EnterpriseのAdobe Analytics Cookieについて説明します。
solution: Analytics
title: Adobe Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
TQID: https://experienceleague.adobe.com/H-N88ygcQUcUIej1Kkwlv9UmIe1qPDYwo-qF3TdDqHg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 10%

---

# Adobe Analytics cookie

Adobe Analytics では、異なるブラウザーからのリクエストを区別する目的と、アプリケーションによって後で使用されることがある有用な情報を保存する目的で cookie を使用します。 また、閲覧情報を顧客レコードに関連付けることもできます。

Adobe Analyticsでは、Cookieを使用して新規訪問者を匿名で定義し、クリックストリームデータを分析して、特定のキャンペーンへの対応やセールスサイクルの長さなどのweb サイト上の過去のアクティビティを追跡します。

| cookie 名 | 有効期限 | サイズ | ロケーション | 説明 |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 13 か月 | 45 バイト。 | ファーストパーティ | CX Enterprise ID （ECID）またはMIDを格納します。 HTTP レスポンスで設定します。 MIDは`s_ecid=MCMID`形式で保存されます。 クライアントがAMCV Cookieを設定した後に設定します。 永続的なファーストパーティ ID トラッキングを許可し、AMCV Cookieの有効期限が切れた場合は参照IDとして使用されます。 `SameSite`は「Lax」に設定されています。 Web SDKを使用してAdobe Analyticsを実装する場合、Cookieの有効期限は2年に設定されますが、ほとんどの最新のブラウザーでは、有効期限は13か月に切り捨てられます。 |
| **`s_cc`** | Session | 4 バイト。 | ファーストパーティ | Cookieが有効かどうかを指定します。 JavaScriptによる設定。 |
| **`s_sq`** | Session | 100 ～ 200 バイト | ファーストパーティ | Activity Mapで使用。 訪問者がクリックした前のリンクに関する情報が含まれます。 JavaScriptによる設定。 |
| **`s_vi`** | 2 年。 | 44 バイト。 | ファーストパーティ、または`*.omtrdc.net` （サードパーティ） | 一意の訪問者IDとタイムスタンプを保存します。 HTTP レスポンスで設定します。 各訪問者IDは、Adobe サーバー上の訪問者プロファイルに関連付けられます。 訪問者プロファイルは、訪問者ID Cookieの有効期限にかかわらず、非アクティブ状態が1年後に削除されます。 `SameSite`が「なし」で、接続がHTTPSの場合、`Secure` フラグが設定されます。 `SameSite`は、ファーストパーティ Cookieのデフォルトでは「Lax」です。 `SameSite`は、`omtrdc.net`や`2o7.net`などのサードパーティ Cookieを使用する場合、「なし」です。 単一のCNAMEを使用して複数のドメインまたはプロパティを追跡する場合は、`SameSite`を「なし」に設定します。 |
| **`s_fid`** | 2 年。 | 33 バイト。 | ファーストパーティ | フォールバックの一意の訪問者IDとタイムスタンプを保存します。 サードパーティ Cookieの制限により、標準の`s_vi` Cookieを設定できない場合は、JavaScriptで設定します。 1st パーティ Cookieの実装には使用されません。 |
| **`s_ac`** | 即時 | 1 バイト | ファーストパーティ | AppMeasurement Cookieを設定するための正しいドメインを特定するのに役立ちます。 静的値`"1"`が含まれます。 このCookieが設定されると、すぐに削除されます。 |

Adobe AnalyticsがCookieを使用して訪問者を識別する方法について詳しくは、[Adobe Analyticsでの訪問者特定](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/overview)を参照してください。

## プラグインで設定される cookie

一部の実装では、Analyticsの追加機能を提供するコードのスニペットであるプラグインを使用します。 これらのプラグインは、上記に記載されていないCookieを設定できます。 使用可能なプラグインのリストと、それらが設定するCookieについては、[Analytics プラグインの概要](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins)を参照してください。

## Analytics Cookieの削除による影響

訪問者がAnalytics Cookieを削除する場合は、次の点を考慮してください。

* **訪問者IDが失われます：** Cookieが削除されると、Adobe Analyticsは再訪問者を認識できません。 次回ユーザーがサイトにアクセスすると、新規訪問者としてカウントされます。
* **セッションの連続性が壊れています：** セッションベースまたは複数訪問の分析（アトリビューションやコンバージョンの追跡など）が中断されています。 Cookie削除後に発生するイベントとコンバージョンは、同じユーザーによる以前のアクティビティと関連付けることはできません。
* **Personalizationとセグメント化は影響を受けます：**&#x200B;以前のデータが現在の訪問に関連付けられなくなったため、訪問者の履歴や行動に基づくセグメントまたはパーソナライズされたエクスペリエンスはリセットされます。
* **クロスドメインのトラッキングが中断されます：** サードパーティ Cookieの場合、それらを削除すると、所有している複数のドメイン間でAdobe Analyticsがユーザーアクティビティをリンクできなくなります。

