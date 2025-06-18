---
description: FTP 経由で顧客属性データをExperience Cloudにアップロードする方法を説明します。
solution: Experience Cloud
title: FTP を使用した顧客属性データファイルのアップロード
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 71%

---

# オプション - FTP を使用したデータファイルのアップロード

ドラッグ&amp;ドロップを使用してアップロードしない場合は、FTP 経由で顧客属性データをExperience Cloudにアップロードできます。

Experience Cloudで顧客属性ソースと FTP アカウントを作成したら、データをアップロードできます。 属性ソースごとに 1 つの FTP アカウントを作成できます。アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>[顧客属性をアップロードするためのデータファイル要件](crs-data-file.md)を確認してください。

顧客属性 FTP サイトへのファイルアップロードは、FTP または SFTP を使用して実行できます。

* SFTP 接続をサポートしているクライアントが必要です。
* [こちら](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)で説明しているように、ユーザー名／パスワードを使用して、またはパスワードを使用せずに、SFTP で接続できます。

**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](t-crs-usecase.md)。

   FTP サイトにログインしていることを `ftp.adobe.com/<sftpname>`.

1. **[!UICONTROL アクション]**／**[!UICONTROL ファイルのアップロード]**&#x200B;をクリックします。

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。空のメモ帳ファイルでもかまいません。例えば、`crs123.csv` をアップロードする場合は、`crs123.fin` もアップロードします。

   アップロードが正常に完了すると、どちらのファイルも **processed** というフォルダーに移動されます。

   ファイル名とファイル構造について詳しくは、[顧客属性をアップロードするためのデータファイル要件](crs-data-file.md)を参照してください。
