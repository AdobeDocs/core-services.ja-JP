---
description: DNS プリフェッチを実装すると、各種ソリューションやサービスでページ読み込み時間を短縮できます。
seo-description: DNS プリフェッチを実装すると、各種ソリューションやサービスでページ読み込み時間を短縮できます。
seo-title: 様々なソリューションおよびサービスによる DNS プリフェッチの使用
solution: Experience Cloud
title: 様々なソリューションおよびサービスによる DNS プリフェッチの使用
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 様々なソリューションおよびサービスによる DNS プリフェッチの使用

DNS プリフェッチを実装すると、各種ソリューションやサービスでページ読み込み時間を短縮できます。

## DNS プリフェッチについて {#section_772BF9CB7C4141DE9B0355146E2CD962}

ブラウザーは、DNSプリフェッチを使用して、Webページにリンクされたドメイン名を、対応するIPアドレスに自動的に解決します。 プリフェッチ処理は、ブラウザがWebページを読み込むと開始されます。 例えば、ページ内に `www.adobe.com` へのクリック可能なリンクがあるとします。When a browser loads this page, it uses the [DNS system](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) to look up the linked domain name and resolve it to a corresponding numeric IP address. DNSプリフェッチは、サイト訪問者がそのリンクまたはボタンをクリックする前にドメイン名が既にIPアドレスに解決されるので、ページのパフォーマンスを向上させます。 DNSプリフェッチ処理は、ユーザーに対して透過的です。

## DNS プリフェッチと Adobe Experience Cloud ソリューション {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNSプリフェッチは、ページ上の静的な埋め込みリンクで自動的に機能します。 また、次の理由から、DNSの自動プリフェッチは異なる [!UICONTROL Experience Cloudのソリューション] /サービスでは機能しません。

* 各Experience Cloudソリューションまたはサービスは、ページの読み込み時に動的にDNS呼び出しを生成します。
* これらの呼び出しが行われる前に、ブラウザーはドメイン名をIPアドレスに解決できません。

ただし、Experience CloudソリューションでDNSプリフェッチを手動で実装することはできます。 これを実装するには、以下に示すように HTML タグ `<dns-prefetch>` をページコードの `<head>` セクションに追加します。DNS プリフェッチが適切に実装されると、ページ読み込み時間を数ミリ秒短縮できます。

## DNS プリフェッチのコードサンプル {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

以下のサンプルは、各種 [!DNL Experience Cloud] ソリューションおよびサービスに対する DNS プリフェッチの呼び出し方法を示しています。一部のプリフェッチ呼び出しには[!DNL Adobe]組織 ID またはトラッキングサーバー情報が必要です。各サンプル内の&#x200B;*斜体*&#x200B;で記述されたコードは変数のプレースホルダーを表しています。これらの部分は、自分の [!DNL Adobe] パートナー ID、顧客コード、トラッキングサーバー情報などに置き換えます。

* **Analytics：** `<link rel="dns-prefetch" href="//insert tracking server name here">`。

   非セキュアなトラッキングサーバーとセキュアなトラッキングサーバーを使用する場合は、DNS 名ごとに個別のタグを追加します。

* **Audience Manager：** `<link rel="dns-prefetch" href="//dpm.demdex.net">`。

* **Experience Cloud IDサービス：** ここにパ `<link rel="dns-prefetch" href="//fast. *`ートナーIDを挿入`*.demdex.net">`

* **Dynamic Tag Manager**（DTM）：必須ではありません。ページが読み込まれるとすぐに DTM リンクが使用可能になります。

* **Media Manager（広告クラウド）：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **[!DNL Target]:**`<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_LIKE_THIS]
>
>* [DNSのプリフェッチ](https://www.chromium.org/developers/design-documents/dns-prefetching)

