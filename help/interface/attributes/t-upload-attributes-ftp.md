---
description: ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。
keywords: 顧客属性;コアサービス
seo-description: ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。
seo-title: オプション - FTP を使用したデータファイルのアップロード
solution: Experience Cloud
title: オプション - FTP を使用したデータファイルのアップロード
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# オプション - FTP を使用したデータファイルのアップロード

ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。

Experience Cloud に顧客属性ソースと FTP アカウントを作成したら、データをアップロードできます。属性ソースごとに 1 つの FTP アカウントを作成できます。アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>[顧客属性をアップロードするためのデータファイル要件](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)を確認してください。


顧客属性 FTP サイトへのファイルアップロードは、FTP または SFTP を使用しておこなうことができます。

* SFTP 接続をサポートしているクライアントが必要です。
* [こちら](https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/?f=ftp_sftp_cert_auth)で説明しているように、ユーザー名／パスワードを使用して、またはパスワードを使用せずに、SFTP で接続できます。



<!-- <p>Error states - get with Matt and Dave </p> 
<p>What are the most common reasons for doing this? Retail? Do a use case example, then show an AN example. </p> 
<p>You create one FTP per attribute source. Files go to the root folder in that account. The file type .fin is user-created. (For example, upload a .csv then a .fin of the same name, which signals you have completed the upload. https://wiki.corp.adobe.com/display/marketingcloud/Customer+Record+Services#CustomerRecordServices-FileFormats (leverage for doc). Possibly link from FTP File Reqs page to a help file about naming conventions. Need a new file type page for this. Similar content here: https://marketing.adobe.com/resources/help/en_US/reference/c_general_file_structure.html and here: https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/ftp_datasources.html </p> 
<p>Drag-n-drop and zip functionality for uploads - 1/21/2015. S/b less than 100 megs for drag and drop zip file. Fin file not required for drag/drop. </p> 
<p>Preview Data - shows the last upload (?) </p> 
<p>Need a link to the "instructions" on that information icon with the image. </p> 
<p>Workflow: Drag and drop, validate schema, configure subscription, save/activate. </p> -->
**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)。

   FTP サイトにログインしていることを [!DNL ftp.adobe.com/<sftpname>] で確認します。

1. **[!UICONTROL アクション]**／**[!UICONTROL ファイルのアップロード]**&#x200B;をクリックします。

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。空のメモ帳ファイルでもかまいません。例えば、[!DNL crs123.csv] をアップロードする場合は、[!DNL crs123.fin] もアップロードします。

   アップロードに成功すると、どちらのファイルも **processed** というフォルダーに移動されます。


   ファイル名と構造に関する重要情報については、[顧客属性をアップロードするためのデータファイル要件](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)を参照してください。
