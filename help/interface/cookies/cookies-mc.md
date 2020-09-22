---
description: Adobe Experience Cloud で訪問者 ID を保存するために使用される cookie は、様々な Experience Cloud ソリューションで利用されます。
keywords: cookies;privacy
seo-description: Adobe Experience Cloud で訪問者 ID を保存するために使用される cookie は、様々な Experience Cloud ソリューションで利用されます。
seo-title: Experience Cloud の cookie
solution: Experience Cloud,Analytics,Target
title: Experience Cloud の cookie
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
translation-type: tm+mt
source-git-commit: 11ce83401a12c25853cd6412413b8abf98dd6612
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 100%

---


# Experience Cloud の cookie {#experience-cloud-cookies}

Adobe Experience Cloud で訪問者 ID を保存するために使用される cookie は、様々な Experience Cloud ソリューションで利用されます。

**cookie 名：s_ecid**

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
   <td colname="col2"> <p> Experience Cloud ID（ECID）または MID のコピーが含まれます。MID は、s_ecid=MCMID|&lt;ECID&gt; という構文に従うキーと値のペアとして保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p>2 年。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p>この cookie は、AMCV cookie がクライアントで設定された後に、お客様のドメインで設定されます。この cookie の目的は、ファーストパーティ状態の永続的 ID トラッキングを許可し、AMCV cookie の有効期限が切れた場合に参照 IDとして使用することです。詳しくは、こちらの AMCV cookie を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 場所 </p> </td> 
   <td colname="col2"> <p>CNAME のお客様のみ。サードパーティのシナリオには適用されません。Cookie はお使いのドメインに保存され、同じドメインが CNAME および Analytics イメージリクエストで使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> サイズ </p> </td> 
   <td colname="col2"> <p>45 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>

**cookie 名：AMCV_###@AdobeOrg**

[Experience Platform ID サービス](https://docs.adobe.com/content/help/ja-JP/id-service/using/home.html)では、JavaScript を使用して現在の Web サイトのドメインの `AMCV_###@AdobeOrg` cookie に一意の訪問者 ID を保存します（`###` には `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.` などのランダムな文字列が入ります）。

詳しくは、[Cookie と ID サービス](https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/cookies.html)を参照してください。

<table id="table_1883C0836C1E4AF5A262FBF5000C1B11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p> Experience Cloud ソリューションで使用される一意の訪問者 ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p> 2 年。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p> この cookie は、 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 場所 </p> </td> 
   <td colname="col2"> <p> この cookie は（イメージリクエストのドメインではなく）Web サイトのドメインに保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> サイズ </p> </td> 
   <td colname="col2"> <p> この cookie の長さは状況に応じて変化しますが、通常は 200 バイト程度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>
