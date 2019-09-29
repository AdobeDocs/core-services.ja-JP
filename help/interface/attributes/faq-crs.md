---
description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
keywords: 顧客属性
seo-description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
seo-title: よくある質問、制限事項、ベストプラクティス
solution: Experience Cloud
title: よくある質問、制限事項、ベストプラクティス
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 08c2caa1e0e5ca5c487294e9ce33600dde9c9a1e

---


# よくある質問、制限事項、ベストプラクティス

Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。


## ベストプラクティスと制限事項 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

顧客属性を使用する際のガイダンスと制限事項

| 問題 | 説明 |
|--- |--- |
| 顧客属性サブスクリプションに関する制限事項 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |
| カスタム Analytics ID（s.visitorID） | 顧客 ID を設定するときに  s.visitorID を使用すると、Analytics でユーザーを特定しやすくなります。しかし、s.visitorID を使用して訪問者を特定する場合は、ID サービスを用いて Analytics データをエクスポートまたはインポートする統合機能を使用できません。<br>これには共有オーディエンス、Analytics for Target（A4T）、顧客属性などが該当しますが、これらに限定されません。<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
| Analytics での文字の長さの制限 | Analytics サブスクリプションの作成時には、アップロードするファイルのフィールド長が 255 文字以下になるように切り詰められます。 |

