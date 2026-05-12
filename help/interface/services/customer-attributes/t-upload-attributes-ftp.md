---
description: FTPを介して顧客属性データをCX Enterpriseにアップロードする方法について説明します。
solution: Experience Cloud
title: FTP経由での顧客属性データファイルのアップロード
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
TQID: 'https://experienceleague.adobe.com/VkV54Ix1ryiVxbDsPejsS1-0EVLrZC9ZPqGiG3aQ-94'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:
role_v2: id:
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 379
ht-degree: 53%

---

# FTP経由でデータファイルをアップロードします（オプション）

ドラッグ&amp;ドロップを使用してアップロードしない場合は、FTP経由で顧客属性データをCX Enterpriseにアップロードできます。

CX Enterpriseで顧客属性ソースとFTP アカウントを作成した後、データをアップロードできます。 属性ソースごとに 1 つの FTP アカウントを作成できます。 アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。 データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>ファイルをアップロードする前に、[顧客属性データファイルとソース &#x200B;](crs-data-file.md)を確認してください。

顧客属性FTP サイトへのファイルのアップロードは、FTPまたはSFTPを使用して実行できます。

* SFTP 接続をサポートしているクライアントが必要です。
* [こちら](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)で説明しているように、ユーザー名／パスワードを使用して、またはパスワードを使用せずに、SFTP で接続できます。

**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](t-crs-usecase.md)。

   FTP サイトにログインしていることを `ftp.adobe.com/<sftpname>`.

1. **[!UICONTROL Actions]**／**[!UICONTROL File Upload]**&#x200B;をクリックします。

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。 空のメモ帳ファイルでもかまいません。 例えば、`crs123.csv` をアップロードする場合は、`crs123.fin` もアップロードします。

   アップロードが正常に完了すると、どちらのファイルも **processed** というフォルダーに移動されます。

   ファイル名と構造に関する重要な情報については、[顧客属性データファイルとソース &#x200B;](crs-data-file.md)を参照してください。

## FTP アカウントの設定

属性ソースごとに1つのFTP アカウントを設定します。

[!UICONTROL File Upload and Schema Validation] ページで、**[!UICONTROL FTP Setup]**&#x200B;をクリックします。

![スキーマの編集](assets/ftp-account.png)

アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。 データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

文字列、整数および数値に適用する名前は、[!DNL Analytics] 指標の作成に使用されます。

* アップロードされた`.csv` ファイルから&#x200B;**[!UICONTROL attribute:]**&#x200B;属性データを読み取りました。

* **[!UICONTROL Type:]** データ型。例：

   * **文字列：**&#x200B;一連の文字。

   * **整数：** ゼロ、正の自然数および負の自然数。

   * **数値：**&#x200B;小数第 2 位まで取ることができます。

* **[!UICONTROL Display Name:]**&#x200B;属性のわかりやすい名前。 例えば、属性&#x200B;*customer age*&#x200B;を&#x200B;*customer Since*&#x200B;に変更できます。

* **[!UICONTROL Description:]**&#x200B;属性のわかりやすい説明。

