---
description: Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。
keywords: cookies;privacy
seo-description: Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。
seo-title: Target の cookie
solution: Marketing Cloud,Analytics,Target,Social
title: Target の cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Adobe Target Cookies{#target-cookies}

Adobe Targetは、Webサイトの運営者に対して、訪問者により関連性の高いオンラインコンテンツやオファーをテストする機能を提供するためにcookieを使用します。

cookieの期間を除き、必要に応じてこれらの設定を変更できます。 Cookieの設定を変更する場合は、アカウント担当者にお問い合わせください。

>[!NOTE]
>
>Adobe Targetユーザーは、カスタマイズしたサードパーティCookieを作成することもできます。

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 設定 </th> 
   <th colname="col2" class="entry"> 情報 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie名 </p> </td> 
   <td colname="col2"> <p>mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookieドメイン </p> </td> 
   <td colname="col2"> <p>mboxを扱うドメインの2番目と最上位のレベル。 会社のドメインなので、cookie はファーストパーティ cookie になります。例：<span class="filepath">mycompany.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サーバードメイン </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> clientcode.tt.omtrdc.net</span>。Adobe Targetアカウントのクライアントコードを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookieの期間 </p> </td> 
   <td colname="col2"> <p>cookieは、訪問者の最後のログインから2年間、訪問者のブラウザーに残ります。 Cookieの期間は変更できません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>いずれかのドメイン名に国コードが含まれている場合は（例：[!DNL mycompany.co.uk]）、クライアントサービスにお問い合わせのうえ、ご使用のドメインをサポートするように [!DNL mbox.js] を設定してください。

Cookieには、訪問者がAdobe Targetキャンペーンを体験する方法を管理するための多数の値が保持されます。

<table id="table_5245F72A2D5A4322B40ABB10B7DFB338"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 値 </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> session ID</span> </p> </td> 
   <td colname="col2"> <p>ユーザーセッションの一意のID。 デフォルトでは、30分間存続します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>訪問者のブラウザーの半永久的なID。 Cookieが手動で削除されるまで存続します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>訪問者がcookieをサポートしているかどうかを判断するために使用される単純なテスト値です。 訪問者がページをリクエストするたびに設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>訪問者の読み込み時間が <span class="filepath">mbox.js</span> ファイルで設定されているタイムアウトを超えた場合に設定されます。デフォルトでは、1 時間存続します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

