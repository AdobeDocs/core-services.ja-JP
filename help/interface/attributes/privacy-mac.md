---
description: Adobe Experience Cloud でアップロードされて使用される、個人情報（PII）に関する配慮とベストプラクティスです。
keywords: customer attributes;core services
seo-description: Adobe Experience Cloud でアップロードされて使用される、個人情報（PII）に関する配慮とベストプラクティスです。
seo-title: プライバシーに関する配慮 - 顧客属性
solution: Experience Cloud
title: プライバシーに関する配慮 - 顧客属性
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# プライバシーに関する配慮 - 顧客属性

Adobe Experience Cloud でアップロードされて使用される、個人情報（PII）に関する配慮とベストプラクティスです。


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* 姓と名
* 自宅または他の住所
* 電子メールアドレス
* 電話番号
* 社会保障番号
* 個人の物理的またはオンラインでの接触を許可するその他の識別子。 (場所によって異なります。 プライバシーとPIIに関する地域の法令を確認し、遵守してください。)


アドビは、広告主がサイトを訪問した顧客やアプリケーションを使用した顧客に関する行動情報を収集できるツールを提供します。 また、アドビは、広告主が他の情報管理システム内に持つオフラインまたは外部の顧客レコードを使用して、広告主がこの情報を拡張するためのツールも提供しています。

広告主がこの方法を採用する一般的な理由の1つは、消費者に適したマーケティングや広告の意思決定を行う際に、情報をより良くすることです。 Adobe AnalyticsとTargetでは、広告主が電子メールアドレスなどの個人情報(PII)をアップロードできるのは、その情報がハッシュ化された後に限られ、個人への連絡に使用できなくなります。 ハッシュ化された情報は、引き続き分析やマーケティングの目的に使用できます。 アドビでは、医療記録、財務アカウント情報、未成年者に関する情報など、機密性の高い個人情報を広告主がアドビに送信することを禁止しています。

このようなマーケティングや広告の決定に消費者のプライバシーが影響を及ぼす可能性があることに気付いたので、アドビはプライバシー制御を組み込んで消費者の期待に応えました。 広告主は、マーケティングの目的に適した情報を慎重に検討し、その情報を使用する権限がある状況を考慮することをお勧めします。

**ベストプラクティス**

PIIをAdobe AnalyticsまたはAdobe Targetにアップロードする場合は、アドビにアップロードする前に、PIIをハッシュ化することをお勧めします。 ハッシュ化された情報は、引き続き分析やマーケティングの目的に使用できます。 アドビでは、医療記録、財務アカウント情報、未成年者に関する情報など、機密性の高い個人情報を広告主がAdobe AnalyticsおよびAdobe Targetに送信することを禁止しています。

広告主は、マーケティングの目的に適した情報を慎重に検討し、その情報を使用する権限がある状況を考慮することをお勧めします。

消費者プライバシー法は流動的なままなので、広告主は次の3つの一般的な考え方を尊重することをお勧めします。

1. （プライバシーポリシーで）自分の言うことを行います。
1. 自分の行動を（プライバシーポリシーで）伝えます。
1. 消費者を驚かせないで。

アドビでは、これらの期待を念頭に置き、広告主が閲覧アクティビティをPIIに関連付ける場合、消費者が認証されたことを示す通知またはパーソナライゼーションを提供することをお勧めします。 例えば、Webサイトのヘッダー内に挨拶を含めます。 また、広告主は、PIIに関連付ける閲覧情報の種類や、閲覧情報がPIIに関連付けられる状況について、プライバシーポリシーで説明することをお勧めします。 最後に、消費者に提供するオプトアウトの選択肢を確認し、非認証のプロファイル情報投稿のオプトアウトを使用できるかどうかと、その方法を理解することを強くお勧めします。

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to t-publish-audience-segment, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-privacy.html </p> -->
