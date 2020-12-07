---
description: ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。
keywords: Customer Attributes;core services
solution: Experience Cloud
title: FTPを使用した顧客属性データファイルのアップロード |Adobe Experience Cloud
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: 4bea0c29afa580dc63b21535ce5c275cd649c9a5
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 95%

---


# オプション - FTP を使用したデータファイルのアップロード

ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。

Experience Cloud に顧客属性ソースと FTP アカウントを作成したら、データをアップロードできます。属性ソースごとに 1 つの FTP アカウントを作成できます。アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>[顧客属性をアップロードするためのデータファイル要件](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)を確認してください。

顧客属性 FTP サイトへのファイルアップロードは、FTP または SFTP を使用しておこなうことができます。

* SFTP 接続をサポートしているクライアントが必要です。
* [こちら](https://docs.adobe.com/help/ja-JP/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)で説明しているように、ユーザー名／パスワードを使用して、またはパスワードを使用せずに、SFTP で接続できます。

**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)。

   FTP サイトにログインしていることを `ftp.adobe.com/<sftpname>`.

1. **[!UICONTROL アクション]**／**[!UICONTROL ファイルのアップロード]**&#x200B;をクリックします。

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。空のメモ帳ファイルでもかまいません。例えば、[!DNL crs123.csv] をアップロードする場合は、[!DNL crs123.fin] もアップロードします。

   アップロードが正常に完了すると、どちらのファイルも **processed** というフォルダーに移動されます。

   ファイル名とファイル構造について詳しくは、[顧客属性をアップロードするためのデータファイル要件](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)を参照してください。
