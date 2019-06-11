---
description: DNS プリフェッチを実装すると、各種ソリューションやサービスでページ読み込み時間を短縮できます。
seo-description: DNS プリフェッチを実装すると、各種ソリューションやサービスでページ読み込み時間を短縮できます。
seo-title: 様々なソリューションおよびサービスによるDNSプリフェッチの使用
solution: Experience Cloud
title: 様々なソリューションおよびサービスによるDNSプリフェッチの使用
uuid: 4220e223- e00e-46b1-8bde-52248913bea1
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# 様々なソリューションおよびサービスによるDNSプリフェッチの使用

DNS プリフェッチを実装すると、各種ソリューションやサービスでページ読み込み時間を短縮できます。

## DNSプリフェッチについて {#section_772BF9CB7C4141DE9B0355146E2CD962}

ブラウザーでは、Web ページ上のリンクされているドメイン名を対応する IP アドレスに自動解決するために DNS プリフェッチが使用されます。プリフェッチプロセスは、ブラウザーが Web ページを読み込んだ時点で開始されます。例えば、ページにクリック可能なリンクが含まれているとし `www.adobe.com`ます。このページが読み込まれると、ブラウザーは [DNS システム](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)を使用してリンクされているドメイン名を検索し、それを対応する数値 IP アドレスに解決します。サイト訪問者がリンクやボタンをクリックした時点では既にドメイン名が IP アドレスに解決されているので、DNS プリフェッチはページパフォーマンスの向上に役立ちます。DNS プリフェッチプロセスはユーザーに対して透過的なプロセスです。

## DNSプリフェッチおよびAdobe Experience Cloudソリューション {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS プリフェッチはページ上に埋め込まれている静的リンクに対して自動的に実行されます。以下の理由から、自動 DNS プリフェッチは、各種 [!UICONTROL Experience Cloud] ソリューションおよびサービスに対しては実行されません。

* 各 Experience Cloud ソリューションまたはサービスでは、ページ読み込み時に DNS 呼び出しが動的に生成されます。
* ブラウザーは、これらの呼び出しがおこなわれる前に、ドメイン名を IP アドレスに解決することができません。

ただし、DNS プリフェッチは、Experience Cloud ソリューションと共に手動で実装することができます。これを行うには、次に示すように、ページコードのセクションにHTML `<dns-prefetch>``<head>` タグを追加します。DNS プリフェッチが適切に実装されると、ページ読み込み時間を数ミリ秒短縮できます。

## DNSプリフェッチコードサンプル {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

以下のサンプルは、各種 [!DNL Experience Cloud] ソリューションおよびサービスに対する DNS プリフェッチの呼び出し方法を示しています。一部のプリフェッチ呼び出しで [!DNL Adobe] は、組織IDを要求するか、サーバー情報を追跡する必要があります。各サンプル内の*斜体*で記述されたコードは変数のプレースホルダーを表しています。そのコードを独自 [!DNL Adobe] のパートナーID、顧客コード、トラッキングサーバー情報などに置き換えます。

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   非セキュアなトラッキングサーバーとセキュアなトラッキングサーバーを使用する場合は、DNS 名ごとに個別のタグを追加します。

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience Cloud IDサービス:**`<link rel="dns-prefetch" href="//fast. *`ここにパートナーIDを挿入する`*.demdex.net">`

* **Dynamic Tag Manager** （DTM）:不要です。ページが読み込まれるとすぐに DTM リンクが使用可能になります。

* **Media Manager（広告クラウド）:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **Target:** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_ LIKE_ THIS]
>
>* [DNS プリフェッチ](https://www.chromium.org/developers/design-documents/dns-prefetching)

