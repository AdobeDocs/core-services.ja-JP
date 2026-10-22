---
title: Adobe Experience Platform Web SDK Cookie
description: Web SDKが、実装に適用されるCookieを使用する方法について説明します。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: 'https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
    internal-label: Getting started
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 7b12d5debfccd62ab7b416e9a6fe278d251a4ca5
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 0%
---
# Adobe Experience Platform Web SDKのCookie

Adobe Experience Platform Web SDKでは、実装に固有の値を保存するためにCookieを使用します。

| 名前 | 最大年齢 | サイズ | 説明 |
| --- | --- | --- | --- |
| **`AMCV_###@AdobeOrg`** | 33696000 （390日） Web SDKによって書かれた場合 | Web SDK （`MCMID\|<ECID>`）によって書き込まれた場合は44 バイト、書き込まれた場合は大きくなります（`VisitorAPI.js`） | [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)が有効になっている場合に表示されます。これはデフォルトです。 サイトの一部がまだ`VisitorAPI.js`を使用している間に、Web SDKに移行する際に役立ちます。 Web SDKは、このCookieを読み取り、既存のECIDを再利用します。 Edge NetworkがECIDを返した後、Cookieが見つからないか、別のECIDが含まれている場合、Web SDKはこのCookieに書き込みます。 |
| **`com.adobe.alloy.getTld`** | なし（セッション Cookie、すぐに削除） | 22 バイト | Web SDKが現在のサイトのトップレベルドメインを判断するために内部で使用する一時的なヘルパーCookie。 Web SDKは、ライブラリの読み込み時に、`configure` コマンドの実行前および同意が評価される前にこのCookieを書き込み、削除します。これにより、Cookie スキャナーは同意前に設定されたとしてレポートできます。 このCookieには独自の名前のみが含まれ、行動データやプロファイルデータは保存されません。 |
| **`demdex`** | 15552000 （180日間） | 可変 | `demdex.net` ドメインのサードパーティ Cookie。 [`thirdPartyCookiesEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/thirdpartycookiesenabled)が有効（デフォルト）で、ブラウザーでChromeやEdgeなどのサードパーティ Cookieがデフォルトで許可されている場合に表示されます。 この場合、Web SDKはID リクエストを`adobedc.demdex.net`に送信し、このCookieを設定します。 Audience Managerでは、このCookieを使用して一意のIDを割り当て、IDの同期、セグメンテーション、モデリング、レポート機能をサポートします。 [Audience Manager Cookie](audience-manager.md)の`demdex`を参照してください。 |
| **`kndctr_<orgId>_identity`** | 34128000 （395日） | 100 ～ 120 バイト（変数） | そのデバイスのECIDおよびその他の関連情報を保存します。 |
| **`kndctr_<orgId>_cluster`** | 1800 （30分） | 3 ～ 5 バイト | 現在のユーザーのリクエストを処理するEdge Network リージョン（場所ヒント）を保存します。 このリージョンは、Edge Networkがリクエストを正しいリージョンにルーティングできるように、URL パスで使用されます。 ユーザーがCookieの有効期間の中で別のIP アドレスに接続した場合、リクエストは再び最も近い地域にルーティングされます。 |
| **`kndctr_<orgId>_consent`** | 15552000 （180日間） | 10 ～ 11 バイト | 訪問者の同意設定を保存します。 同意の環境設定そのものを保存するため、同意に関係なく常に設定されます。 |
| **`kndctr_<orgId>_consent_check`** | 7200 （2時間） | | TTLの有効期限が切れた後、Edge Networkにサーバーサイドで同意を再チェックするようにシグナルを送る、セッション範囲のヘルパー。 キャッシュされた同意に対してTTLを適用します。 |
| **`kndctr_<orgId>_personalization`** | 34128000 （395日） | | Adobe Targetがコンテンツのパーソナライズに使用するセッション情報を保存します。 |
| **`kndctr_<orgId>_advertising`** | 31622400 （366日）、Cookieが更新されるたびに更新されます | 80 バイトから1 KB （変数） | Adobe Advertising コンポーネント （ベータ版）がWeb SDK ビルドに含まれ、訪問者の同意が`in`である場合に表示されます。 Web SDKは、ページ URLにAdobe Advertising クリックパラメーター（`s_kwcid`または`ef_id`）が含まれている場合、または[Adobe Advertising DSP](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)広告主が設定されている場合に、このCookieを書き込みます。 検索クリックデータ（`_les_lsc`）、ハッシュ化されたIP アドレス、LiveRampID エンベロープ（RampID JavaScript パスが設定されている場合）、重複コンバージョンのスロットリングに使用されるコンバージョンタイムスタンプを含むことができる、URL エンコードされたJSONが格納されます。 デフォルトでサードパーティ Cookieを許可するブラウザーでは、Adobe Advertising サーファーIDと表示クリックデータ （`ev_lcc`）も保存されます。 このCookieは現在のホスト名にのみ設定されます。 コンポーネントは、`pixel.everesttech.net`、`www.everestjs.net` （ID5 パートナーIDが設定されている場合）、およびRampID `ats.js` パスからもリソースを読み込みます。 これらのリソースは、このページに記載されていない独自のCookieを設定できます。 |
| **`kndctr_<orgId>_bc_session_id`** | なし（セッション Cookie） | | Brand Concierge コンポーネント（ベータ版）を使用する場合に表示されます。 Brand Concierge チャットセッション IDを保存します。 Web SDKは、[`stickyConversationSession`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/conversation)が有効になっている場合にのみ、このCookieを読み取るので、チャットセッションはページ読み込み全体で保持されます。 |
| **`mbox`** | 63072000 （2年間） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)が有効になっている場合に表示されます。 Web SDKでTarget [mbox cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)を設定できます。 |
| **`mboxEdgeCluster`** | 1800 （30分） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)が有効になっている場合に表示されます。 これにより、Web SDKは適切なエッジクラスターを`at.js`に通信できるので、ユーザーがサイトを移動してもTarget プロファイルを同期させることができます。 `kndctr_<orgId>_cluster` Cookieが存在しない場合、Web SDKはこのCookieも読み取り、リクエストを一致するEdge Network リージョンにルーティングします。 |
| **`s_ecid`** | 63115200 （2年間） | ～ 45 バイト | CX Enterprise ID （ECID/MID）のコピーを`s_ecid=MCMID\|<ECID>`形式で含みます。 ECIDのファーストパーティバックアップとして機能し、主にCNAME （ファーストパーティ）シナリオに対して機能します。 [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)が有効になっている場合、Web SDKはこのCookieを読み取り、既存のECIDを再利用します。 |
| **Audience Manager cookieの宛先** （名前は異なります） | 宛先が別のライフタイムを指定しない限り、864000 （10日間）です | 可変 | Edge Networkが訪問者のAudience Manager [cookieの宛先](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/destinations/custom-destinations/create-cookie-destination)を返したときに表示されます。 Web SDKは、宛先で定義されたCookie名、値、ドメインを使用して、ファーストパーティ Cookieを書き込みます。 値は、Audience Manager Data Integration Library（DIL）と一致するURL エンコードされます。 |

Edge Networkは、すべてのCookieを`secure`および`sameSite="none"`属性で設定します。 現在、web サイトに安全なセクションと安全でないセクションの両方がある場合、ユーザー識別が不正確になる可能性があります。 ユーザーがサイトの安全なセクションから安全でないセクションに移動すると、Edge Networkはリクエストとともに新しい`ECID`を生成します。

Web SDKがEdge Networkの方向ではなく、独自に作成するCookieは、異なる属性を使用します。 `AMCV_###@AdobeOrg` cookieおよびAudience Manager cookieの宛先には、HTTPS ページにのみ`secure`属性と`sameSite="none"`属性が含まれます。 `com.adobe.alloy.getTld`および`kndctr_<orgId>_advertising` Cookieは、ブラウザーのデフォルト属性を使用します。
