---
description: Audience Managerは、異なる機能を実行するために、いくつかの単純なcookieを使用します。 例えば、IDの割り当て、データ呼び出しの記録、エラー追跡、cookieが設定できるかどうかを確認するテストなどが含まれます。 この節では、Audience Managerで設定される様々なcookieの一覧と説明を示します。
keywords: cookies
seo-description: Audience Managerは、異なる機能を実行するために、いくつかの単純なcookieを使用します。 例えば、IDの割り当て、データ呼び出しの記録、エラー追跡、cookieが設定できるかどうかを確認するテストなどが含まれます。 この節では、Audience Managerで設定される様々なcookieの一覧と説明を示します。
seo-title: Audience Manager の cookie
solution: Marketing Cloud,Audience Manager
title: Audience Manager の cookie
uuid: 8b384c38-b85a-4e93-b00e-41a9d3ae2b21
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Audience Manager の Cookie{#audience-manager-cookies}

Audience Managerは、異なる機能を実行するために、いくつかの単純なcookieを使用します。 例えば、IDの割り当て、データ呼び出しの記録、エラー追跡、cookieが設定できるかどうかを確認するテストなどが含まれます。 この節では、Audience Managerで設定される様々なcookieの一覧と説明を示します。

**demdex cookie**

<table id="table_1CCF7EA2BC9E421F8DEECA5F611E33F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>目的</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager</span> は、サイト訪問者に一意の ID を割り当てることを目的としてこの cookie を設定します。<span class="keyword">Audience Manger</span> は <span class="wintitle">demdex</span> cookie を利用して、訪問者の識別、ID の同期、セグメント化、モデリング、レポート作成などの基本的な機能を実行します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>コンテンツ</b> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">demdex</span> cookie には次のような形式で一意のユーザー ID（UUID）が書き込まれます。 </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p><a href="https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/ids-in-aam.html" format="https" scope="external">Audience Manager の ID のインデックス</a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>その他の属性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">有効期間：<span class="wintitle">demdex</span> cookie の有効期間（TTL）は 180 日に設定されます。TTLは、パートナーのWebサイトとの各ユーザーのインタラクション時に180日にリセットされます。 TTLの間にユーザーがサイトに戻ってこない場合、cookieは期限切れになります。 </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. この場合、cookie の TTL は 10 年に設定されます。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**dextp cookie**

<table id="table_7343C9C9ADD24D3FA693ECC76E4A4045"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>目的</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> は、最後にデータ同期呼び出しをおこなった日時を記録することを目的としてこの cookie を設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>コンテンツ</b> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">dextp</span> cookie には、データプロバイダー名または ID と UNIX UTC タイムスタンプがパイプ区切り形式で書き込まれます。次の例に含まれる斜体の部分には実際の情報が入ります。<i></i> </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">Old style: <span class="codeph"> <span class="varname"> data provider name here </span>-1490307822097| <span class="varname"> data provider name here </span>-1490307822038 </span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">新しい形式：<span class="codeph">21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>後述のdextpデータ構文の節も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>その他の属性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">有効期間：<span class="wintitle">dextp</span> cookie の有効期間（TTL）は 180 日に設定されます。 </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. この場合、cookie の TTL は 10 年に設定されます。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

dextp cookie のデータ構文：

次の表に、データ文字列内の位置を基準として [!DNL dextp] cookie の要素を示します。

<table id="table_BE00604B97F24F5A94AA4F566063D785"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 可変位置 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>First or Second</b> </p> </td> 
   <td colname="col2"> <p>データプロバイダーの名前またはIDの位置は、cookieで新しい形式が使用されているか、古い形式が使用されているかによって異なります。 </p> <p> <b>古いスタイルの書式：</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Syntax: <span class="codeph"> <span class="varname"> data provider name </span> - <span class="varname"> UNIX UTC timestamp </span> </span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">例：<span class="codeph"> dataProvider1 - 1490307822038 </span> </li> 
     </ul> </p> <p>古いスタイルのcookieは、読み取り可能な名前を持つデータプロバイダーを識別します。 </p> <p> <b>新しいスタイルの書式：</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Syntax: <span class="codeph"> <span class="varname"> data provider ID </span> - 1|2 - <span class="varname"> UNIX UTC timestamp </span> </span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">例：<span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>新しいスタイルcookie: </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">読み取り可能なデータプロバイダー名を数値IDに置き換えます。 </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">ID 1またはID 2の呼び出しタイプを識別します。 ID 1はID同期呼び出しを表します。 ID 2は、使用されなくなった非推奨の呼び出しを表します。 ID 2のdextp cookieは多く（またはどれも）表示されません。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>最後</b> </p> </td> 
   <td colname="col2"> <p>最後の位置には、UNIXのUTCタイムスタンプが含まれます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**dst cookie**

<table id="table_83AE9B6350C6408BAECD9FCF33022B98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>目的</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> は、<a href="https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html#purposes" format="https" scope="external">宛先</a>へのデータ送信中にエラーが発生すると、この cookie を設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>コンテンツ</b> </p> </td> 
   <td colname="col2"> <p> <span class="wintitle">DST</span> cookie には、宛先の ID と UNIX タイムスタンプのセットがパイプ区切り形式で書き込まれます。次の例に含まれる斜体の部分には実際の情報が入ります。<i></i> </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">構文：<span class="codeph"> <span class="varname"> destination ID </span> - <span class="varname"> UNIX UTC タイムスタンプ </span> </span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">例：<span class="codeph">067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>その他の属性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">有効期間：<span class="wintitle">dst</span> cookie の有効期間（TTL）は 180 日に設定されます。 </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**_dp cookie**

これは一時的な cookie です。[!DNL Audience Manager] は、demdex.net ドメインにサードパーティのコンテキストで他の cookie を設定できるかどうかを確認することを目的として [!DNL _dp] cookie の設定を試みます。設定に成功した場合は、[!DNL _dp] に値 1 が書き込まれます。[!DNL Audience Manager] はこの値を読み取ると、即座にこの cookie を削除します。[!DNL _dp] cookie が存在しない場合、[!DNL Audience Manager] は cookie を設定できないものと判断します。