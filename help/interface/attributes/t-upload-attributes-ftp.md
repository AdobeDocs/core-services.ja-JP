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
ht-degree: 54%

---


# オプション - FTP を使用したデータファイルのアップロード

ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。

Experience Cloudに顧客属性ソースとFTPアカウントを作成した後に、データをアップロードできます。 属性ソースごとに1つのFTPアカウントを作成します。 アップロードされたファイルは、そのアカウントのルートフォルダーに保存されます。 データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>Review [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) before uploading the file.

顧客属性FTPサイトへのファイルのアップロードは、FTPまたはSFTPを使用して行うことができます。

* SFTP接続をサポートするクライアントが必要です。
* ここで説明するように、ユーザー名/パスワードを使用して、またはパスワードを使用しないでSFTPで接続でき [ます](https://docs.adobe.com/help/en/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)。

**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)。

   FTP サイトにログインしていることを [!DNL ftp.adobe.com/<sftpname>] で確認します。

1. Click **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。空のメモ帳ファイルでもかまいません。例えば、[!DNL crs123.csv] をアップロードする場合は、[!DNL crs123.fin] もアップロードします。

   アップロードが正常に完了すると、両方のファイルは「 **処理済み**」というフォルダーに移動されます。

   See [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) for important information about file names and structure.
