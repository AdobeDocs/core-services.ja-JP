---
description: Adobe Advertisingエンゲージメントイベントをコンバージョンイベントにマッピングし、場合によっては、その情報を使用して広告の入札を最適化するための広告の cookie について説明します。
title: Adobe Advertisingの cookie
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 5d0e02713ec4b233e06ecd3ac0234d1526b947f1
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 75%

---

# Adobe Advertisingの cookie{#advertising-cloud-cookies}

Adobe Advertising( 旧称Adobe Advertising Cloud) は、広告エンゲージメントイベントをコンバージョンイベントにマッピングし、場合によってはその情報を使用して広告入札を最適化するために、cookie を使用します。

>[!NOTE]
>
>ベータAdobe AdvertisingJavaScript タグで、 [Adobe Experience Cloud ID(ECID) サービス](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja) 作成 [ファーストパーティExperience Clouds_ecid の cookie](cookies-first-party.md)ではなく、Adobe AdvertisingCookie です。

## cookie 名：_lcc

<table id="table_821F8EBE91F244CBA72B0975B961B908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>ディスプレイクリックの ID およびタイムスタンプ（yyyymmdd 形式）</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>15 分</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>ディスプレイ広告のクリックイベントが Adobe Analytics ヒットに適用されるかどうかを判断するために使用されるサードパーティ cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>52 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：_tmae

<table id="table_28C2B62595E240D5A3C3E0BE147748C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>Adobe Advertising DSPトラッキングを使用する広告エンゲージメント用のエンコードされた ID およびタイムスタンプ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>1 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>ユーザーエンゲージメントを広告と共に保存するサードパーティ cookie（「2016 年 6 月 30 日（PT）に最後に表示された広告 xyz123」など） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>状況に応じて変化します。データはエンコードされ、通常は 1 KB 未満です </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：adcloud

<table id="table_D7CD238736BC4571883F92F47673F57C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>広告主の Web サイトへのサーファーの最後の訪問のタイムスタンプ、サーファーの最後の検索クリックのタイムスタンプ、ユーザーが広告をクリックした際に作成された ef_id</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>1 年</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>サーファー ID を関連するオーディエンスセグメントおよびコンバージョンに関連付けるファーストパーティ cookie </p> <p> 最後の訪問に関する情報を使用して、 [!DNL Adobe] サーバー。 </p> <p>最後の検索クリックに関する情報は、コンバージョンイベントがクリックまたはビュースルー（インプレッションによるコンバージョンだがクリックされていない）の結果かどうかを判断するのに役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>広告主のトップレベルドメイン（example.com など） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>状況に応じて変化しますが、通常は 50 ～ 150 バイトです </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：ev_sync_&#42;

（ev_sync_ax、ev_sync_bk、ev_sync_dd、ev_sync_fs、ev_sync_ix、ev_sync_nx、ev_sync_ox、ev_sync_pm、ev_sync_rc、ev_sync_tm、ev_sync_yh）

<table id="table_A05C02AB261946E0AABAD78259392D81"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>同期が実行された日付（yyyymmdd 形式） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>同期が実行された日付（yyyymmdd 形式） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>Adobe Advertisingサーファー ID をパートナーの広告交換と同期する、サードパーティの広告交換固有の Cookie。 この cookie は新規サーファーに対して作成され、有効期間が過ぎると同期要求が送信されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>8 文字 </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：everest_g_v2

<table id="table_04043292A43B41B69EAF17AF4E217C69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>ブラウザーおよびサーファー ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>1 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>ユーザーが最初にクライアントの広告をクリックした後に作成され、現在およびそれ以降のクリックをクライアントの Web サイトの他のイベントにマッピングするのに使用されます </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>～ 27 文字 </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：everest_session_v2

<table id="table_1A3AE4CA71304ADB943CB1F64BE695F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>セッション ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>ブラウザーが閉じられたとき </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>サードパーティブラウザーセッション cookie。1 つの cookie はすべてのアカウントに使用される </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>～ 16 文字 </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：ev_tm

<table id="table_6C4D9DCFA4BF4FB2BD445E027550955F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>Adobe Advertising DSP(Demand Side Platform) ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>2 年。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>everest_g_v2 cookie のサーファー ID に対応する DSP ID を保存するサードパーティ cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>～ 20 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>

## cookie 名：id_adcloud

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>保存される情報 </p> </td> 
   <td colname="col2"> <p>サーファー ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効期限 </p> </td> 
   <td colname="col2"> <p>91 日 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>用途 </p> </td> 
   <td colname="col2"> <p>この cookie はファーストパーティドメインに設定されますが、まだ使用されていません </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>場所 </p> </td> 
   <td colname="col2"> <p>広告主のトップレベルドメイン（example.com など） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>サイズ </p> </td> 
   <td colname="col2"> <p>16 バイト </p> </td> 
  </tr> 
 </tbody> 
</table>
