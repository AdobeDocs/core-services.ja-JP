---
description: デスクトップまたはモバイルブラウザーですべての cookie をブロックしているユーザーを削除します。このプライバシー設定は、Analyticsデータ収集をオプトアウトしたユーザーを除外します。
keywords: cookies;privacy
seo-description: デスクトップまたはモバイルブラウザーですべての cookie をブロックしているユーザーを削除します。このプライバシー設定は、Analyticsデータ収集をオプトアウトしたユーザーを除外します。
seo-title: ブラウザー cookie のプライバシー設定の有効化
solution: Marketing Cloud,Adobe Analytics,Adobe Target,Adobe Social
title: ブラウザー cookie のプライバシー設定の有効化
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# ブラウザー cookie のプライバシー設定の有効化{#enable-privacy-settings-for-browser-cookies}

デスクトップおよびモバイルブラウザーですべてのcookieをブロックしたユーザーを削除できます。 この機能は、データ収集をオプトアウトしたユーザーを除外するプライバシー設定です。Analyticsの処理を停止するユーザーの意図を尊重できます。

**ブラウザーCookieのプライバシー設定を有効にするには**

1. Navigate to **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]**.
1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Privacy Settings]**.
1. （デスクトップまたはモバイルに対して）「**[!UICONTROL プライバシー設定]**」を有効にします。

>[!IMPORTANT]
>
>多くのモバイルアプリ（FacebookやTwitterのアプリ内ブラウザーなど）は標準のモバイルブラウザーとして表示できますが、すべてのCookieを許可していないことに注意してください。 この機能を有効にすると、Analyticsレポートからモバイルトラフィックの大部分が除外される可能性があります。

**ブラウザーのプライバシー設定について**

法律や規制のガイダンスでは、cookieをブロックするユーザーの行動は、プロファイルをオプトアウトするユーザーの行動と同じであると表明されています。 この機能を有効にすると、ユーザーがブラウザーを設定してすべてのCookieをブロックしたデスクトップブラウザーから収集されたデータは、Analyticsレポートから除外されます。 アドビがWebブラウザーを認識できない場合、データはAnalyticsレポートに含まれます。

世界中の議員が、cookieブラウザーの設定は、プロファイリングをオプトアウトするユーザーの好みを示すものであると（ガイダンスと決済の両方で）述べています。 特に、これらの議員は、サードパーティcookieをブロックするブラウザー設定は、サードパーティ（クロスサイト）の追跡からのオプトアウトリクエストであると述べています。 すべてのCookieのブロックアウトは、すべての追跡のオプトアウトリクエストです。 サーバー側の識別子（IPアドレスやユーザーエージェントなど）は、cookieブラウザーの設定をバイパスする望ましいオプションですが、一部の議員は、これらをユーザー選択の妨げと見なします。