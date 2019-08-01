---
description: デスクトップまたはモバイルブラウザーですべての cookie をブロックしているユーザーを削除します。
keywords: cookie;プライバシー
seo-description: デスクトップまたはモバイルブラウザーですべての cookie をブロックしているユーザーを削除します。
seo-title: ブラウザー cookie のプライバシー設定の有効化
solution: Marketing Cloud、Analytics、Target、Social
title: ブラウザー cookie のプライバシー設定の有効化
uuid: f6a56e8b- b021-49db-8eb4-6c14af0c7243
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# ブラウザー cookie のプライバシー設定の有効化{#enable-privacy-settings-for-browser-cookies}

デスクトップまたはモバイルブラウザーですべての cookie をブロックしているユーザーを削除します。

この設定をおこなうと、ユーザーがブラウザーの cookie 設定ですべての cookie をブロックしている場合に、Analytics の処理を停止したいというユーザーの意向を尊重することができます。

1. **[!UICONTROL 管理ツール]** / **[!UICONTROL レポートスイートに移動]**&#x200B;します。
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Privacy Settings]**.
1. **[!UICONTROL プライバシー設定]** を有効にする（デスクトップまたはモバイル用）。

   この機能を有効にすると、すべての cookie をブロックするように設定されているデスクトップブラウザーから収集されたデータは、Analytics のレポートから除外されます。そのブラウザーがアドビの認識外のものである場合は、収集されたデータが Analytics のレポートに含まれます。

>[!IMPORTANT]
>
>多くのモバイルアプリ（FacebookやTwitter用のアプリブラウザーなど）は、標準モバイルブラウザーとして表示できますが、すべてのCookieを許可しないことに注意してください。この機能を有効にすると、モバイルトラフィックの多くが Analytics のレポートから除外される可能性があります。

**ブラウザーのプライバシー設定について**

法律および規制手引きでは、エンドユーザーが cookie をブロックするアクションはプロファイルをオプトアウトするアクションと同じであるとされています。この機能を有効にすると、すべての cookie をブロックするように設定されているデスクトップブラウザーから収集されたデータは、Analytics のレポートから除外されます。その Web ブラウザーがアドビの認識外のものである場合は、収集されたデータが Analytics のレポートに含まれます。

世界中の立法関係者が（手引きと合意の両方において）、ブラウザーの cookie 設定はプロファイリングの対象から外れたいというユーザーの意思を示すものであると言明しています。具体的に言うと、サードパーティ cookie をブロックするブラウザー設定はサードパーティ（クロスサイト）トラッキングからのオプトアウトを表明するものであり、すべての cookie をブロックする設定はすべてのトラッキングからのオプトアウトを表明するものであると多くの立法関係者が述べています。ブラウザーの cookie 設定を迂回する手段としてサーバー側の識別情報（IP アドレスやユーザーエージェント）を利用する方法もありますが、こうした手法はユーザーの選択に背くものであると一部の立法関係者は考えています。

<!--
<p>Awaiting content from Vinay May 20 2015 </p>
<p>https://wiki.corp.adobe.com/display/omtrcache/Inferred+Opt+Out </p>
<p>https://wiki.corp.adobe.com/display/omtrplatform/Auto-opt-out+For+Users+Who+Block+Cookies </p>
-->

