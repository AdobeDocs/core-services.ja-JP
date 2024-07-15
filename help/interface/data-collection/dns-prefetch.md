---
description: DNS プリフェッチを実装して、Experience Cloud の様々なアプリケーションやサービスでページの読み込み時間を短縮する方法について説明します。
solution: Experience Cloud
title: DNS プリフェッチの使用
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: 9ee4d9b0e670dec35cda530892c49e36bf7cc107
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 92%

---

# DNS プリフェッチの使用

DNS プリフェッチを実装すると、様々なアプリケーションやサービスでページ読み込み時間を短縮できます。

## DNS プリフェッチについて

ブラウザーでは、Web ページ上のリンクされているドメイン名を対応する IP アドレスに自動解決するために DNS プリフェッチが使用されます。プリフェッチプロセスは、ブラウザーが Web ページを読み込んだ時点で開始されます。例えば、ページ内に `www.adobe.com` への選択可能なリンクがあるとします。このページが読み込まれると、ブラウザーは [DNS システム](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)を使用してリンクされているドメイン名を検索し、それを対応する数値 IP アドレスに解決します。サイト訪問者がリンクやボタンをクリックした時点では既にドメイン名が IP アドレスに解決されているので、DNS プリフェッチはページパフォーマンスの向上に役立ちます。DNS プリフェッチプロセスはユーザーに対して透過的なプロセスです。

## DNS プリフェッチと Adobe Experience Cloud アプリケーション

DNS プリフェッチは、ページ上に埋め込まれた静的リンクに対して自動的に機能します。これは、以下の理由から、自動 DNS プリフェッチが異なる [!UICONTROL Experience Cloud] アプリケーションおよびサービスで機能しないことも意味します。

* 各 Experience Cloud アプリケーションまたはサービスは、ページ読み込み時に DNS 呼び出しを動的に生成します。
* これらの呼び出しが行われる前に、ブラウザーはドメイン名を IP アドレスに解決することはできません。

ただし、Experience Cloud アプリケーションを使用して DNS プリフェッチを手動で実装できます。これを実装するには、以下に示すように HTML タグ `<dns-prefetch>` をページコードの `<head>` セクションに追加します。DNS プリフェッチが適切に実装されると、ページ読み込み時間を数ミリ秒短縮できます。

## DNS プリフェッチのコードサンプル

次の例は、様々な [!DNL Experience Cloud] アプリケーションおよびサービスに対して DNS プリフェッチを呼び出す方法を示しています。一部のプリフェッチ呼び出しには[!DNL Adobe]組織 ID またはトラッキングサーバー情報が必要です。各サンプル内の&#x200B;*斜体*&#x200B;で記述されたコードは変数のプレースホルダーを表しています。そのコードは、自分の [!DNL Adobe] パートナー ID、顧客コード、トラッキングサーバー情報などに置き換えます。

* **Analytics：** `<link rel="dns-prefetch" href="//data.example.com">`。

  非セキュアなトラッキングサーバーとセキュアなトラッキングサーバーを使用する場合は、DNS 名ごとに個別のタグを追加します。

* **Audience Manager：** `<link rel="dns-prefetch" href="//dpm.demdex.net">`。

* **Experience CloudID サービス：** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]：** `<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* Chromium での [DNS プリフェッチ ](https://www.chromium.org/developers/design-documents/dns-prefetching)
