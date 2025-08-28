---
description: FTP 経由で顧客属性データをExperience Cloudにアップロードする方法を説明します。
solution: Experience Cloud
title: FTP 経由での顧客属性データファイルのアップロード
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 67%

---

# FTP を使用したデータファイルのアップロード（オプション）

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

## FTP アカウントの設定

属性ソースごとに 1 つの FTP アカウントを設定します。

[!UICONTROL  ファイルのアップロードとスキーマの検証 ] ページで、「**[!UICONTROL FTP 設定]**」をクリックします。

![スキーマの編集](assets/ftp-account.png)

アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

文字列、整数および数値に適用する名前は、[!DNL Analytics] 指標の作成に使用されます。

* **[!UICONTROL attribute:]** アップロードされた `.csv` ファイルから読み取られた属性データ。

* **[!UICONTROL タイプ：]**&#x200B;データタイプ。次のようなものがあります。

   * **文字列：**&#x200B;一連の文字。

   * **整数：** ゼロ、正の自然数および負の自然数。

   * **数値：**&#x200B;小数第 2 位まで取ることができます。

* **[!UICONTROL 表示名：]**&#x200B;属性のわかりやすい名前。例えば、属性 *顧客の年齢* を *顧客となった年数* に変更できます。

* **[!UICONTROL 説明：]**&#x200B;属性のわかりやすい説明。