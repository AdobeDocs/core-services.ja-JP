---
description: CX Enterpriseの様々なアプリケーションやサービスでページの読み込み時間を短縮するために、DNS プリフェッチを実装する方法について説明します。
solution: Experience Cloud
title: DNS プリフェッチの使用
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
TQID: https://experienceleague.adobe.com/oAe81mw-qFetDM0zky2eS6DNf-XZ67H68Qw-Sa8mk0Y
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
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 77%

---

# DNS プリフェッチの使用

DNS プリフェッチを実装すると、様々なアプリケーションやサービスでページ読み込み時間を短縮できます。

## DNS プリフェッチについて

ブラウザーでは、Web ページ上のリンクされているドメイン名を対応する IP アドレスに自動解決するために DNS プリフェッチが使用されます。 プリフェッチプロセスは、ブラウザーが Web ページを読み込んだ時点で開始されます。 例えば、ページ内に `www.adobe.com` への選択可能なリンクがあるとします。 このページが読み込まれると、ブラウザーは _DNS システム_&#x200B;を使用してリンクされているドメイン名を検索し、それを対応する数値 IP アドレスに解決します。 サイト訪問者がリンクやボタンをクリックした時点では既にドメイン名が IP アドレスに解決されているので、DNS プリフェッチはページパフォーマンスの向上に役立ちます。 DNS プリフェッチプロセスはユーザーに対して透過的なプロセスです。

## DNS プリフェッチとAdobe CX Enterprise アプリケーション

DNS プリフェッチは、ページ上に埋め込まれた静的リンクに対して自動的に機能します。 また、次の理由により、DNS プリフェッチが異なる[!UICONTROL CX Enterprise]個のアプリケーションとサービスで機能しないことも意味します。

* 各CX Enterprise アプリケーションまたはサービスは、ページの読み込みに応じてDNS呼び出しを動的に生成します。
* これらの呼び出しが行われる前に、ブラウザーはドメイン名を IP アドレスに解決することはできません。

ただし、CX Enterprise アプリケーションでは、DNS プリフェッチを手動で実装できます。 これを実装するには、以下に示すように HTML タグ `<dns-prefetch>` をページコードの `<head>` セクションに追加します。 DNS プリフェッチが適切に実装されると、ページ読み込み時間を数ミリ秒短縮できます。

## DNS プリフェッチのコードサンプル

次の例は、様々な [!DNL CX Enterprise] アプリケーションおよびサービスに対して DNS プリフェッチを呼び出す方法を示しています。 一部のプリフェッチ呼び出しには[!DNL Adobe]組織 ID またはトラッキングサーバー情報が必要です。 各サンプル内の&#x200B;*斜体*&#x200B;で記述されたコードは変数のプレースホルダーを表しています。 そのコードは、自分の [!DNL Adobe] パートナー ID、顧客コード、トラッキングサーバー情報などに置き換えます。

* **Analytics：** `<link rel="dns-prefetch" href="//data.example.com">`。

  非セキュアなトラッキングサーバーとセキュアなトラッキングサーバーを使用する場合は、DNS 名ごとに個別のタグを追加します。

* **Audience Manager：** `<link rel="dns-prefetch" href="//dpm.demdex.net">`。

* **CX Enterprise ID サービス：** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]:** `<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* Chromiumで[DNS プリフェッチ &#x200B;](https://www.chromium.org/developers/design-documents/dns-prefetching)

