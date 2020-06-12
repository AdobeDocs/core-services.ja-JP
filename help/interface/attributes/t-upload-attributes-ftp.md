---
description: ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。
keywords: Customer Attributes;core services
seo-description: ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。
seo-title: オプション - FTP を使用したデータファイルのアップロード
solution: Experience Cloud
title: オプション - FTP を使用したデータファイルのアップロード
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 85%

---


# オプション - FTP を使用したデータファイルのアップロード

ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。

Experience Cloud に顧客属性ソースと FTP アカウントを作成したら、データをアップロードできます。属性ソースごとに 1 つの FTP アカウントを作成できます。アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>Review [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) before uploading the file.

顧客属性FTPサイトへのファイルのアップロードは、FTPまたはSFTPを使用して行うことができます。

* SFTP 接続をサポートしているクライアントが必要です。
* [こちら](https://docs.adobe.com/help/ja-JP/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)で説明しているように、ユーザー名／パスワードを使用して、またはパスワードを使用せずに、SFTP で接続できます。

**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)。

   FTP サイトにログインしていることを [!DNL ftp.adobe.com/<sftpname>] で確認します。

1. **[!UICONTROL アクション]**／**[!UICONTROL ファイルのアップロード]**&#x200B;をクリックします。

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。空のメモ帳ファイルでもかまいません。例えば、[!DNL crs123.csv] をアップロードする場合は、[!DNL crs123.fin] もアップロードします。

   アップロードが正常に完了すると、どちらのファイルも **processed** というフォルダーに移動されます。

   See [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) for important information about file names and structure.
