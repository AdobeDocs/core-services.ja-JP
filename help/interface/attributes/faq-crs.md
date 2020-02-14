---
description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
keywords: customer attributes
seo-description: Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。
seo-title: よくある質問、制限事項、ベストプラクティス
solution: Experience Cloud
title: よくある質問、制限事項、ベストプラクティス
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: e5bc3afea458d85421ab86ae87a65ebe4e88bb75

---


# よくある質問、制限事項、ベストプラクティス

Analytics と Target の顧客属性に関してよくある質問とベストプラクティスを紹介します。

## ベストプラクティスと制限事項 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

顧客属性を使用する際のガイダンスと制限事項

| 問題 | 説明 |
|--- |--- |
| 顧客属性サブスクリプションに関する制限事項 | Analytics Premium にアップグレードすると、追加の属性を使用できるようになるまでに 24 時間の遅延が生じます。この遅延の間に、属性サブスクリプションの上限に関連するエラーが発生することがあります。 |
| 同じデバイスでの複数のログイン | 顧客属性を使用して顧客プロファイルをデータソースにアップロードする場合、同じデバイス（つまり、同じExperience Cloud ID）を共有するユーザーに対しては、アドビでは推奨しています。 そうすると、デバイス上で存続するECIDサービスが、同じExperience Cloud IDで複数のユーザーをリンクする原因となり、予期しない結果が生じる場合がありま [!DNL Target]す。 **** 注意：Mobileの場合、ECIDはMobileアプリのインストール後に永久的に使用されます。新しいECIDを生成するには、アプリを再インストールする必要があります。 Webの場合、ブラウザーのCookieがクリアされた後に新しいECIDが生成されます。 |
| 毎日の頻度のアップロード制限 | 顧客属性の更新は、1日に1回のみ行うことをお勧めします。 同じプロファイルのセットに対して別の顧客プロファイルデータファイルをアップロードするには、少なくとも24時間待つ必要があります。 |
| Custom Analytics ID (`s.visitorID`) | `s.visitorID` を使用して顧客 ID を設定すると、Analytics でユーザーを特定しやすくなります。ただし、IDサービスを使用してAnalyticsデータを書き出したり読み込んだりする統合は、訪問者が `s.visitorID.`<br>This includes、Analytics for Target(A4T)および顧客属性を使用して識別された場合は機能しません。<br>これらの統合機能では、カスタム Analytics ID の設定はサポート対象外となります。 |
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
   <td colname="col2"> <p>数百の <span class="filepath">.csv</span> 列を顧客属性サービスにアップロードできます。ただし、購読を設定して属性を選択する場合は、所有するソリューションに応じて、次の制限が（レポートスイートごとに）適用されます。</p> <p> 
     <ul>
     <li>Foundation：0 件</li>
     <li>Select：3 件</li>
     <li>Prime：15 件</li>
     <li>Ultimate：200 件</li>
     <li>Standard：合計 3 件</li>
     <li>プレミアム：200</li>
     <li>Target Standard：5 件</li>
     <li>Target Premium：200 件</li></ul>
     </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud ID サービスへの移行は必須ですか。 </p> </td> 
   <td colname="col2"> <p>移行が必要かどうかは、使用するソリューションによって異なります。 </p> <p> 
     <ul id="ul_9C473434B5DA4C6299AAB209DEDFCDE7"> 
      <li id="li_8BC10EB2825F4ADF8CA61F71D4994A28"> <b>Adobe Analytics</b>：強く推奨されます。 </li> 
      <li id="li_56F518E3F3DF4C93B6F7EF3B40ACC52F"> <b>Adobe Target</b>：必要です。 </li> 
     </ul> </p> <p>ID サービスを使用すると、リアルタイムオーディエンス、Target 最新化、Analytics 統合、ビデオハートビート追跡など、最新の Experience Cloud 機能を利用できる機会が広がります。 </p> <p>詳しくは、<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> コアサービス - ソリューションを有効にする方法</a>を参照してください。 </p> <p> <b>注意</b>:Experience Cloud IDサービス <span class="term"> は</span> 、以前の <span class="term"> Analytics訪問者IDサービスと呼ばれていた、最新の実装です</span>。 </p> </td> 
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
   <td colname="col2"> <p> <a href="https://www.adobe.io/apis/experiencecloud/target.html" format="https" scope="external">一括プロファイル API</a> を使用すると、API を介して、Target プロファイルを個別または一括で直接更新できます。この機能は顧客属性に似ていますが、次のような大きな違いもあります。 </p> 
    <ul id="ul_5AAA4A8497C04F50A8AAA9F776BB868E"> 
     <li id="li_B20AEA397F3B4C86A1140CDA61ABD575">プロファイル API は REST API 呼び出しで、顧客属性は FTP を使用します。 </li> 
     <li id="li_7FBE428EF5D34B6AA09B6368E8210344">Target のプロファイル API は、Experience Cloud 全体ではなく、Target に対してのみデータを送信します。 </li> 
     <li id="li_CBB4D3FAF53944E0A066A4AD9F9C8760">顧客属性は、この外部データを作成および管理するためのシンプルなインターフェイスを提供します。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Target のみ）</b>顧客属性から Adobe Target にデータをアップロードすると、Target の訪問者プロファイルの有効期間が延びますか。 </p> </td> 
   <td colname="col2"> <p>はい。Adobe Target ヘルプの<a href="https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html" format="https" scope="external">訪問者プロファイルの有効期間</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（Target のみ）</b>訪問者が顧客 ID によって特定された後すぐ、顧客属性にアップロードされたデータをターゲットにできますか。 </p> </td> 
   <td colname="col2"> <p>はい。 </p> <p>mbox サードパーティ ID を含む Target へのサーバーコール時に、すべての顧客属性データを使用できます。 </p> </td> 
  </tr> 
    <tr> 
   <td colname="col1"> <p> <b> （Targetのみ）</b> 「同期ステータス」列は、顧客属性ソースにアップロードされたファイルを表しますか。 </p> </td> 
   <td colname="col2"> <p> Targetが公開および同期したレコードの数は、特定の属性ファイルに対して同期ステータスアイコンをクリックすると表示できます。 「同期%」は、Targetで同期されたプロファイルの%を指定するリアルタイム指標です。 </p> <p> <b></b> 注意：属性がTargetと同期されるまで、最大24時間かかる場合があります。 </p>
 </td> 
  </tr> 
<tr>
	<td colname="col1"> <p> 顧客属性ソースでは、ファイルのアップロード指標は何を表しますか。 </p> </td>
	<td colname="col2"> <p> 次の指標を使用して、顧客属性にアップロードされた属性のステータスを確認できます。 </p>
		<ul>
			<li> <b> レコード：属 </b> 性ファイル内のレコード数。 </li>
			<li> <b> 新しいレコード：属性 </b> ファイルに存在する新しいレコードの数。 </li>
			<li> <b> 更新されたレコード：顧客属 </b> 性に既に存在し、ファイル内の値が更新されているレコードの数。 </li>
			<li> <b> すべてのデータ（レコード）:顧客属 </b> 性に正常にアップロードされたレコードの合計数です。 </li>
		</ul>
	</td>
</tr>

</tbody> 
</table>