## 顧客属性に関する FAQ {#section_E47866EEA83348E09FE43CEC5E44C461}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 質問 </th> 
   <th colname="col2" class="entry"> 回答 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>顧客属性のアップロードステータスに関する通知を受け取ることはできますか。 </p> </td> 
   <td colname="col2"> <p>はい。<a href="../admin-getting-started/organizations.md#concept_0105453AD71847B8BFCAF4A40915F157" format="dita" scope="local">通知の管理</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 顧客データの使用を開始するために何をおこなう必要がありますか。 </p> </td> 
   <td colname="col2"> 
    <ol id="ol_1FACEF0990B6486B8DE86245D17695A8"> 
     <li id="li_F0C1542853684F8591FDC1B441D31A56"> <p>プロビジョニングを受けます。 </p> <p>既に <b>Analytics</b> ユーザーになっている場合は、そのユーザーを顧客属性用にアドビがプロビジョニングします。<b>Target</b> のみを使用していて、Analytics を所有していない場合は、コアサービス用のプロビジョニングをカスタマーケアに依頼する必要があります。 </p> </li> 
     <li id="li_444FEDEE4B7244F79BA847662F5B17CB"> <p>CRM チームに連絡します。Analytics や Experience Cloud 全体で使用すると興味深い結果が得られそうな顧客データの種類を見極めます。 </p> </li> 
     <li id="li_32D4AAF8C29748A78801A0E1BFB37AF5"> <p>コアサービスを実装します。 </p> <p>コアサービスの実装を最新化する手順については、<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">はじめに - コアサービス向けにソリューションを有効化</a>を参照してください（重要な情報については、顧客 ID の同期に関する節を参照してください）。 </p> </li> 
    </ol> <p> <b>注意：</b>コアサービスの実装に関する管理者向けの FAQ については、<a href="../admin-getting-started/faq.md#concept_13219B4E51784577B6FF78AAA203DE91" format="dita" scope="local">こちら</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用できる顧客属性はいくつありますか。 </p> </td> 
   <td colname="col2"> <p>数百の <span class="filepath">.csv</span> 列を顧客属性サービスにアップロードできます。ただし、サブスクリプションを設定して属性を選択する場合、所有するソリューションに応じて、次の制限が適用されます。 </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analytics Standard</b>：合計 3 件 </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium</b>：レポートスイートあたり 200 件 </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Target Standard：</b>5 件 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Target Premium：</b>200 件 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud ID サービスへの移行は必須ですか。 </p> </td> 
   <td colname="col2"> <p>移行が必要かどうかは、使用するソリューションによって異なります。 </p> <p> 
     <ul id="ul_9C473434B5DA4C6299AAB209DEDFCDE7"> 
      <li id="li_8BC10EB2825F4ADF8CA61F71D4994A28"> <b>Adobe Analytics</b>：強く推奨されます。 </li> 
      <li id="li_56F518E3F3DF4C93B6F7EF3B40ACC52F"> <b>Adobe Target</b>：必要です。 </li> 
     </ul> </p> <p>ID サービスを使用すると、リアルタイムオーディエンス、Target 最新化、Analytics 統合、ビデオハートビート追跡など、最新の Experience Cloud 機能を利用できる機会が広がります。 </p> <p>詳しくは、<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> コアサービス - ソリューションを有効にする方法</a>を参照してください。 </p> <p> <b>メモ</b>：The <span class="term"> Experience Cloud ID サービス</span>は、以前<span class="term"> Analytics 訪問者 ID サービス</span>と呼ばれていたサービスの実装を最新化したものです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>顧客属性機能と Adobe Audience Manager にはどのような関係がありますか。 </p> </td> 
   <td colname="col2"> <p>Audience Manager はデータを受信してオーディエンス識別を実行できますが、属性を履歴行動データに連結する分析機能を実行したり、Adobe Analytics で使用可能なレポート、分析およびセグメント化機能を提供したりすることはできません。People コアサービスは、ソリューション全体からのリッチデータを 1 つにまとめて、Experience Cloud 全体で使用する単一の ID に関連付けることができます。 </p> <p> Adobe Target の場合、顧客属性は、他のルールと統合してオーディエンスを構築できる個人属性として表示されます。People コアサービスで共有されるオーディエンスは、修正できない完全なオーディエンスです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Analytics のみ）</b>この機能と Analytics Premium で提供される機能にはどのような違いがありますか。 </p> </td> 
   <td colname="col2"> <p>以前は、顧客属性データと Analytics データの組み合わせに興味があっても、この機能を利用するには data workbench ツールに大きく依存する必要がありました。顧客属性では、顧客属性データをディメンションおよび指標として Reports &amp; Analytics、Ad Hoc Analysis および Report Builder に提供することで、この機能をより幅広く利用できるようになりました。Analytics Standard のユーザーは顧客属性にアクセスできますが、使用できる機能には制限があります。Analytics Premium のユーザーは、すべての機能を使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Target のみ）</b>これまで Target で扱っていない顧客のデータをプリロードまたはアップロードできますか。 </p> </td> 
   <td colname="col2"> <p> はい。訪問者が Target に対して最初のリクエストをすると、システムは、その訪問者に関して持っている既存の情報を顧客属性から取得し、ターゲティング用に使用します。 </p> <p> <p>注意：このデータの取得には、訪問者が最初に Target とやり取りしてから、最大で 20 分かかります。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Target のみ）</b>顧客属性データと共有オーディエンスデータを組み合わせて、スーパーオーディエンスを作成することはできますか。 </p> </td> 
   <td colname="col2"> <p>いいえ。共有オーディエンスデータは、完了したオーディエンスです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Target のみ）</b>顧客属性機能と Target の一括プロファイル API にはどのような違いがありますか。 </p> </td> 
   <td colname="col2"> <p> <a href="https://marketing.adobe.com/developer/documentation/test-target/r-profile-update" format="https" scope="external">一括プロファイル API</a> を使用すると、API を介して、Target プロファイルを個別または一括で直接更新できます。この機能は顧客属性に似ていますが、次のような大きな違いもあります。 </p> 
    <ul id="ul_5AAA4A8497C04F50A8AAA9F776BB868E"> 
     <li id="li_B20AEA397F3B4C86A1140CDA61ABD575">プロファイル API は REST API 呼び出しで、顧客属性は FTP を使用します。 </li> 
     <li id="li_7FBE428EF5D34B6AA09B6368E8210344">Target のプロファイル API は、Experience Cloud 全体ではなく、Target に対してのみデータを送信します。 </li> 
     <li id="li_CBB4D3FAF53944E0A066A4AD9F9C8760">顧客属性は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Target のみ）</b>顧客属性から Adobe Target にデータをアップロードすると、Target の訪問者プロファイルの有効期間が延びますか。 </p> </td> 
   <td colname="col2"> <p>はい。Adobe Target ヘルプの<a href="https://marketing.adobe.com/resources/help/en_US/target/ov/?f=c_visitor_profile_lifetime" format="https" scope="external">訪問者プロファイルの有効期間</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Target のみ）</b>訪問者が顧客 ID によって特定された後すぐ、顧客属性にアップロードされたデータをターゲットにできますか。 </p> </td> 
   <td colname="col2"> <p>はい。 </p> <p>mbox サードパーティ ID を含む Target へのサーバーコール時に、すべての顧客属性データを使用できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

