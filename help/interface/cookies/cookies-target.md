---
description: Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。
keywords: cookie;プライバシー
seo-description: Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。
seo-title: Target の cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Target の cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Target の cookie{#target-cookies}

Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。

cookie の期間を除き、必要に応じてこれらの設定を変更できます。cookie の設定を変更する場合は、アカウント担当者にお問い合わせください。

>[!NOTE]
>
>Targetユーザーは、カスタマイズされたサードパーティCookieを作成することもできます。

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 設定 </th> 
   <th colname="col2" class="entry"> 情報 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>cookie 名 </p> </td> 
   <td colname="col2"> <p>mbox。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookie ドメイン </p> </td> 
   <td colname="col2"> <p>mbox を扱うドメインの 2 番目および最上位のレベルです。mbox は会社のドメインから扱うので、cookie はファーストパーティ cookie になります。例：<span class="filepath">mycompany.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サーバードメイン </p> </td> 
   <td colname="col2"> <p> <span class="filepath">clientcode.tt.omtrdc.net</span>。Target アカウントのクライアントコードを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookie の期間 </p> </td> 
   <td colname="col2"> <p>cookie が訪問者のブラウザーに残る期間は、訪問者が最後にログインしてから 2 週間です。cookie の期間は変更できません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If any of your domain names include a country code, such as [!DNL mycompany.co.uk], work with your Client Services to configure your [!DNL mbox.js] to support this.

cookie には、訪問者が Target キャンペーンをエクスペリエンスとして体験する方法を管理するための様々な値が保持されています。

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
   <td colname="col2"> <p>ユーザーセッションの一意の ID。デフォルトでは、30 分間存続します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>訪問者のブラウザーの半永久的な ID です。cookie が手動で削除されるまで存続します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>訪問者が cookie をサポートするかどうかを判別するために使用される簡単なテスト値。訪問者がページをリクエストするたびに設定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>訪問者の読み込み時間が <span class="filepath">mbox.js</span> ファイルで設定されているタイムアウトを超えた場合に設定されます。デフォルトでは、1 時間存続します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

