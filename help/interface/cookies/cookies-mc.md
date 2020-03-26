---
description: Adobe Experience Cloud で訪問者 ID を保存するために使用される cookie は、様々な Experience Cloud ソリューションで利用されます。
keywords: cookies;privacy
seo-description: Adobe Experience Cloud で訪問者 ID を保存するために使用される cookie は、様々な Experience Cloud ソリューションで利用されます。
seo-title: Experience Cloud の cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Experience Cloud の cookie
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Experience Cloud の cookie{#experience-cloud-cookies}

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
   <td colname="col2"> <p>2年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p>この cookie は、AMCV cookie がクライアントで設定された後に、お客様のドメインで設定されます。このcookieの目的は、ファーストパーティ状態での永続的なID追跡を許可することで、AMCV cookieの有効期限が切れた場合に参照IDとして使用されます。 詳しくは、こちらの AMCV cookie を参照してください。 </p> </td> 
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

[Experience Platform IDサービスは](https://docs.adobe.com/content/help/en/id-service/using/home.html) 、JavaScriptを使用して、現在のWebサイトのドメイン上の `AMCV_###@AdobeOrg` cookieに一意の訪問者IDを格納します。このcookieは、 `###` 次のような文字列をランダムに表します。 `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

See also, [Cookies and the ID Service](https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html).

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
   <td colname="col2"> <p> Experience Cloudソリューションで使用される一意の訪問者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 有効期限 </p> </td> 
   <td colname="col2"> <p> 2年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 用途 </p> </td> 
   <td colname="col2"> <p> この cookie は、 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> ロケーション </p> </td> 
   <td colname="col2"> <p> この cookie は（イメージリクエストのドメインではなく）Web サイトのドメインに保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> サイズ </p> </td> 
   <td colname="col2"> <p> 多くのお客様は、このcookieの長さが約200バイトであると考えています。 </p> </td> 
  </tr> 
 </tbody> 
</table>
