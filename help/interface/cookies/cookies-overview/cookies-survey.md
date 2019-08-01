---
description: Survey では、異なるブラウザーからの要求を区別する目的と、顧客感情をよりよく理解するために役立つ情報を保存する目的で cookie を使用します。
keywords: cookie;プライバシー
seo-description: Survey では、異なるブラウザーからの要求を区別する目的と、顧客感情をよりよく理解するために役立つ情報を保存する目的で cookie を使用します。
seo-title: Survey の cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Survey の cookie
uuid: e57d9b58-3c62-463a- ad52- e2a0de2e1ee1
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Survey の cookie{#survey-cookies}

Survey では、異なるブラウザーからの要求を区別する目的と、顧客感情をよりよく理解するために役立つ情報を保存する目的で cookie を使用します。

* [cookie 名：s_sv_sid](../cookies-overview/cookies-survey.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [cookie 名：s_sv_s1](../cookies-overview/cookies-survey.md#section-14ad50dfcd7342f9ac80283b1f0d3400)
* [cookie 名：s_sv_p1](../cookies-overview/cookies-survey.md#section-05d1c52c478541609f4a18a9c1eb032f)

## cookie 名：s_sv_sid {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 説明 |
|---|---|
| 保存される情報 | ブラウザー上に調査ページをレンダリングする目的で使用される JavaScript ファイルを確実にキャッシュするために、一意の数値が保存されます。 |
| 有効期限 | この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 |

## cookie 名：s_sv_s1 {#section-14ad50dfcd7342f9ac80283b1f0d3400}

<table id="table_6835D64C5D464A049F576621F2BE3FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 保存される情報 </td> 
   <td colname="col2"> <p> 
     <ul id="ul_350369AFBEFF49938026D7D25D012A88"> 
      <li id="li_EA3D03382BFA474B802D1EE2054FABDB">訪問者に調査の回答を促したときに「後で」をクリックされ、回答が延期された調査の ID が保存されます。 </li> 
      <li id="li_6111E8D568D64D7CBFB906046134025C"> Web サイトの直後に続くページで起動する予定だった調査の ID が保存されます。 </li> 
      <li id="li_A16519F487654435B50577DA08654E70">起動が開始された調査の ID が保存されます。 </li> 
      <li id="li_8322C91846AB4A65B277C435D61660BF">Survey システムが（延期された調査に対して）実行開始された時刻が保存されます。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 有効期限 </td> 
   <td colname="col2"> この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：s_sv_p1 {#section-05d1c52c478541609f4a18a9c1eb032f}

<table id="table_8F6CC83D32D54BEE99884318AD126C98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 保存される情報 </td> 
   <td colname="col2"> <p> 
     <ul id="ul_A2717AD89DA540468963E9E7FBD382D5"> 
      <li id="li_21B0165911C74BA796111E9C93142B95">回答することを承諾または拒否された調査の ID が保存されます。 </li> 
      <li id="li_DD966285CAE7438C9E43AFC4E91569F8">その訪問者がサンプルレートに適合したかどうかを指定する情報が保存されます。 </li> 
      <li id="li_27BD16FE78BC46C3846BFFE4DF65BCB3">訪問者がサイトから移動したことを確認するために「サイトからの離脱」調査の起動時に使用される、増加し続ける数値が保存されます。 </li> 
      <li id="li_0C9FF8939615407BB9A0DB24C7C31CE6">顧客により指定された疲労設定にその訪問者が到達したので調査から除外すべきであるかどうかを示すフラグが保存されます。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 有効期限 </td> 
   <td colname="col2"> この cookie は永続的な cookie です。 </td> 
  </tr> 
 </tbody> 
</table>

<a id="section_488AFFB899004968A2479B2423E6EEB7"></a>

>[!NOTE]
>
>s_ sv_ s1またはs_ sv_ p1に格納する情報が大きすぎる場合、必要に応じて、s_ sv_ s2、s_ sv_ s3、s_ sv_ p3などの名前を付けて、追加のcookieに分割して保存します。

