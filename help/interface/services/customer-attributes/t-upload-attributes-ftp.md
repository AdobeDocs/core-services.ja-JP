---
description: FTP 経由で顧客属性データをExperience Cloudにアップロードする方法を説明します。
solution: Experience Cloud
title: FTP 経由での顧客属性データファイルのアップロード
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
TQID: https://experienceleague.adobe.com/jI2dWXMmrrWxceVi-sZtzF5cTF11iy4d7QKkx71vF-I
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 361
ht-degree: 56%

---

# FTP を使用したデータファイルのアップロード（オプション）

ドラッグ&amp;ドロップを使用してアップロードしない場合は、FTP 経由で顧客属性データをExperience Cloudにアップロードできます。

Experience Cloudで顧客属性ソースと FTP アカウントを作成したら、データをアップロードできます。 属性ソースごとに 1 つの FTP アカウントを作成できます。アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

>[!IMPORTANT]
>
>ファイルをアップロードする前に、[&#x200B; 顧客属性データファイルとソース &#x200B;](crs-data-file.md) を確認してください。

顧客属性 FTP サイトへのファイルアップロードは、FTP または SFTP を使用して実行できます。

* SFTP 接続をサポートしているクライアントが必要です。
* [こちら](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=ja)で説明しているように、ユーザー名／パスワードを使用して、またはパスワードを使用せずに、SFTP で接続できます。

**FTP を使用してデータファイルをアップロードするには**

1. [顧客属性ソースを作成し、データファイルをアップロードします](t-crs-usecase.md)。

   FTP サイトにログインしていることを `ftp.adobe.com/<sftpname>`.

1. **[!UICONTROL Actions]**／**[!UICONTROL File Upload]**&#x200B;をクリックします。

1. ファイルを取得できるように、`.fin` ファイルをアップロードします。

   ファイルタイプ `.fin` は、ユーザーによって作成されるもので、アップロードが完了したことを示す合図です。空のメモ帳ファイルでもかまいません。例えば、`crs123.csv` をアップロードする場合は、`crs123.fin` もアップロードします。

   アップロードが正常に完了すると、どちらのファイルも **processed** というフォルダーに移動されます。

   ファイル名とファイル構造に関する重要な情報については、[&#x200B; 顧客属性データファイルとソース &#x200B;](crs-data-file.md) を参照してください。

## FTP アカウントの設定

属性ソースごとに 1 つの FTP アカウントを設定します。

[!UICONTROL File Upload and Schema Validation] ページで「**[!UICONTROL FTP Setup]**」をクリックします。

![スキーマの編集](assets/ftp-account.png)

アップロードしたファイルは、そのアカウントのルートフォルダーに保存されます。データは `.csv` 形式にする必要があります。2 つ目の `.fin` ファイルは、アップロードが完了したことを示します。

文字列、整数および数値に適用する名前は、[!DNL Analytics] 指標の作成に使用されます。

* **[!UICONTROL attribute:]** ップロードされた `.csv` ファイルから読み取られた属性データ。

* **[!UICONTROL Type:]** データタイプ（例：）。

   * **文字列：**&#x200B;一連の文字。

   * **整数：** ゼロ、正の自然数および負の自然数。

   * **数値：**&#x200B;小数第 2 位まで取ることができます。

* **[!UICONTROL Display Name:]** 属性のわかりやすい名前。 例えば、属性 *顧客の年齢* を *顧客となった年数* に変更できます。

* **[!UICONTROL Description:]** 属性のわかりやすい説明。

