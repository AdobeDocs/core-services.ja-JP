---
description: 1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。
seo-description: 1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。
seo-title: 組織へのレポートスイートのマッピング
title: 組織へのレポートスイートのマッピング
uuid: b983d5a6-b3d0-4137-ac53-bc5681d3e58b
translation-type: tm+mt
source-git-commit: b6ef7f0b7ef3b43b437524b20cee940889c26ba8

---


# 組織へのレポートスイートのマッピング {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。

Experience Cloudサービス（Experience Cloud IDサービスやPeopleコアサービスなど）は、個々のレポートスイートではなく、組織に関連付けられます。 これらのサービスを正しく機能させるには、各 Analytics レポートスイートを組織にマッピングする必要があります。マッピングプロセスは以下のように実行されます。

* Experience Cloud 組織をレポートスイート用の主要組織として設定します。
* レポートスイートにアクセスできるユーザーは変更されません（アクセスが可能かどうかは引き続き各ユーザーの Adobe Analytics ログインアカウントによって決定されます）。

**要件**

マッピングをおこなうには、マッピングしたいレポートスイートへのアクセス権を持つログイン会社の Analytics 管理者であることが必要です。また、このアカウントが [Experience Cloud 組織にリンクされている](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)ことが、その組織にレポートスイートをマッピングするうえで必須となります。

指定したレポートスイートへのアクセス権を持つ組織のログイン会社の Analytics 管理者権限を持っていない場合、その組織はグレー表示されます。

## 組織へのレポートスイートのマッピング {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. **[!UICONTROL Experience Cloud]** /管理/レポー **[!UICONTROL トスイ]****[!UICONTROL ートのマッピングをクリックします]**

1. 各レポートスイートにアクセスできるログイン会社を確認するには、「**[!UICONTROL 表示可能なログイン会社名]**」をクリックします。

   この画面は、十分な情報に基づいてマッピングをおこなえるようにすることを目的としています。

1. レポートスイートの横にある「**[!UICONTROL マッピングされた組織]**」列のドロップダウンリストをクリックし、マッピングする組織を選択します。

   Experience Cloud 組織の選択に関するヒントについては、次の節を参照してください。

## 組織に複数のレポートスイートをマッピングする{#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. **[!UICONTROL Experience Cloud]**／**[!UICONTROL 管理]**／**[!UICONTROL Report Suite Mapping]** をクリックします。

1. マッピングするレポートスイートを選択します。

   ![](assets/rs-mapping-multiple.png)

1. 組織（この例では Outdoors Inc）を選択し、「**[!UICONTROL 選択]**」をクリックします。

   Experience Cloud 組織の選択に関するヒントについては、次の節を参照してください。

1. 「**[!UICONTROL マッピングを保存]**」をクリックします。

## Experience Cloud 組織の選択に関するヒント {#mapping-tips}

この節では、レポートスイートをマッピングする必要がある Experience Cloud 組織を選択するうえで役立つヒントを紹介します。

**どの組織を選択すべきか**

If the Experience Cloud ID Service is currently deployed on the report suite, ensure the organization you select in the Report Suite Mapping tool is the same organization specified in the [!DNL visitorAPI.js] file on your site. [Experience Cloud ID サービスのテストと検証](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/test-verify.html)の指示に従えば、訪問者 ID サービスで使用されている組織 ID を確認できます。

レポートスイート用のデータを収集するサイト上にまだ訪問者 ID サービスがデプロイされておらず、今後 Experience Cloud 訪問者 ID サービスをデプロイする予定がある場合は、レポートスイートマッピングツールで選択した組織と一致するようにデプロイをおこなう必要があります。

**一部の組織がグレー表示されている理由**

これは、グレー表示されているレポートスイートにマッピングするために必要な権限が不足していることを示しています。次の例をご覧ください。


![](assets/rs-mapping.png)

この図では、青色の鍵が管理権限を示しています。グレーの線は可視性を示しています。

このユーザーは、2 つの Experience Cloud 組織にアクセスできます。このユーザーは以下の操作を実行しました。

