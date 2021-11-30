---
description: DNS プリフェッチを実装して、Experience Cloud の様々なアプリケーションやサービスでページの読み込み時間を短縮する方法について説明します。
solution: Experience Cloud
title: '様々なアプリケーションおよびサービスによる DNS 事前読み込みの使用 '
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: ht
source-wordcount: '381'
ht-degree: 100%

---

# 様々なアプリケーションおよびサービスによる DNS 事前読み込みの使用

DNS プリフェッチを実装すると、様々なアプリケーションやサービスでページ読み込み時間を短縮できます。

## DNS プリフェッチについて {#section_772BF9CB7C4141DE9B0355146E2CD962}

ブラウザーでは、Web ページ上のリンクされているドメイン名を対応する IP アドレスに自動解決するために DNS プリフェッチが使用されます。プリフェッチプロセスは、ブラウザーが Web ページを読み込んだ時点で開始されます。例えば、ページ内に `www.adobe.com` への選択可能なリンクがあるとします。このページが読み込まれると、ブラウザーは [DNS システム](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)を使用してリンクされているドメイン名を検索し、それを対応する数値 IP アドレスに解決します。サイト訪問者がリンクやボタンをクリックした時点では既にドメイン名が IP アドレスに解決されているので、DNS プリフェッチはページパフォーマンスの向上に役立ちます。DNS プリフェッチプロセスはユーザーに対して透過的なプロセスです。

## DNS プリフェッチと Adobe Experience Cloud アプリケーション {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS プリフェッチは、ページ上に埋め込まれた静的リンクに対して自動的に機能します。これは、以下の理由から、自動 DNS プリフェッチが様々な [!UICONTROL Experience Cloud] アプリケーションおよびサービスで機能しないことも意味します。

* 各 Experience Cloud アプリケーションまたはサービスは、ページ読み込み時に DNS 呼び出しを動的に生成します。
* これらの呼び出しが行われる前に、ブラウザーはドメイン名を IP アドレスに解決することはできません。

ただし、Experience Cloud アプリケーションを使用して DNS プリフェッチを手動で実装できます。これを実装するには、以下に示すように HTML タグ `<dns-prefetch>` をページコードの `<head>` セクションに追加します。DNS プリフェッチが適切に実装されると、ページ読み込み時間を数ミリ秒短縮できます。

## DNS プリフェッチのコードサンプル {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

次の例は、様々な [!DNL Experience Cloud] アプリケーションおよびサービスに対して DNS プリフェッチを呼び出す方法を示しています。一部のプリフェッチ呼び出しには[!DNL Adobe]組織 ID またはトラッキングサーバー情報が必要です。各サンプル内の&#x200B;*斜体*&#x200B;で記述されたコードは変数のプレースホルダーを表しています。そのコードは、自分の [!DNL Adobe] パートナー ID、顧客コード、トラッキングサーバー情報などに置き換えます。

* **Analytics：** `<link rel="dns-prefetch" href="//insert tracking server name here">`。

   非セキュアなトラッキングサーバーとセキュアなトラッキングサーバーを使用する場合は、DNS 名ごとに個別のタグを追加します。

* **Audience Manager：** `<link rel="dns-prefetch" href="//dpm.demdex.net">`。

* **Experience Cloud ID サービス：** `<link rel="dns-prefetch" href="//fast. *`ここにパートナー ID を挿入する`*.demdex.net">`

* **Dynamic Tag Manager**（DTM）：必須ではありません。DTM リンクは、ページの読み込み時に利用できます。

* **Media Optimizer（Advertising Cloud）：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **[!DNL Target]：** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [DNS プリフェッチ](https://www.chromium.org/developers/design-documents/dns-prefetching)

