---
description: DNS プリフェッチを実装して、Experience Cloud の様々なソリューションやサービスでページ読み込み時間を短縮する方法について説明します。
solution: Experience Cloud
title: '様々なソリューションおよびサービスによる DNS プリフェッチの使用 '
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
feature: 顧客属性
topic: 管理
role: Administrator
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: 93f5eda7229990e3645b54efa2a172d7b57dcb9b
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 88%

---

# 様々なソリューションおよびサービスによる DNS プリフェッチの使用

DNS プリフェッチを実装すると、各種ソリューションやサービスでページ読み込み時間を短縮できます。

## DNS プリフェッチについて {#section_772BF9CB7C4141DE9B0355146E2CD962}

ブラウザーでは、Web ページ上のリンクされているドメイン名を対応する IP アドレスに自動解決するために DNS プリフェッチが使用されます。プリフェッチプロセスは、ブラウザーが Web ページを読み込んだ時点で開始されます。例えば、ページに`www.adobe.com`への選択可能なリンクが含まれているとします。 このページが読み込まれると、ブラウザーは [DNS システム](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)を使用してリンクされているドメイン名を検索し、それを対応する数値 IP アドレスに解決します。サイト訪問者がリンクやボタンをクリックした時点では既にドメイン名が IP アドレスに解決されているので、DNS プリフェッチはページパフォーマンスの向上に役立ちます。DNS プリフェッチプロセスはユーザーに対して透過的なプロセスです。

## DNS プリフェッチと Adobe Experience Cloud ソリューション {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS プリフェッチはページ上に埋め込まれている静的リンクに対して自動的に実行されます。以下の理由から、自動 DNS プリフェッチは、各種 [!UICONTROL Experience Cloud] ソリューションおよびサービスに対しては実行されません。

* 各 Experience Cloud ソリューションまたはサービスでは、ページ読み込み時に DNS 呼び出しが動的に生成されます。
* ブラウザーは、これらの呼び出しがおこなわれる前に、ドメイン名を IP アドレスに解決することができません。

ただし、DNS プリフェッチは、Experience Cloud ソリューションと共に手動で実装することができます。これを実装するには、以下に示すように HTML タグ `<dns-prefetch>` をページコードの `<head>` セクションに追加します。DNS プリフェッチが適切に実装されると、ページ読み込み時間を数ミリ秒短縮できます。

## DNS プリフェッチのコードサンプル {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

以下のサンプルは、各種 [!DNL Experience Cloud] ソリューションおよびサービスに対する DNS プリフェッチの呼び出し方法を示しています。一部のプリフェッチ呼び出しには[!DNL Adobe]組織 ID またはトラッキングサーバー情報が必要です。各サンプル内の&#x200B;*斜体*&#x200B;で記述されたコードは変数のプレースホルダーを表しています。このコードを、独自の[!DNL Adobe]パートナーID、顧客コード、トラッキングサーバー情報などに置き換えます。

* **Analytics：** `<link rel="dns-prefetch" href="//insert tracking server name here">`。

   非セキュアなトラッキングサーバーとセキュアなトラッキングサーバーを使用する場合は、DNS 名ごとに個別のタグを追加します。

* **Audience Manager：** `<link rel="dns-prefetch" href="//dpm.demdex.net">`。

* **Experience Cloud ID サービス：**`<link rel="dns-prefetch" href="//fast. *`ここにパートナー ID を挿入する`*.demdex.net">`

* **Dynamic Tag Manager**（DTM）：必須ではありません。ページの読み込み時にDTMリンクを使用できます。

* **Media Manager(Advertising Cloud):**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **[!DNL Target]：**`<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [DNS プリフェッチ](https://www.chromium.org/developers/design-documents/dns-prefetching)