* Linked his admin account in the [!UICONTROL chapek] Analytics login company to his [!UICONTROL Chapek] Corp Experience Cloud organization account.
* Linked his non-admin account in the [!UICONTROL doohan] Analytics login company to his [!UICONTROL Chapek] Corp Experience Cloud organization account.
* Analytics ログイン会社「nigel」内の自分の非管理者アカウントを Experience Cloud 組織「Nigel Inc」の自分のアカウントにリンクした。

以下は、これらのレポートスイートに関して実行できるマッピングアクションと実行できないマッピングアクションを一覧にまとめたものです。

* [!UICONTROL このユーザーはリンクされたAnalyticsログイン会社(] chapek [!UICONTROL )の管理者で、アカウントはこの組織にリンクされているので、Chapek-prodレポートスイートは] ChapekCorp組織にマッピングできます。
* [!UICONTROL このユーザーは nigel-prod レポートスイートを表示できるログイン会社の管理者ではないので、このレポートスイートをリンクすることはできません。]
* [!UICONTROL Doohan-prod] report suiteは、Experience Cloud組織にリンクされているログイン会社( [!UICONTROL chapek] )の管理者なので、Chapek Corpにマッピングできます（Doohan Analyticsログイン会社の管理者ではないことに注意）。 It is important to be aware that the [!UICONTROL doohan-prod] report suite is also eligible to be mapped to the Nigel Inc Experience Cloud org, even though this user cannot perform that mapping. In this case, both Experience Cloud organizations are displayed in the list, but [!UICONTROL Nigel Inc] is grayed out. マッピングをおこなう前に、このユーザーはログイン会社「nigel」の管理者に問い合わせて、マッピングに最適な候補はどちらの組織なのかを判断する必要があります。最初にレポートスイートを作成するときに使用した組織とは異なる組織を選択した場合、UI には「競合の可能性」警告が表示されます。

## よくある質問 {#section_099E485805994C929FF9C9F75219BEE1}

**すべてのレポートスイートが表示されないのはなぜですか。**

一部のレポートスイートは別のログイン会社で表示できる場合があります。画面上部にあるドロップダウンリストを使用すると現在のログイン会社を変更できます。

**レポートスイートのドロップダウンリストに見覚えのない組織が表示されている場合はどうすればよいですか。**

マッピング権限を持っていないレポートスイートがあったとしても、リストにはレポートスイートをマッピングできる可能性のあるすべての組織が表示されます。リスト内でグレー表示されている組織にレポートスイートをマッピングする必要があるかどうかがわからない場合は、組織の Experience Cloud 管理者に問い合わせてください。

**レポートスイートの「表示可能なログイン会社名」列に見覚えのないログイン会社が表示されている場合はどうすればよいですか。**

そのレポートスイートは別のログイン会社と共有されていて、そのログイン会社は別の Experience Cloud 組織に属していた可能性があります。

**「競合の可能性」エラーが表示され、このレポートスイートが別の組織から生成されたものであるというメッセージが表示されたのですが、これは何を意味しますか。どのような点が問題なのでしょうか。**

これは、十分な情報に基づいてレポートスイートのマッピングをおこなえるようにするための通知です。そのレポートスイートが本来は別の組織で作成されたものであり、その組織の方がマッピングに適している可能性があるという点を認識してもらうことが目的です。

**レポートスイートがマッピングされているかどうかを確認するには、どうすればよいですか。**

マッピング済みレポートスイートは編集不可能な形式で表示されます。マッピングを変更する必要がある場合は、カスタマーケアまでご連絡ください。

**Experience Cloud 組織の組織 ID しかわからない場合、組織 ID に対応する名前を調べるには、どうすればよいですか。**

組織名は「[組織とアカウントの設定](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html)」で確認できます。

**「マッピング日」列に日付が表示されています。誰がこのマッピングを実行したのでしょうか。**

Analytics インターフェイスで「レポートスイートの変更ログ」を参照することで、変更をおこなったユーザーのユーザー ID を確認できます。IMS 組織にスイートが関連付けられたことを示すイベントを探してください。
