---
description: Adobe Experience Cloud でアップロードされて使用される、個人情報（PII）に関する配慮とベストプラクティスです。
keywords: 顧客属性;コアサービス
seo-description: Adobe Experience Cloud でアップロードされて使用される、個人情報（PII）に関する配慮とベストプラクティスです。
seo-title: プライバシーに関する配慮 - 顧客属性
solution: Experience Cloud
title: プライバシーに関する配慮 - 顧客属性
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# プライバシーに関する配慮 - 顧客属性

Adobe Experience Cloud でアップロードされて使用される、個人情報（PII）に関する配慮とベストプラクティスです。


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* 姓名
* 自宅またはその他の住所
* 電子メールアドレス
* 電話番号
* 社会保障番号
* 個人との物理的またはオンラインでの接触を可能にするその他の識別情報（場所によって異なります。営業しているすべての場所のプライバシーと PII に関する現地の法規制を確認し、遵守してください）。


アドビは、広告主がサイト訪問者やアプリケーション利用者の行動情報を収集するためのツールを提供しています。また、広告主の他の情報管理システム内にあるオフラインや外部の顧客レコードを活用して、さらに有益な情報を得るためのツールも提供しています。

広告主がこのような情報収集をする主な理由の 1 つは、消費者に合ったマーケティングや広告を展開する際に、その判断の根拠となる情報の質を高めるためです。Adobe Analytics および Target では、広告主が電子メールアドレスなどの個人情報（PII）をアップロードする前に、その情報が個人への接触に利用されないようにするためにハッシュ化をおこなうことができます。ハッシュ化されていても、その情報は引き続き分析やマーケティングに利用できます。なお、アドビは医療記録、金融口座情報、未成年に関する情報など、機密性の高い個人情報を広告主がアドビに送信することを禁止しています。

アドビは、このようなマーケティングや広告の判断が消費者のプライバシーに触れる可能性があることを理解しています。そこで、消費者の期待に添ったマーケティング活動を支援するために、プライバシーコントロールの機能を組み込んでいます。広告主は、マーケティングのために収集すべき情報の種類と、その情報の利用が認められる状況について、慎重に検討する必要があります。

**ベストプラクティス**

PII を Adobe Analytics または Target にアップロードするときには、事前にハッシュ化することをお勧めします。ハッシュ化されていても、その情報は引き続き分析やマーケティングに利用できます。なお、アドビは医療記録、金融口座情報、未成年に関する情報など、機密性の高い個人情報を広告主が Adobe Analytics に送信することを禁止しています。

広告主は、マーケティングのために収集すべき情報の種類と、その情報の利用が認められる状況について、慎重に検討する必要があります。

消費者プライバシー法はまだ流動的なので、次の 3 つの一般的なガイドラインに従うことをお勧めします。

1. プライバシーポリシーの記述に従って行動する
1. どのように行動するかをプライバシーポリシーに記述する
1. あらかじめ消費者に明示する

これらを念頭に置いた上で、広告主が閲覧アクティビティを PII に関連付ける場合は、消費者を特定していることを示す通知またはパーソナライズを提供することをお勧めします。Web サイトのヘッダーに断り書きを含めることは、この一例です。また、PII に関連付ける閲覧情報の種類と、閲覧情報を PII に関連付ける状況について、プライバシーポリシーに明記することをお勧めします。最後に、顧客に提示するオプトアウトの選択肢では、消費者が未認証のプロファイル情報投稿をオプトアウトできるかどうかと、その方法を明確に示すようにすることを強くお勧めします。

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to https://marketing.adobe.com/resources/help/en_US/mcloud/t-publish-audience-segment.html, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/ </p> -->
