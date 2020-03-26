---
description: Adobe Analyticsは、異なるブラウザーからの要求を区別し、後でアプリケーションが使用できる役立つ情報を保存する目的でcookieを使用します。 また、閲覧情報を顧客レコードに関連付けるためにも使用できます。
keywords: cookies;privacy
seo-description: Adobe Analyticsは、異なるブラウザーからの要求を区別し、後でアプリケーションが使用できる役立つ情報を保存する目的でcookieを使用します。 また、閲覧情報を顧客レコードに関連付けるためにも使用できます。
seo-title: Analytics の cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Analytics の cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Analytics の cookie{#analytics-cookies}

Adobe Analyticsは、異なるブラウザーからの要求を区別し、後でアプリケーションが使用できる役立つ情報を保存する目的でcookieを使用します。 また、閲覧情報を顧客レコードに関連付けるためにも使用できます。

特に、Analyticsは、cookieを使用して、新しい訪問者を匿名で定義し、クリックストリームデータの分析を支援し、特定のキャンペーンへの反応や販売サイクルの長さなど、Webサイト上での履歴アクティビティを追跡します。

* [cookie 名：s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [cookie 名：AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [cookie 名：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [cookie 名：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie名：s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [cookie 名：s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie名：s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [プラグインで設定されるCookie](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

詳しくは、Analyticsヘルプのファーストパーティcookieに [関する情報を参照してください](/help/interface/cookies/cookies-first-party.md)。

## cookie 名：s_ecid {#section-32fd753c3fa54452acd62b021434919a}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | Experience Cloud ID（ECID）または MID のコピーが含まれます。MID は、s_ecid=MCMID という構文に従うキーと値のペアとして保存されます。 | `<ECID>` |
| 有効期限 | 2年 |
| 用途 | この cookie は、AMCV cookie がクライアントで設定された後に、お客様のドメインで設定されます。この cookie の目的は、ファーストパーティ状態の永続的 ID トラッキングを許可し、AMCV cookie の有効期限が切れた場合に参照 IDとして使用することです。詳しくは、こちらの AMCV cookie を参照してください。 |
| 場所 | CNAME のお客様のみ。サードパーティのシナリオには適用されません。Cookie はお使いのドメインに保存され、同じドメインが CNAME および Analytics イメージリクエストで使用されます。 |
| サイズ | 45 バイト |

## cookie 名：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | このcookieは、JavaScriptコードによって設定および読み取られ、cookieが有効かどうかを判断します（単に「True」に設定する）。 |
| 有効期限 | このcookieはセッションcookieで、ブラウザーを閉じると有効期限が切れます |
| 用途 | すべてのアカウントに対して1つのCookieのみ |
| ロケーション | このcookieは、ページのドメインに保存されます。 |
| サイズ | 4 バイト |

## Cookie Name: s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | このcookieは、ClickMap機能またはActivity Map機能が有効な場合に、JavaScriptコードによって設定および読み取られます。ユーザーがクリックした以前のリンクに関する情報が含まれます。 |
| 有効期限 | このcookieはセッションcookieで、ブラウザーを閉じると有効期限が切れます |
| 用途 | すべてのアカウントに対して1つのCookieのみ |
| ロケーション | このcookieは、ページのドメインに保存されます。 |
| サイズ | ページ URL サイズによって変わりますが、通常は 100 ～ 200 バイトです。 |

## cookie 名：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | 個別訪問者IDの時間/日付スタンプ |
| 有効期限 | 2年 |
| 用途 | この cookie は、 |
| ロケーション | このcookieはイメージリクエストのドメイン（サードパーティcookieを使用している場合は、通常は2o7.netまたはomtrdc.netの下の顧客固有のサブドメイン）に保存されます。また、ドメインでファーストパーティcookieを使用している場合も同様です。 |
| サイズ | 44 バイト |

>[!NOTE]
>
>各 Analytics 訪問者 ID は、Adobe サーバー上の訪問者プロファイルに関連付けられます。訪問者プロファイルは、1 年間操作が実行されなかった場合は訪問者 ID cookie の有効期限にかかわらず削除されます。

## Cookie Name: s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | フォールバックの一意の訪問者IDのタイムスタンプ |
| 有効期限 | 2年 |
| 用途 | この cookie は、 if the standard  `s_vi` cookie is unavailable due to third-party cookie restrictions. ファーストパーティcookieを使用する実装には使用されません。 |
| ロケーション | このcookieは、ファーストパーティcookieとしてドメインに保存されます。 |
| サイズ | 33 バイト |

## cookieフラグ

次の表に、Analytics cookieのフラグを示します。

| Cookie（設定者） | httpOnly | セキュア | SameSite |
|--- |--- |--- |--- |
| s_vi （http応答） | × | はい（同じサイトが「なし」で、接続にHTTPSが使用されている場合） | CNAME[名前管理]コマンドを使用した場合の既定値は&quot;Lax&quot;です。 2o7.netまたはomtrdc.netを使用する場合は「なし」。 |
| s_ecid （http応答） | × | × | &quot;Lax&quot; |
| s_fid (JavaScript) | × | × | 未設定 |
| s_cc(JavaScript) | × | × | 未設定 |
| s_sq(JavaScript) | × | × | 未設定 |

>[!NOTE] 単一のCNAMEを使用して複数のドメインまたはプロパティで追跡する場合、SameSiteは「なし」に設定する必要がありま `s_vi`す。 Analytics cookieの設定の変更については、カスタマーケアにお問い合わせください。

## プラグインで設定されるCookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

Analyticsプラグインの使用に応じて、追加のcookieを設定できます。 これらのcookieは、様々な状況で使用できるコードスニペットです。 次のような状況が考えられます。urlからの値の取得；analyticsに渡す値の連結；フォームの中断のキャプチャなど。 各種プラグインで実際に設定される cookie について詳しくは、ClientCare にお問い合わせください。一例として、*Set Once Per* プラグインおよび&#x200B;*Set and Get Last Value* プラグインでは [!DNL s_vh] という cookie が使用されます。

電子メール内に配置されるコードなど、JavaScript を使用しないイメージリクエスト時に渡されるコンバージョン変数（eVarX）は、電子メールクライアントと Web ブラウザーが同じ cookie 領域を共有している場合にのみ適切に関連付けられます。
