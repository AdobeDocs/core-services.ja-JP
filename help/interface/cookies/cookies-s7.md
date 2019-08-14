---
description: Scene7 では、ブラウザーにダイナミックメディアを配信するために役立つ情報を保存する目的で cookie を使用します。
keywords: cookie;プライバシー
seo-description: Scene7 では、ブラウザーにダイナミックメディアを配信するために役立つ情報を保存する目的で cookie を使用します。
seo-title: Scene7 の cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Scene7 の cookie
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Scene7 の cookie{#scene-cookies}

Scene7 では、ブラウザーにダイナミックメディアを配信するために役立つ情報を保存する目的で cookie を使用します。

Scene7 は AS2 Flash をベースとする一部の古いビューア向けに情報をローカルに保存します。

AS2 ビューア向けの cookie には次の特徴があります。

* ユーザーのセッションの状態（現在のページ、表示した画像、現在のズームレベルなど）を追跡するために使用されます。
* ユーザーの前回のセッション以降に経過した時間を確認するために使用されます。ビューアはこの情報を使用して前回のセッションを再開するか新しいセッションを開始するかを決定します。この情報は Scene7 サーバーにも送信されますが、使用されません。

AS2 Flash をベースとする eCatalog ビューア向けの cookie には次の特徴があります。

* ユーザーによって生成されたコンテンツ（eCatalog ビューアの「ノート注釈」機能を使用してユーザーが入力する最も注目すべきコンテンツ）が保存されます。このコンテンツはユーザーがセッションを再開するときに復元されます。
* ユーザーが他のユーザーと eCatalog を共有するために電子メールを開始すると、2 番目の AS2 ビューアブレットのノート注釈コンテンツがアドビのサーバーにコピーされて、受信者に提供できる状態になります。受信者がビューアセッションを開始すると、ノート注釈コンテンツがサーバーから取得されて cookie にコピーされます。この機能はほとんど使用されないので、有効期限は設定されず、古いコンテンツも削除されません。現在のところ、アドビのサーバーにはこれらのコンテンツが無期限に保存されます。

新しい AS3 ビューアにはセッション継続機能が実装されていません。

* [cookie 名：VatLogin.jsp](../cookies-overview/cookies-s7.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie名:s7js. flyout. InfoMessage. displayed. state](../cookies-overview/cookies-s7.md#section-14ad50dfcd7342f9ac80283b1f0d3400)
* [Cookie名:s7js. flyout. InfoMessage. displayed_ idx. ant](../cookies-overview/cookies-s7.md#section-05d1c52c478541609f4a18a9c1eb032f)

## cookie 名：VatLogin.jsp {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 説明 |
|---|---|
| 保存される情報 | セッション cookie を設定します。IPS ImageServer に組み込まれる AuthFilter（IS、IR、および SWF／スキンとビデオのコンテキスト）では、この cookie がアクセス認証用に使用されます。これが存在する場合、HTTP 要求は通過が許可され、存在しない場合は未承認で戻されます。 |
| 有効期限 | この cookie はセッション cookie です。Scene7 IPS [!DNL web.xml] で、現在のセッションの有効期限は 45 分に設定されています。 |

## Cookie名:s7js. flyout. InfoMessage. displayed<assetId>.state {#section-14ad50dfcd7342f9ac80283b1f0d3400}

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
   <td colname="col2"> <p>&lt;assetId&gt; は、閲覧者がアクセスしているアセットの名前です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 有効期限 </td> 
   <td colname="col2"> この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 </td> 
  </tr> 
 </tbody> 
</table>

## Cookie名:s7js. flyout. InfoMessage. displayed<assetId>_idx<id>. ant {#section-05d1c52c478541609f4a18a9c1eb032f}

ブラウザー cookie は、従来形式のビューアでは状態情報およびノート注釈データの保存に使用されます。また、マルチスクリーン DHTML フライアウトでは、メッセージインジケーターをセッションに特化させる目的に使用されます。

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
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; は閲覧者がアクセスしているアセットの名前です。&lt;id&gt; はノート注釈のインデックス番号で、先頭は 0 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 有効期限 </td> 
   <td colname="col2"> この cookie はセッション cookie で、ブラウザーを閉じると有効期限が切れます。 </td> 
  </tr> 
 </tbody> 
</table>

