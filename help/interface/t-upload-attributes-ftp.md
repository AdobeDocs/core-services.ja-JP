---
description: FTP 経由で顧客属性データを Experience Cloud にアップロードする方法について説明します。
keywords: 顧客属性;コアサービス
solution: Experience Cloud
title: 'FTP を介した顧客属性データファイルのアップロード '
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
feature: 顧客属性
topic: 管理
role: Administrator
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: ebefd433e96da422674e7ee71c8988d4011fed11
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 90%

---

# オプション - FTP を使用したデータファイルのアップロード

ドラッグ＆ドロップを使用してアップロードしない場合は、FTP を利用して顧客属性データを Experience Cloud にアップロードできます。

Experience Cloud に顧客属性ソースと FTP アカウントを作成したら、データをアップロードできます。属性ソースごとに 1 つの FTP アカウントを作成できます。アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは`.csv`形式にする必要があります。2つ目の`.fin`ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>[顧客属性をアップロードするためのデータファイル要件](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)を確認してください。

顧客属性 FTP サイトへのファイルアップロードは、FTP または SFTP を介して実行できます。

* SFTP 接続をサポートしているクライアントが必要です。
* [こちら](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=en)で説明しているように、ユーザー名／パスワードを使用して、またはパスワードを使用せずに、SFTP で接続できます。

**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)。

   FTP サイトにログインしていることを `ftp.adobe.com/<sftpname>`.

1. **[!UICONTROL アクション]**／**[!UICONTROL ファイルのアップロード]**&#x200B;をクリックします。

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。空のメモ帳ファイルでもかまいません。例えば、[!DNL crs123.csv] をアップロードする場合は、[!DNL crs123.fin] もアップロードします。

   アップロードが正常に完了すると、どちらのファイルも **processed** というフォルダーに移動されます。

   ファイル名とファイル構造について詳しくは、[顧客属性をアップロードするためのデータファイル要件](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)を参照してください。