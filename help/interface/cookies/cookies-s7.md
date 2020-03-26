---
description: Scene7 では、ブラウザーにダイナミックメディアを配信するために役立つ情報を保存する目的で cookie を使用します。
keywords: cookies;privacy
seo-description: Scene7 では、ブラウザーにダイナミックメディアを配信するために役立つ情報を保存する目的で cookie を使用します。
seo-title: Scene7 の cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Scene7 の cookie
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Scene7 の cookie{#scene-cookies}

Scene7 では、ブラウザーにダイナミックメディアを配信するために役立つ情報を保存する目的で cookie を使用します。

一部の古いAS2 Flashベースのビューア用に、情報がローカルに保存されます。

AS2ビューアの場合、cookie:

* 現在のページや画像、現在のズームレベルなど、ユーザのセッション状態を追跡します。
* ユーザーの前回のセッションからの経過時間を確認します。 この情報は、前のセッションを続行するか、新しいセッションを開始するかを決定するために使用されます。 この情報はScene7サーバにも送信されますが、この情報は使用されません。

AS2 Flash eCatalogビューアの場合、cookieは次のとおりです。

* ユーザーが生成したコンテンツ（特に、eCatalogビューアの「付箋」機能でユーザーが入力したコンテンツ）を保存します。 このコンテンツは、ユーザーがセッションを再開すると復元されます。
* ユーザーが電子メールを開始してeCatalogを別のユーザーと共有すると、2番目のAS2ビューアの箇条書きのノート注釈の内容がアドビのサーバーにコピーされ、受信者に提供されます。 受信者がビューアセッションを開始すると、ノート注釈のコンテンツがサーバーから取得され、cookieにコピーされます。 この機能はあまり使用されないので、期限切れにならず、古いコンテンツは削除されません。 現時点では、サーバー上での保持は無期限です。

新しいAS3ビューアでは、セッションパーシスタンスは実装されません。

**Cookie名：VatLogin.jsp**

| 属性 | 説明 |
|---|---|
| 保存される情報 | セッションcookieを設定します。 IPS ImageServer（IS、IR、SWF/スキン、ビデオコンテキスト）に埋め込まれたAuthFilterは、アクセス認証にcookieを使用します。 存在する場合、HTTPリクエストの受け渡しが許可されます。 それ以外の場合は、未認証で返されます。 |
| 有効期限 | このcookieはセッションcookieです。 Scene7 IPS [!DNL web.xml] で、現在のセッションの有効期限は 45 分に設定されています。 |

**cookie 名：s7js.flyout.InfoMessage.displayed`assetId`.state**

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
   <td colname="col2"> <p>&lt;assetId&gt;は、ビューアが操作しているアセットの名前です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 有効期限 </td> 
   <td colname="col2"> このCookieはセッションCookieで、ブラウザーを閉じると有効期限が切れます。 </td> 
  </tr> 
 </tbody> 
</table>

**cookie 名：s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

ブラウザーのcookieは、従来のDHTMLビューアで、状態情報とノート注釈データの保存に使用されます。 また、複数画面のDHTMLフライアウトでは、メッセージインジケーターをセッションに固有にする目的でも使用されます。

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
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt;は、ビューアが操作しているアセットの名前で、&lt;id&gt;は0を基準とするノート注釈のインデックスです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 有効期限 </td> 
   <td colname="col2"> このCookieはセッションCookieで、ブラウザーを閉じると有効期限が切れます。 </td> 
  </tr> 
 </tbody> 
</table>

