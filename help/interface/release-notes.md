---
description: 「顧客属性、Audiences、ユーザー管理といった、Experience Cloud サービスの最新の機能、リリースノートおよび既知の問題です。」
keywords: コアサービス
solution: Experience Cloud
title: '累積リリースノート '
uuid: fcff8cc6-e587-4bf2-9a75-261d4eabc7d4
feature: '"顧客属性"'
topic: 管理
role: Admin
level: Experienced
exl-id: b71d144c-a097-4cdb-9721-671519d38aff
source-git-commit: 31cfb3a85c255b72cbe5599aca09494c22fe4301
workflow-type: tm+mt
source-wordcount: '4224'
ht-degree: 88%

---

# 累積リリースノート

Experience Cloud中央インターフェイスコンポーネントの機能、リリースノートおよび既知の問題です。

ドキュメントの更新のリストについては、[Experience Cloud](doc-updates.md#concept_4C8983FCD23848A4B1E4C2D99ED82784) を参照してください。

すべてのソリューションを対象とするリリースノートについては、[Experience Cloud リリースノート](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ja)を参照してください。

## 2021年7月

統合検索が更新され、Journey Optimizer、オファー、Experience Leagueで利用できるようになりました。 以前は、この機能はExperience Platformユーザーのみが使用できました。

## 2021年6月

| 機能 | 日付 | 説明 |
| ------- | ------- | ------- |
| Adobe Federated ID のシングルサインオンサポート | 2021 年 6 月 17 日（PT） | Federated ID を使用すると、メールアドレスやパスワードを入力しなくても、Experience Cloud にログインできます。 この機能を使用するには、Experience CloudURLに`#/sso:@domain`を追加します。 <br>例えば、ドメイン `adobecustomer.com` を所有していて、Adobe Analytics にサインインしたい場合、URLは次のようになります。`https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`. |
| Experience League 検索 | 2021 年 6 月 1 日（PT） | Experience League ドキュメントの検索が改善されました。[Experience League](https://experienceleague.corp.adobe.com/docs/?lang=en) に移動し、「**[!UICONTROL 検索]**」フィールドを使用して、チュートリアル、ドキュメント、コースなどを検索します。 |

{style=&quot;table-layout:auto&quot;}

## 2021 年 5 月

| 機能 | 日付 | 説明 |
| ------- | ------- | ------- |
| Experience Cloud のヘッダーとナビゲーション | 2021 年 5 月 20 日（PT） | Adobe Experience Cloud のアップデートには、ヘッダーのライトテーマに対する変更が含まれます。ダークテーマに簡単に戻せる機能や、暗いテーマに簡単に切り替えて、Experience Cloud ヘッダー内のユーザーアバターから追加の環境設定を制御できるリンクが追加されました。Experience Cloud のすべてのアプリケーションがテーマの設定をサポートしているわけではありませんが、この機能により、今後のテーマのサポートが可能になります。 |
| Experience Cloud のグローバル検索 | 2021 年 5 月 20 日（PT） | このリリースでは、Experience Cloud のグローバル検索で、[Experience League](https://experienceleague.adobe.com/?lang=ja#home) のドキュメント、コース、チュートリアルを検索できます。（現在、グローバル検索は、Experience Platform ユーザーのみが使用できます。[!UICONTROL Platform] のグローバル検索を使用すると、セグメント、データセット、スキーマなど、Experience Cloud 内のあらゆるビジネスオブジェクトを検索できます。） |
| Experience Cloud の言語設定 | 2021 年 5 月 20 日（PT） | この更新には、Experience Cloud の[環境設定](https://experience.adobe.com/preferences)で優先言語を設定する機能が含まれます。 |

{style=&quot;table-layout:auto&quot;}

## 2020 年 8 月

| 機能 | 説明 |
| -----------| ---------- |
| 管理ツール — ポリシー | このページには、組織内の Experience Cloud ポリシーの完全なリストが表示されます。製品、インスタンス、ユーザー、デベロッパーに関する情報を提供します。検索、並べ替え、フィルタリングによるポリシーリストのカスタム表示が可能です。詳しくは、[Experience Cloud 管理ツール](admin-tool-experience-cloud.md)のヘルプを参照してください。 |

{style=&quot;table-layout:auto&quot;}

## 2020 年 4 月

* Experience Cloud [!UICONTROL フィード]ページは非推奨になりました。（EXC-8505）
* 新しいブランディング要素を反映するよう、Experience Cloud のログインページが更新されました。（EXC-10747）

## 2020 年 2 月

| 機能 | 説明 |
| -----------| ---------- |
| 管理ツール - ユーザーの詳細を表示 | 管理者は、新しい管理ツールで、すべての Experience Cloud ユーザーとその詳細に関する、並べ替え可能でフィルタリング可能なリストを表示できます。ユーザーの詳細には、ユーザーの製品アクセス、ロール、最終アクセス日が含まれます。詳しくは、[Experience Cloud 管理ツール](admin-tool-experience-cloud.md)のヘルプを参照してください。 |

{style=&quot;table-layout:auto&quot;}

**修正点**

* **顧客属性：**&#x200B;顧客属性 UI に、Target で同期されたプロファイルの追加のステータスが表示されるようになりました。（MCUI-10231）
* **Triggers コアサービス：**&#x200B;あまり使用されないので、離脱タイプのトリガーを作成する際の傾向スコア「30 日以内に戻る可能性」が削除されました。（MCUI-10056）

## 2020 年 1 月

* フィードページは2019年12月に廃止されました。 製品内の廃止のお知らせを探してください。（MCUI-10039）

## 2019 年 8 月

* Experience Cloud ログイン中に一部のユーザーがログアウトされる問題を修正しました。（MCUI-6908）
* Experience Cloud ログイン機能のパフォーマンスを向上させ、待ち時間を短縮できるよう改善しました。（MCUI-6854、MCUI-6869、MCUI-6883）
* インターフェイスの外観を更新しました。（MCUI-6861、MCUI-6911、MCUI-6862）
* Experience Cloud の [!UICONTROL Triggers] で、[!UICONTROL トリガー]定義の _Like_ 句が正常に動作しない問題を修正しました。（MCUI-6611）

## 2019 年 4 月

* アプリを切り替えるメニューに Marketo が追加され、ブランディングが Experience Cloud に更新されました。（MCUI-6529）
* Experience Cloud ホームが更新され、フィードおよび管理ページへのリンクが含まれるようになりました。（MCUI-6682）
* [!UICONTROL トリガー]の定義の問題が修正され、「like」条件を正しく使用できるようになりました。（MCUI-6611）
* 顧客属性が改善され、サブスクリプション設定が適切にログに記録されるようになりました。（MCUI-6519）

## リリース 19.1.1 - 2019 年 1 月 17 日（PT）

**注意：** 2019 年 3 月から、Experience Cloud インターフェイスで Internet Explorer 11 がサポートされなくなります。

* ヘルプ検索で結果が表示されない問題を修正しました。（MCUI-1670）
* Triggers における eVar 管理の問題を修正し、改善しました。（MCUI-6400）

## リリース 16.5.1 - 2016 年 5 月 26 日（PT） {#section_3785F182BC13493F84903CA69EB6D0A8}

**機能および改善点**

<table id="table_ABBCE1A66F534059BD728BC2B9AEFA80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Admin Console で事前に構成されている製品設定 </p> </td> 
   <td colname="col2"> <p>Experience Cloudの顧客管理者は、事前に作成され、AnalyticsおよびDynamic Tag Managementのデフォルトの権限グループにマッピングされた製品設定を使用できます。 </p> <p>この最適化は、新しくプロビジョニングされた組織で利用でき、Admin Console でユーザーを管理するために組織が必要とする時間を削減します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィードフィードの強化 </p> </td> 
   <td colname="col2"> <p> Experience Cloudフィードで投稿を作成する際、宛先行は、デフォルトで組織を使用する代わりに、現在アクティブなトピックを使用するようになりました。</p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* Assets on Demand から Experience Cloud Feed に共有されたアセットで、サムネールが表示されなかった問題を修正しました。（MAC-29955）

## リリース 16.2 - 2016 年 2 月 18 日（PT） {#section_D9610373116C4D77A38F67815C725EA3}

<table id="table_C9B288CF42034F329C3C72D95D22E515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Assets の機能向上 </p> </td> 
   <td colname="col2"> <p>Experience Cloud Assets では、1 つの場所からデジタルアセットを保存、共有、同期できます。Experience Cloudアセットは、<span class="keyword"> Adobe Experience Manager</span> (AEM)の機能の一部を使用します。 </p> <p><a href="experience-cloud-assets.md#concept_DDA5224C907D4A4F817D795DA0ED64D0" format="dita" scope="local">Experience Cloud</a> を参照してください。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アカウントのリンク機能の改善 </p> </td> 
   <td colname="col2"> <p>ソリューションアカウントを Experience Cloud（Adobe ID）にリンクする方法が改善されました。この新しいワークフローでは、組織に関連付けられたユーザーのアカウントがすべて検出され、リンクするアカウントを選択できます。また、アカウントのリンク操作を効率化し、組織を管理ページにアクセスして手動でアカウントをリンクする必要がなくなりました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* Analytics でリンクと SSO を実行できなかった問題を修正しました。この問題が発生すると、「注意：エラーメッセージ：ERROR IMS SSO が失敗しました。リンクされた会社が見つかりません。」というメッセージが表示されていました。

**既知の問題**

**[!UICONTROL Experience Cloud]**／**[!UICONTROL Activation]** で Dynamic Tag Management にアクセスすると、Dynamic Tag Management アカウントが Experience Cloud（Adobe ID）にリンクされず、Dynamic Tag Management にログインできません。この問題を回避するには、ブラウザーの新しいタブで `dtm.adobe.com` に直接アクセスしてください。

## リリース 16.1 - 2016 年 1 月 21 日（PT） {#section_33B3F7DF6CA347E3AA93801BAC6232CE}

<table id="table_4223658257DA41C999AC710A10D26771"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> オーディエンスライブラリのメッセージ </td> 
   <td colname="col2"> <p> オーディエンスライブラリを改善し、ーディエンスの構築時またはタイムアウトの発生時に、役立つメッセージを表示するようにしました。 </p> <p>例えば、5 つを超えるルールを追加すると、許可されたルールの最大数を超えたことを示すメッセージが表示されます。（MAC-27376、MAC-27375） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Microsoft®は、Internet Explorer 8、9、および10の[サポートを終了](https://www.microsoft.com/ja-jp/WindowsForBusiness/End-of-IE-support)します。 そのため、今後アドビでは、Internet Explorer のこれらのバージョンに対して報告された問題は修正しません。

## リリース 15.10 - 2015 年 10 月 14 日（PT） {#section_68123833D3634BD3A473C12862BF9606}

**既知の問題**

* Experience Cloud 経由の SSO で Analytics にアクセスすると、Report Builder にログインできません。この問題は、従来の Analytics 資格情報を使用するお客様には影響しません。
* Analytics の「レポートへのリンク」機能に関する既知の問題です。お客様が Experience Cloud 経由で Analytics にログインし、レポートを共有しようとすると、SSO ではないログインページに誘導されます。

## リリース 15.9 - 2015 年 9 月 10 日（PT） {#section_BCCE3E7DF62A4FF5A57B9C8FE2A5F37B}

* 顧客属性データをアップロードする際に、Audience Manager API で断続的なタイムアウトが発生するパフォーマンスの問題を修正しました。（MAC-26305）
* 200 個の顧客属性を追加できなかった問題を修正しました。（MAC-26188）
* オーディエンスライブラリで、オーディエンス共有が Analytics でセグメント化できなかった問題を修正しました。この問題が原因で、「データを収集中」（0 オーディエンス）と表示されていました。この問題を避けるために、セグメントあたりのオーディエンスメンバーが 50,000 人未満になるようにセグメントサイズを維持することをお勧めします。（MAC-25788）
* 顧客属性のスキーマを編集ページで表示名を変更すると Content Aware（500）エラーが発生していた問題を修正しました。（MAC-25589、AN-103834）

## リリース 15.7 - 2015 年 7 月 22 日（PT） {#section_2683A152176944E48EF6C943892975B7}

* スキーマを表示 / 編集ページ（顧客属性）で指定された属性の説明が Analytics レポートで更新されなかった問題を修正しました。（MAC-25985）
* アップロードしたアセットのサムネールが表示されない問題を修正しました。（MAC-25863）
* Reports &amp; Analytics で作成された新しいセグメントが Experience Cloud Audiences で使用できなかった問題を修正しました。（MAC-25817）
* 訪問者 ID サービスを使用する際に、Analytics からオーディエンスを共有できなかった問題を修正しました。（MAC-25788、MAC-25747）
* 顧客属性でのマルチバイト文字のサポートが追加されました。（MAC-25552）

**既知の問題**

既知の問題によって、Audience Manager のアカウントが重複して自動生成され、ユーザーの Experience Cloud ID に自動的にリンクされることがあります。この問題は、アカウントをリンクする前に Audience Manager にアクセスしようとすると発生します。Audience Manager にアクセスする前に、Audience Manager アカウントを Experience Cloud にリンクすることをお勧めします。（MAC-25640）

## リリース 15.6.1 - 2015 年 6 月 11 日（PT） {#section_AD2019F8D2F84C9EB2B0533FAACF7043}

情報がありません。

## リリース 15.5.1 - 2015 年 5 月 13 日（PT） {#section_EF197410964E40D294D0D8024738CFBA}

<table id="table_14E7B35E06C84A258A21D09691B58354"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>左側のナビゲーションメニューが更新、整理され、すべてのコアサービスとソリューションにアクセスできるようになりました。重要な変更点は次のとおりです。 </p> 
    <ul id="ul_5BEBAB86B9234A239C4E2DAF8826D8E3"> 
     <li id="li_7FA9F64CE69144B8A8A92746BF40E5A1">「<span class="term">オーディエンスライブラリ</span>」メニューと「<span class="term">顧客属性</span>」メニューの選択は、<span class="term">Audiences</span> の下に移動されました。 </li> 
     <li id="li_95D62A43AE6243DBB2A65EDB830D05C4"><span class="term">Exchange</span> へのリンクは、ヘルプドロップダウンメニューから左側のナビゲーションパネルに移動されました。 </li> 
     <li id="li_0443FD50C78446CD8AA27A4F272CAD31"> <span class="term">ソリューション</span>は削除されました。ナビゲーションパネルの下側から、すべてのソリューションを起動できます。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

* 一部の顧客の顧客属性を同期できなかった問題を修正しました。
* [Adobe Target 製品ドキュメント](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)ページが日本語で表示されなかった問題を修正しました。
* [!DNL Creative Cloud] と [!DNL Experience Cloud] の間のコメントで日本語のテキストが使用できなかった問題を修正しました。

## リリース 15.4.1 - 2015 年 4 月 8 日（PT） {#section_75634120CC934B3381EDEA7F6F976F0A}

<table id="table_3A6FBAE36558425A803B078150862C92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>管理機能の強化： </p> 
    <ul id="ul_7D5FCBEFA262435D865CA1018BFB792E"> 
     <li id="li_6E98974CCB094ABBAB57C51ED56C3F00"> <span class="wintitle">Admin Console</span> </li> 
     <li id="li_8CDAB6301FD44C3999EE4EEB1A0A2FD6">エンタープライズとFederated IDのサポート </li> 
    </ul> </td> 
   <td colname="col2"> <p>ユーザーおよびグループ管理機能は、Admin Console に移行されました。次の手順でアクセスするようになりました。 </p> <p> <span class="uicontrol"> Experience Cloud</span>／<span class="uicontrol">管理</span>／<span class="uicontrol">Admin Console を起動</span></p> <p> また、Enterprise ID および Federated ID のサポートが追加されました。Enterprise ID、Federated ID および Adobe ID を全社で使用できます。例えば、他のアドビ製品やサービスを使用する可能性のあるユーザーには Adobe ID を使用します。アカウントを厳密に管理したいユーザーには、Enterprise ID または Federated ID を使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* [!DNL Experience Cloud] と [!DNL Media Optimizer] の間でシングルサインオンができなかった問題を修正しました。

**既知の問題**

* Dynamic Tag Management 組織と Experience Cloud のリンクおよびリンク解除が、新しく作成した Experience Cloud 組織で機能しません。Adobeは、5月のリリースでこの問題を修正し、正常な機能を復元するための作業を進めています。 Experience Cloud を使用して Dynamic Tag Management へのシングルサインオンで問題が発生した場合は、[!DNL dtm.adobe.com] での従来のログインを使用してください。
* 既知の問題により、リンクされた Analytics アカウントによって所有されていないレポートスイートをオーディエンス共有できません。現在、改善に取り組んでいます。

## リリース 15.3.2 - 2015 年 3 月 19 日（PT） {#section_07760FD9CA43497FA8BDCCA990A24BFD}

<table id="table_54025DBE2D094FF1BE837BA60816C6DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>顧客属性 </p> </td> 
   <td colname="col2"> <p>エンタープライズ顧客データを顧客関係管理(CRM)データベースに取り込む場合は、そのデータをExperience Cloudの顧客属性データソースにアップロードできます。 データをアップロードした後、Analytics で<span class="uicontrol">訪問者プロファイル</span>／<span class="uicontrol">顧客属性</span>レポートを実行できます。 </p> <p>アップロードしたデータを <span class="keyword">Adobe Target</span> でオーディエンスセグメントとして使用することもできます。 </p> <p><a href="attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1" format="dita" scope="local">顧客属性</a>製品ドキュメントを参照してください。 </p> <p> コアサービス用ソリューションの最新化については、<a href="core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">コアサービスのソリューションの有効化</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## リリース 15.3.1 - 2015 年 3 月 4 日（PT） {#section_57CB69C044DD47BDBC1A1BEC38957551}

<table id="table_EB3FFBA2DF904546A5185EC9A63BBA98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>グループマッピング </p> </td> 
   <td colname="col2"> <p>グループ管理ページは、グループの作成、グループへのユーザーの追加、Experience Cloud ソリューションでの権限の適用をおこなえる管理インターフェイスとして再設計されました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1 対多のマッピング </p> </td> 
   <td colname="col2"> <p>Experience Cloud のソリューションアカウントをリンクする際に、ソリューションおよび組織が複数ある場合、複数の製品およびサービスを 1 つの組織にマッピングできるようになりました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation </p> </td> 
   <td colname="col2"> <p> <a href="activation.md#concept_EE756B6B0A0643DAB8CA3A00E665406C" format="dita" scope="local">Activation</a> が <span class="keyword">Experience Cloud</span> の左側のナビゲーションに表示されるようになりました。<span class="wintitle"> </span> Activationは、現在はDynamic Tag Managementテクノロジーで構成さ <span class="keyword"> </span> れるExperience Cloudサービスで、選択するとこの機能に移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ドキュメントの更新 - コアサービス </p> </td> 
   <td colname="col2"> <p>コアサービスの実装に役立つトピックとして、<a href="core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">ソリューションのコアサービスへの対応</a>を追加しました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## リリース 15.2.1 - 2015 年 2 月 19 日（PT） {#section_BC694D5AE16A4E16B44B353ED67947F3}

修正点：

* アカウントプロビジョニングのためのユーザー電子メール招待ワークフローを改善しました。
* アセットフォルダーで、[!DNL Experience Cloud] および [!DNL Adobe Campaign] のアセットを同一のフォルダー階層に表示できなかった問題を修正しました。
* 非有効化された [!DNL Target] アクティビティの一部であるオーディエンスを削除できなかった問題を修正しました。
* [!UICONTROL 新しいオーディエンスを作成]ページの「[!UICONTROL ルール]」の下に追加（プラス）アイコンが表示されなかった問題を修正しました。
* Experience Cloud インターフェイスが強化され、Internet Explorer 9 をサポートするようになりました。

## リリース 15.1.1 - 2015 年 1 月 15 日（PT） {#section_F1A352E928AF432E94CC0A289C345184}

[!DNL Adobe Experience Cloud] のコラボレーションおよび共有インターフェイスの新機能および修正点です。

<table id="table_AD0A8CA760E64227BB04BA6B0E425E80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>読み取り専用アクセス権 </p> </td> 
   <td colname="col2"> <p>管理者が管理者以外のユーザーに読み取り専用アクセス権を付与できるようになりました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* PNG ファイルをカード上でレンダリングできない問題を修正しました。
* ファイルをドラッグ＆ドロップ操作で Experience Cloud Assets にアップロードするときの問題を修正しました。

**既知の問題**

* ユーザーがボードで PowerPoint ファイルを共有できません。
* ユーザー管理でおこなったグループおよび資格の変更が新規ログイン後にしか有効になりません。
* 大きなファイルを Experience Cloud アセットにアップロードするときに問題が生じる場合があります。
* ユーザーが Media Manager から取り出した Experience Cloud カードにリンクがない場合があります。
* 管理者権限のあるユーザーが Experience Cloud への参加の招待を受け入れた後に、アカウントのリンクに関して問題が生じる場合があります。
* 複数のユーザーが同時に使用すると Experience Cloud インターフェイスのパフォーマンスが低下する可能性があります。
* 古くなったアセットに関するエラー通知を受信する代わりに、そのアセットを削除できてしまう場合があります。
* 同じ Adobe ID で 2 つのブラウザーに同時にログインすると問題が生じる場合があります。
* Creative Cloud ユーザーを削除した後、Creative Cloud ユーザーを共有フォルダーに再び追加できない場合があります。
* フォルダーを Experience Cloud から Creative Cloud へ共有するときにユーザーへの通知が遅れる場合があります。
* フォルダーを Experience Cloud と Creative Cloud の間で共有するときに問題が生じる場合があります。
* 共有オーディエンスを有効にした後、Analytics レポートスイート内でのオーディエンスの作成がうまくいかなくなることがあります。
* ボードへのアセットのアップロードで問題が発生する場合があります。

## リリース 14.11.1 - 2014 年 11 月 13 日（PT） {#section_A6CF1D4F27B9496892A89C983EB39102}

既知の問題:

* 古くなったアセットに関するエラー通知を受信する代わりに、そのアセットを削除できてしまう場合があります。
* 一部の [!DNL .png] ファイルは、カードにレンダリングできません。
* ボードへのアセットのアップロードで問題が発生する場合があります。
* ユーザー管理でおこなったグループおよび権限付与の変更は、新しくログインした後でのみ有効になります。
* 管理者がアカウントの設定でおこなった変更を確認するには、ログアウトしてから再度ログインする必要があります。
* ユーザーがボードで PowerPoint ファイルを共有できません。
* 多くのユーザーが同時に使用すると [!DNL Experience Cloud] インターフェイスのパフォーマンスが低下する可能性があります。
* Adobe Experience Manager から Creative Cloud への同期が機能していません。

## リリース 14.10.1 - 2014 年 10 月 16 日（PT） {#section_E3A0F4423B814707AA3745E083500835}

[!DNL Adobe Experience Cloud] のコラボレーションおよび共有インターフェイスの新機能および修正点です。

<table id="table_7C1ACE8108D54782AE128ACD35069DF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ユーザー権限を編集 </p> </td> 
   <td colname="col2"> <p>ボードの所有者は、特定のボードのユーザー権限を編集できるようになりました。 </p> <p> 
     <ol id="ol_B12251C510744538AF9BCE60ACB04016"> 
      <li id="li_87B3EDE9542B47CEBE0BE7F2D1DE844D">ボード上で、「<span class="uicontrol">設定</span>」を選択します。 </li> 
      <li id="li_0F4786B0E1E743069D082E7DC488A031">各所有者の横の「<span class="uicontrol">所有者</span>」、「<span class="uicontrol">閲覧者</span>」または「<span class="uicontrol">エディター</span>」を指定します。 </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* PDF からカードを作成したり、ボードにカードを共有すると、エラーメッセージが返されていた問題を修正しました。

**既知の問題**

* ボードへのアセットのアップロードで問題が発生する場合があります。
* 一部の [!DNL .png] ファイルは、カードにレンダリングできません。
* ユーザー管理でおこなったグループおよび権限付与の変更は、新しくログインした後でのみ有効になります。
* PDF からカードを作成してボードに共有することができない場合があります。
* 古くなったアセットに関するエラー通知を受信する代わりに、そのアセットを削除できてしまう場合があります。
* ユーザーがボードで PowerPoint ファイルを共有できません。
* 多くのユーザーが同時に使用すると [!DNL Experience Cloud] インターフェイスのパフォーマンスが低下する可能性があります。
* [!DNL Search&Promote] リンクが[!UICONTROL 組織と製品へのアクセス]ページから利用できません。

## リリース 14.9.1 - 2014 年 9 月 18 日（PT） {#section_20F156A9CC2F4FC59C4970075C181D3A}

**修正点および改善点**

* [!DNL experience.adobe.com] に移動した場合のログイン操作が、アドビの Creative Cloud ログインと一致するようになりました。
* 組織を管理ページ上のリンク操作（招待を受け取った後）が各ソリューションで共通になりました。

**既知の問題**

* ユーザー管理でおこなったグループおよび権限付与の変更は、新しくログインした後でのみ有効になります。
* PDFからカードを作成してボードに共有できない場合があります。
* ボードへのアセットのアップロードで問題が発生する場合があります。
* 古くなったアセットに関するエラー通知を受信する代わりに、そのアセットを削除できてしまう場合があります。
* ユーザーがボードで PowerPoint ファイルを共有できません。
* 一部の [!DNL .png] ファイルは、カードにレンダリングできません。
* 多くのユーザーが同時に使用すると [!DNL Experience Cloud] インターフェイスのパフォーマンスが低下する可能性があります。
* [!DNL Search&Promote] リンクが[!UICONTROL 組織と製品へのアクセス]ページから利用できません。
* [!DNL Creative Cloud] でコンテンツが共有されていない場合、[!DNL Experience Cloud] コンテンツが一部のユーザーのフォルダーから削除されることがあります。

## リリース 14.8.1 - 2014 年 8 月 21 日（PT） {#section_03BF00F6A95A490C91BCC0A1988FA7AA}

[!DNL Adobe Experience Cloud] のコラボレーションおよび共有インターフェイスの新機能および修正点です。

<table id="table_1E7DBEB5E83B4E4285B6FD1D718CD16D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>左側のナビゲーションから <span class="keyword">Adobe Mobile Services</span> にアクセスできるようになりました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**既知の問題**

* ユーザー管理でおこなったグループおよび権限付与の変更は、新しくログインした後でのみ有効になります。
* PDF からカードを作成してボードに共有することができない場合があります。
* ボードへのアセットのアップロードで問題が発生する場合があります。
* [!DNL Target] から [!DNL Experience Cloud] にログインできない場合があります。
* Audience Manager で、[!DNL Experience Cloud] にログインできない場合があります。
* 古くなったアセットに関するエラー通知を受信する代わりに、そのアセットを削除できてしまう場合があります。
* [!DNL Experience Cloud] から削除されたファイルが [!DNL Digital Asset Management] から削除されません。
* ユーザーがボードで PowerPoint ファイルを共有できません。
* 一部の [!DNL .png] ファイルは、カードにレンダリングできません。
* 多くのユーザーが同時に使用すると [!DNL Experience Cloud] インターフェイスのパフォーマンスが低下する可能性があります。
* [!DNL Search&Promote] リンクが[!UICONTROL 組織と製品へのアクセス]ページから利用できません。
* [!DNL Creative Cloud] でコンテンツが共有されていない場合、[!DNL Experience Cloud] コンテンツが一部のユーザーのフォルダーから削除されることがあります。

## リリース 14.7.1 - 2014 年 7 月 24 日（PT） {#section_B22D4F830756463DB27BB4D508D9ADD5}

[!DNL Adobe Experience Cloud] のコラボレーションおよび共有インターフェイスの新機能および修正点です。

**既知の問題**

* [!DNL Experience Cloud] から削除されたファイルが [!DNL Digital Asset Management] から削除されません。
* 一部の [!UICONTROL Exchange] ユーザーは、コメント内のユーザー名を検索して、名前の代わりに長い文字列の ID にすることができます。
* 一部の [!DNL .png] ファイルは、カードにレンダリングできません。
* ファイルをアップロードした方が、ドラッグ＆ドロップよりも多くのファイルタイプを使用できます。最も良い結果を得るには、[!UICONTROL Assets] を使用してアップロードしてください。
* [!DNL Search&Promote] リンクが[!UICONTROL 組織と製品へのアクセス]ページから利用できません。
* [!DNL Exchange] ユーザーは、エクスペリエンスを改善するために Cookie を消去する必要があります。
* 多くのユーザーが同時に使用すると、[!DNL Experience Cloud] インターフェイスのパフォーマンスが遅くなる可能性があった問題を修正しました。
* [!DNL Experience Cloud] でコンテンツが共有されていない場合、[!DNL Creative Cloud] コンテンツが一部のユーザーのフォルダーから削除されることがあります。
* 無操作状態が 15 分間続くとログアウトします。また、ある場所でログアウトすると、[!DNL Experience Cloud]からログアウトします。
* 一部のユーザーは、Audience Manager アカウントを [!DNL Experience Cloud] にリンクできない可能性があります。
* [!UICONTROL Exchange] ユーザーは、言語セレクターで英語のみ表示できます。

**修正点**

なし

## リリース 14.6.1 - 2014 年 6 月 19 日（PT） {#marketing_cloud_interface}

[!DNL Adobe Experience Cloud] のコラボレーションおよび共有インターフェイスの新機能および修正点です。

**改善点**

<table id="table_C9BD63436BF0414B97B8D07387D1993B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>  オーディエンスの「<span class="wintitle">保存</span>」ボタン </p> </td> 
   <td colname="col2"> <p>オーディエンスを作成する際、<span class="wintitle">新しいオーディエンスを作成</span>ページの必須フィールドがすべて入力されるまで「<span class="wintitle">保存</span>」ボタンは有効になりません。 
      
     <!--MAC-19712 --></p> </td> 
  </tr> 
 </tbody> 
</table>

**既知の問題**

* [!DNL Experience Cloud] から削除されたファイルが [!DNL Digital Asset Management] から削除されません。
* ファイルをアップロードした方が、ドラッグ＆ドロップよりも多くのファイルタイプを使用できます。最も良い結果を得るには、Assets を使用してアップロードしてください。
* [!DNL Search&Promote] リンクが[!UICONTROL 組織と製品へのアクセス]ページから利用できません。
* [!DNL Analytics] からトレンドレポートに適用したフィルターが、[!DNL Experience Cloud] のカードに適用されません。
* 一部のユーザーは、オーディエンス管理アカウントを [!DNL Experience Cloud] アカウントにリンクできません。
* 無操作状態が 15 分間続くとログアウトします。また、ある場所でログアウトすると、Experience Cloudからログアウトします。
* 一部の Exchange ユーザーは、コメント内のユーザー名を検索して、名前の代わりに長い文字列の ID にすることができます。

**修正点**

* アプリケーションへのビデオのアップロードができない問題を修正しました。

## リリース 14.5.1 - 2014 年 5 月 22 日（PT） {#section_7E22B2CB3ABA4D6EAED8CA8EFDE5433E}

<table id="table_4E4B34EEE3D94D78BA1A1FBC62950559"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Exchange </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span>／<span class="uicontrol">ヘルプ</span>／<span class="uicontrol">Exchange</span></p> <p><span class="keyword">Experience Cloud</span> <span class="wintitle">Exchange</span> にアクセスすると、各種の連携ツールの検索、参照、選択、支払いおよびダウンロードをおこなえます。 </p> <p>Data Connectors、Adobeのコア製品のカスタム設定、サードパーティアプリケーション、レポート、<span class="keyword">Experience Cloud</span>カードなどが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Audiences </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud </span>／<span class="uicontrol"> Audiences</span></p> <p> <span class="wintitle">Audiences</span> では、セグメントの操作と同様に、オーディエンスを作成、編集および管理できます。例えば、Reports &amp; Analyticsでセグメントを作成し、<span class="wintitle">Experience Cloud</span><span class="wintitle">オーディエンス</span>と共有できます。 共有すると、オーディエンスを <span class="keyword">Adobe Target</span> でキャンペーンアクティビティに使用したり、Adobe Audience Manager でセグメント化に使用したりできます。 </p> <p> <p>注意：Targetでの有効化をリクエストするには、 <a href="https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES" format="http" scope="external"> https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES</a>にアクセスしてください。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p><span class="keyword">Experience Cloud</span> カードでメンションされたユーザーには、そのカードに対する権限が付与されるようになりました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>新しいAdobeユーザーは、Scene7アカウントをAdobe IDおよびチームメンバーにリンクできます。 管理者は、Scene7 アカウントからユーザーのリンクを解除することもできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アセットの同期 </p> </td> 
   <td colname="col2"> <p> アセット内のアセットをExperience ManagerやCreative Cloudと共有できます。 これらのアセットに対する変更は、Experience CloudとCreative Cloudのアセットの共有コピーに反映されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* [!DNL Experience Cloud] が [!DNL Adobe Target] にリンクされなかった問題を修正しました。この問題は、[!DNL Adobe Target] ログインが複数の [!DNL Target] サーバーで使用できる場合に発生していました。
* [!DNL Experience Cloud] でユーザーが作成された場合、[!DNL Adobe Media Optimizer] でユーザーが自動作成されなかった問題を修正しました。
* 新しいユーザーを追加するためのコンボボックスのオプションが、入力中、一時的に消えていた問題を修正しました。
* アセットカード表示のコメントリンクを選択できませんでした。
* アセットにカスタムタグを追加した後、その他のメタデータの変更が保持されなかった問題を修正しました。
* アセットの画像の削除で、その画像が Adobe Target Essentials で使用されていても、警告が表示されない問題を修正しました。
* 多くのユーザーが同時に使用すると、[!UICONTROL Experience Cloud] インターフェイスのパフォーマンスが遅くなっていた問題を修正しました。
* [!UICONTROL Experience Cloud Assets] での画像の削除で、その画像が [!DNL Adobe Target Essentials] で使用されていても警告が表示されていなかった問題を修正しました。
* 「**[!UICONTROL このアカウントを記憶する]**」が選択されていない場合、ユーザーが 15 分後にログアウトされていた問題を修正しました。
* すべての権限および権限付与の変更を有効にするために、ユーザーがログアウトしてからログインし直す必要があった問題を修正しました。
* [!DNL Experience Cloud] へのログインに、1 秒以上かかっていた問題を修正しました。
* 一部のユーザーで、[!DNL Experience Cloud] からファイルを削除しても、[!DNL Digital Asset Management] で同期されていなかった問題を修正しました。
* ブラウザーの無操作状態が 15 分間続いただけで、ユーザーがログアウトされていた問題を修正しました。
* ユーザーがボードで PowerPoint ファイルを共有できなかった問題を修正しました。
* 一部のユーザーで、Internet Explorer 10での表示レイアウトが低下していました。

## リリース 14.4.1 - 2014 年 4 月 22 日（PT） {#section_E2A699764E744D2E8D418E9A3D40AF6B}

<table id="table_D95C0DC64F2A4B47BAC83E504CFD6825"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ヘルプトピックからカードを作成 </p> </td> 
   <td colname="col2"> <p>Adobe Experience Cloud に共有機能を有効にした後、ブラウザーのブックマークツールバーで、マイクロサイト URL からヘルプページを共有できるようになりました。 </p> <p> <b>ヘルプトピックを共有するには</b> </p> 
    <ol id="ol_F94B816121494B0FA16CC07B0E96AED8"> 
     <li id="li_F47187D4B5FE46D3A51D257DD569B4D6"> <p><span class="keyword">Experience Cloud</span>で、「<span class="uicontrol">管理</span>」を選択します。 </p> </li> 
     <li id="li_94EF58E7A4974B63951E14F72A710183"> <p>「<span class="uicontrol">Adobe Experience Cloud で共有</span>」ボタンをブックマークツールバーにドラッグします。 </p> </li> 
     <li id="li_69EEC4F25D8F4AD7AA106A10B7F50FF6"> <p>ヘルプページに移動して（またはこのページにとどまったまま）、ブラウザーのブックマークツールバーで「 <span class="uicontrol"> Adobe Experience Cloudで共有</span> 」を選択します。 </p> <p>この手順により、<span class="wintitle">Experience Cloud</span> で確認できるカードが作成されます。 </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* アセットにカスタムタグを追加した後、その他のメタデータの変更が保持されません。
* 削除したカードを表示から消すために、ユーザーがボードを更新する必要があります。
* 「**[!UICONTROL このアカウントを記憶する]**」が選択されていない場合、ユーザーは 15 分後にログアウトされます。
* [!DNL Analytics] ソリューションランディングページでフォーマットエラーが表示されます。
* すべての権限および権限付与の変更を有効にするには、ユーザーはログアウトしてからログインし直す必要があります。
* [!UICONTROL アセット]の画像の削除で、その画像が [!DNL Adobe Target Essentials] で使用されていても、警告が表示されません。
* アセットカード表示のコメントリンクは選択できません。
* 新しいユーザーを追加するためのコンボボックスのオプションが、入力中、一時的に消えます。
* [!DNL Experience Cloud] へのログインに、1 秒以上かかります。
* [!DNL Media Optimizer] から共有されたデータが [!DNL Experience Cloud] に正しく表示されなかった問題を修正しました。
* [!DNL Experience Cloud] でユーザーが作成された場合、Adobe [!DNL Media Optimizer] でユーザーが自動作成されなかった問題を修正しました。
* [!DNL Experience Cloud] ログインを複数の [!DNL Adobe Target] サーバーで使用できる場合、[!DNL Adobe Target] が [!DNL Target] にリンクできなかった問題を修正しました。
* 多くのユーザーが同時に使用すると、[!DNL Experience Cloud] インターフェイスのパフォーマンスが遅くなる可能性があった問題を修正しました。
* [!DNL Search&Promote] リンクを[!UICONTROL 組織と製品へのアクセス]ページから利用できなかった問題を修正しました。
* [!DNL Adobe Media Optimizer] シミュレーションカードが正しくレンダリングされない問題を修正しました。
* [!DNL Analytics] からトレンドレポートに適用したフィルターが、[!DNL Experience Cloud] のカードに適用されない問題を修正しました。
* Analytics からトレンドレポートに適用したフィルターが、Experience Cloud のカードに適用されない問題を修正しました。
* 一部の Excel または CSV ファイルは、ボードにアップロードできません。
* 一部のユーザーが、Audience Management アカウントを [!DNL Experience Cloud] にリンクできないことがあった問題を修正しました。
* 一部のユーザーは、[!DNL Analytics] で [!DNL Experience Cloud] セグメントを共有すると、エラーが発生することがあった問題を修正しました。
* 一部のユーザーで、[!UICONTROL アセットセレクター]のサブフォルダーを展開できない可能性があった問題を修正しました。
* 一部のユーザーが、[!DNL Experience Cloud] の AdLens ガジェットを共有できなかった問題を修正しました。

## リリース 14.3.1 - 2014 年 3 月 13 日（PT） {#section_5D142E3225E3477A84DC01B8197D39BC}

バージョン14.3.1は、速度、安定性、セキュリティに重点を置いたメンテナンスリリースです。 重要な新機能は含まれていません。

**修正点**

* アバター画像を削除する機能を追加しました。
* [!DNL Adobe Media Optimizer] アカウントのリンク解除を妨げていた問題を修正しました。

**既知の問題**

* Experience Cloud Assets での画像の削除で、その画像が Adobe Target Essentials で使用されていても警告が表示されません。
* [!DNL Analytics] からカードを更新すると、展開されたカードでグラフが空になることがあります。
* すべての権限および権限付与の変更を有効にするには、ユーザーはログアウトしてからログインし直す必要があります。
* *`Remember me`* が選択されていない場合、ユーザーは 15 分後にログアウトされます。
* [!DNL Analytics] ソリューションランディングページでフォーマットエラーが表示されます。
* アセットカード表示のコメントリンクは選択できません。
* 多くのユーザーが同時に使用すると、Experience Cloud インターフェイスのパフォーマンスが遅くなる可能性があります。
* [!DNL Adobe Target] ログインが複数の Target サーバーで使用できる場合、Experience Cloud は [!DNL Adobe Target] にリンクできません。
* Experience Cloud へのログインに、1 秒以上かかります。
* アセットにカスタムタグを追加した後、その他のメタデータの変更が保持されません。
* Experience Cloud でユーザーが作成された場合、[!DNL Adobe Media Optimizer] でユーザーが自動作成されなかった問題を修正しました。
* 新しいユーザーを追加するためのコンボボックスのオプションが、入力中、一時的に消えます。
* [!DNL Media Optimizer] から共有したデータが、Experience Cloud で誤って表示されます。
* Flickr 画像の共有に失敗します。
* [!DNL Analytics] からトレンドレポートに適用したフィルターが、Experience Cloud のカードに適用されません。
* ユーザー管理でおこなったグループおよび権限付与の変更は、新しくログインした後でのみ有効になります。
* [!DNL Search&Promote] リンクが「[!UICONTROL 組織と製品へのアクセス]」から利用できません。
* 削除したカードを表示から消すために、ユーザーがボードを更新する必要があります。
* 一部の Excel または CSV ファイルは、ボードにアップロードできません。
* [!DNL Adobe Media Optimizer] シミュレーションカードが正しくレンダリングされない問題を修正しました。
* 一部の PNG ファイルは、カードにレンダリングできません。
* ベータフィードバックを送信できません。

## リリース 14.2.1 - 2014 年 2 月 23 日（PT） {#section_5AD81B0737C843AFB4BE9C4420D70EB3}

<table id="table_DFAB002358C94A17A7F91DAB323A488F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 機能 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>oEmbed </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>データを更新 </p> </td> 
   <td colname="col2"> <p> 
     <!--MAC-18174-->データの更新が許可されていない場合、カードにあるグラフの<span class="uicontrol">データを更新</span>アイコンが非表示になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* 共有された [!DNL Analytics] レポートにセグメントフィルターを適用できない問題を修正しました。
* ソリューションアカウントがリンクされていない場合でも、ソリューションがリンクされているものとして [!UICONTROL Experience Cloud ソリューション]ページに表示される問題を修正しました。
* アジアの[!DNL Adobe Target]のお客様がリンク用ページの「**[!UICONTROL Experience Cloudを続行]**」ボタンを選択できない問題を修正しました。
* YouTube ビデオの共有ができない問題を修正しました。
