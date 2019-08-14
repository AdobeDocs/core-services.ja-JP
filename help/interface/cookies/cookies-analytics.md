---
description: Adobe Analytics では、異なるブラウザーからの要求を区別する目的と、アプリケーションによって後で使用されることがある有用な情報を保存する目的で cookie を使用します。また、閲覧行動と顧客レコードを関連付ける目的にも使用します。
keywords: cookie;プライバシー
seo-description: Adobe Analytics では、異なるブラウザーからの要求を区別する目的と、アプリケーションによって後で使用されることがある有用な情報を保存する目的で cookie を使用します。また、閲覧行動と顧客レコードを関連付ける目的にも使用します。
seo-title: Analytics の cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Analytics の cookie
uuid: e2d3d61d-2708-48b2- a7e6-2331f2aed8e0
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics では、異なるブラウザーからの要求を区別する目的と、アプリケーションによって後で使用されることがある有用な情報を保存する目的で cookie を使用します。また、閲覧行動と顧客レコードを関連付ける目的にも使用します。

特に、Analytics では、新しい訪問者を匿名で識別する手段、クリックストリームデータ分析の参考情報、その Web サイトにおける行動履歴（特定のキャンペーンに対する反応、販売サイクルの長さなど）の追跡手段として cookie を使用します。

* [Cookie名:s_ ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [cookie 名：AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [cookie 名：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [cookie 名：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [cookie 名：s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [cookie 名：s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [cookie 名：s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [プラグインで設定される cookie](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

詳細については、Analytics のヘルプで[ファーストパーティ cookie](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_overview.html) に関するトピックを参照してください。

## Cookie名:s_ ecid {#section-32fd753c3fa54452acd62b021434919a}

<table id="table_FF4C70D3D4CC425BA65162D5A9504F7D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p> Experience Cloud ID（ECID）またはMIDのコピーが含まれます。MIDは、この構文に続くキーと値のペアに格納されています。s_ ecid= MCMID|&lt; ECID&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p>2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p>このcookieは、AMCV cookieがクライアントによって設定された後に、顧客のドメインによって設定されます。このcookieの目的は、1^ st^パーティ状態で永続的なIDトラッキングを許可し、AMCV cookieの有効期限が切れた場合に参照IDとして使用されることです。詳しくは、こちらのAMCV cookieを確認してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 場所 </p> </td> 
   <td colname="col2"> <p>CNAMEのお客様のみ。3^ d^パーティシナリオに適用されません。cookieはドメインに保存され、CNAMEとAnalyticsイメージリクエストで使用されるドメインと同じドメインに保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Size </p> </td> 
   <td colname="col2"> <p>45 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

<table id="table_34AA90F2FFB84500A77D8F4C5008D453"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p> この cookie は、cookie が有効になっている（「True」に設定されている）かどうかを判断するために JavaScript コードによって設定され、読み取られます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p> この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p> すべてのアカウントに対して 1 つの cookie のみ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 場所 </p> </td> 
   <td colname="col2"> <p> この cookie はページのドメインに保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> サイズ </p> </td> 
   <td colname="col2"> <p> 4 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

<table id="table_05EEB54B5EA2409DB1D071FD1484E8F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p> この cookie は、ClickMap 機能と Activity Map 機能が有効になっている場合に JavaScript によって設定され、読み取られます。ユーザーが直前にクリックしたリンクに関する情報が含まれています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p> この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p> すべてのアカウントに対して 1 つの cookie のみ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 場所 </p> </td> 
   <td colname="col2"> <p> この cookie はページのドメインに保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> サイズ </p> </td> 
   <td colname="col2"> <p> ページ URL サイズによって異なりますが、一般には 100 ～ 200 バイトです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

<table id="table_774F04AA9E3847D9AE7803520B5AAAE3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p> 一意の訪問者 ID 日時スタンプ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p> 2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p> この cookie は、個別訪問者を特定するために使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 場所 </p> </td> 
   <td colname="col2"> <p> この cookie は、イメージ要求のドメインに保存されます。そのドメインとは、サードパーティ cookie を使用していれば多くの場合は 2O7.net であり、ファーストパーティ cookie を使用していれば自社のドメインになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> サイズ </p> </td> 
   <td colname="col2"> <p> 44 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>各Analytics訪問者IDは、Adobeサーバー上の訪問者プロファイルに関連付けられています。訪問者プロファイルは、1 年間操作が実行されなかった場合は訪問者 ID cookie の有効期限にかかわらず削除されます。

## cookie 名：s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

<table id="table_B0EDB50677D14A86A1BFB7CCAAE95C88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p> 予備として使用される一意の訪問者 ID 日時スタンプ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p>5 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p> この cookie は、個別訪問者を特定するために使用します。 サードパーティ cookie が制限されていて標準の <span class="codeph">s_vi</span> cookie を設定できない場合に使用します。ファーストパーティ cookie が使用される環境では使用しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 場所 </p> </td> 
   <td colname="col2"> <p> この cookie はファーストパーティ cookie として会社のドメインに保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> サイズ </p> </td> 
   <td colname="col2"> <p> 33 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>

## プラグインで設定される cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

使用する Analytics プラグインによっては、上記以外の cookie も設定されることがあります。それらの cookie は、様々な状況でクライアントから使用できるコードスニペットです。使用する状況としては、例えば、URL から値を取得する場合、Analytics に渡す値を連結する場合、また、放棄されたセッションの情報を捕捉する場合などが考えられます。各種プラグインで実際に設定される cookie について詳しくは、ClientCare にお問い合わせください。一例として、[!DNL s_vh]*Set Once Per プラグインおよび**Set and Get Last Value プラグインでは* という cookie が使用されます。

電子メール内に配置されるコードなど、JavaScript を使用しないイメージ要求時に渡されるコンバージョン変数（eVarX）は、電子メールクライアントと Web ブラウザーが同じ cookie 領域を共有している場合にのみ適切に関連付けられます。
