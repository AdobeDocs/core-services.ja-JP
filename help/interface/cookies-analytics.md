---
description: Adobe Experience Cloud の Adobe Analytics の Cookie について説明します。
solution: Experience Cloud,Analytics,Target
title: Analytics の cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: 8f500c7efc0bba2239d81eb9be64916d60d2ea3d
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 95%

---

# Analytics の cookie {#analytics-cookies}

Adobe Analytics では、異なるブラウザーからのリクエストを区別する目的と、アプリケーションによって後で使用されることがある有用な情報を保存する目的で cookie を使用します。また、ブラウジング情報を顧客レコードに関連付けるためにも使用できます。

Analytics では、新しい訪問者を匿名で識別する手段、クリックストリームデータ分析の参考情報、その web サイトにおける行動履歴（特定のキャンペーンに対する反応、販売サイクルの長さなど）の追跡手段として Cookie を使用します。

* [cookie 名：s_ecid](cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [cookie 名：AMCV_###@AdobeOrg](cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [cookie 名：s_cc](cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [cookie 名：s_cc](cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [cookie 名：s_sq](cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [cookie 名：s_vi](cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [cookie 名：s_fid](cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [プラグインで設定される cookie](cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

詳細については、Analytics のヘルプで [ファーストパーティ cookie](cookies-first-party.md) に関するトピックを参照してください。

## cookie 名：s_ecid {#section-32fd753c3fa54452acd62b021434919a}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | Experience Cloud ID（ECID）または MID のコピーが含まれます。MID は、s_ecid=MCMID という構文に従うキーと値のペアとして保存されます。 | `<ECID>` |
| 有効期限 | 2 年。 |
| 用途 | この cookie は、AMCV cookie がクライアントで設定された後に、お客様のドメインで設定されます。この cookie の目的は、ファーストパーティ状態の永続的 ID トラッキングを許可し、AMCV cookie の有効期限が切れた場合に参照 IDとして使用することです。詳しくは、こちらの AMCV cookie を参照してください。 |
| 場所 | CNAME のお客様のみ。サードパーティのシナリオには適用されません。Cookie はお使いのドメインに保存され、同じドメインが CNAME および Analytics イメージリクエストで使用されます。 |
| サイズ | 45 バイト。 |

{style="table-layout:auto"}

## cookie 名：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | この cookie は、cookie が有効になっている（「True」に設定されている）かどうかを判断するために JavaScript コードによって設定され、読み取られます。 |
| 有効期限 | この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 |
| 用途 | すべてのアカウントに対して 1 つの cookie のみ。 |
| 場所 | この cookie はページのドメインに保存されます。 |
| サイズ | 4 バイト。 |

{style="table-layout:auto"}

## cookie 名：s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | この cookie は、ClickMap機能またはActivity Map機能が有効になっている場合に JavaScript コードによって設定および読み取られます。この cookie には、ユーザーが以前に選択したリンクに関する情報が含まれます |
| 有効期限 | この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 |
| 用途 | すべてのアカウントに対して 1 つの cookie のみ。 |
| 場所 | この cookie はページのドメインに保存されます。 |
| サイズ | ページ URL サイズによって変わりますが、通常は 100 ～ 200 バイトです。 |

{style="table-layout:auto"}

## cookie 名：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | 一意の訪問者 ID 日時スタンプ。 |
| 有効期限 | 2 年。 |
| 用途 | この cookie は、ユニーク訪問者を特定するために使用します。 |
| 場所 | この cookie は、イメージリクエストのドメインに保存されます。そのドメインは通常、2o7.net（サードパーティ cookie を使用している場合）または omtrdc.net（ファーストパーティ cookie を使用している場合）の下の顧客固有のサブドメインになります。 |
| サイズ | 44 バイト。 |

{style="table-layout:auto"}

>[!NOTE]
>
>各 Analytics 訪問者 ID は、Adobe サーバー上の訪問者プロファイルに関連付けられます。訪問者プロファイルは、1 年間操作が実行されなかった場合は訪問者 ID cookie の有効期限にかかわらず削除されます。

## cookie 名：s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 属性 | 説明 |
|--- |--- |
| 保存される情報 | 予備として使用される一意の訪問者 ID 日時スタンプ。 |
| 有効期限 | 2 年。 |
| 用途 | この cookie は、ユニーク訪問者を特定するために使用します。サードパーティ cookie が制限されていて標準の `s_vi` cookie を設定できない場合に、個別訪問者を特定するために使用します。ファーストパーティ cookie が使用される環境では使用しません。 |
| 場所 | この cookie はファーストパーティ cookie として会社のドメインに保存されます。 |
| サイズ | 33 バイト。 |

{style="table-layout:auto"}

## cookie のフラグ

Analytics cookie のフラグを次の表に示します。

| cookie（設定元） | httpOnly | 安全 | SameSite |
|--- |--- |--- |--- |
| s_vi（HTTP 応答） | × | SameSite が &quot;None&quot; で、接続が HTTPS を使用する場合は○ | CNAME を使用する場合はデフォルトで &quot;Lax&quot; になります。2o7.net または omtrdc.net を使用する場合は &quot;None&quot; です。 |
| s_ecid（HTTP 応答） | × | × | &quot;Lax&quot; |
| s_fid（JavaScript） | × | × | 未設定 |
| s_cc（JavaScript） | × | × | 未設定 |
| s_sq（JavaScript） | × | × | 未設定 |

{style="table-layout:auto"}

>[!NOTE]
>
>1 つの CNAME を使用して複数のドメインまたはプロパティにわたって追跡する場合、`s_vi` の SameSite は &quot;None&quot; に設定する必要があります。Analytics cookie の設定の変更については、カスタマーケアへのお問い合わせ。

## プラグインで設定される cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

{{plug-in}}

使用する Analytics プラグインによっては、上記以外の cookie も設定されることがあります。これらの cookie は、様々な状況でクライアントに使用できるコードスニペットです。使用する状況としては、例えば、URL から値を取得する場合、Analytics に渡す値を連結する場合、また、放棄されたセッションの情報を捕捉する場合などが考えられます。一例として、*Set Once Per* プラグインおよび&#x200B;*Set and Get Last Value* プラグインでは [!DNL s_vh] という cookie が使用されます。

電子メール内に配置されるコードなど、JavaScript を使用しないイメージリクエスト時に渡されるコンバージョン変数（eVarX）は、電子メールクライアントと web ブラウザーが cookie 領域を共有している場合にのみ適切に関連付けられます。
