---
description: 1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。
seo-description: 1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。
seo-title: 組織へのレポートスイートのマッピング
title: 組織へのレポートスイートのマッピング
uuid: b983d5a6-b3d0-4137-ac53-bc5681d3e58b
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# 組織へのレポートスイートのマッピング {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。

Experience Cloudサービス（Experience Cloud IDサービスやPeopleコアサービスなど）は、個々のレポートスイートではなく、組織に関連付けられます。 これらのサービスを正しく機能させるには、各 Analytics レポートスイートを組織にマッピングする必要があります。マッピングプロセス：

* Experience Cloud組織をレポートスイートのプライマリ組織として設定します。
* レポートスイートにアクセスできるユーザーは変更されません（アクセスは、各ユーザーのAdobe Analyticsログインアカウントによって決まります）。

## 要件

マッピングするレポートスイートにアクセスできるログイン会社のAnalytics管理者である必要があります。 さらに、レポートスイートをその組 [織にマッピングするには](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1) 、このアカウントをExperience Cloud組織にリンクする必要があります。

指定したレポートスイートへのアクセス権を持つ組織のログイン会社の Analytics 管理者権限を持っていない場合、その組織はグレー表示されます。

## 組織へのレポートスイートのマッピング {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. **[!UICONTROL Experience Cloud]** /管理/レポー **[!UICONTROL トスイ]****[!UICONTROL ートのマッピングをクリックします]**

1. 各レポートスイートにアクセスできるログイン会社を確認するには、「**[!UICONTROL 表示可能なログイン会社名]**」をクリックします。

   この画面は、十分な情報に基づいてマッピングをおこなえるようにすることを目的としています。

1. レポートスイートの横にある「**[!UICONTROL マッピングされた組織]**」列のドロップダウンリストをクリックし、マッピングする組織を選択します。

   Experience Cloud 組織の選択に関するヒントについては、次の節を参照してください。

## 組織に複数のレポートスイートをマッピングする{#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. **[!UICONTROL Experience Cloud]** /管理/レポー **[!UICONTROL トスイ]** ートのマッピングをクリックします ****。

1. マッピングするレポートスイートを選択します。

   ![](assets/rs-mapping-multiple.png)

1. 組織（この例では Outdoors Inc）を選択し、「**[!UICONTROL 選択]**」をクリックします。

   Experience Cloud 組織の選択に関するヒントについては、次の節を参照してください。

1. 「**[!UICONTROL マッピングを保存]**」をクリックします。

## Experience Cloud 組織の選択に関するヒント {#mapping-tips}

この節では、レポートスイートのマッピング先のExperience Cloud組織を選択する際に役立つヒントについて説明します。

### 私はどの組織を選べばよいですか？

If the Experience Cloud ID Service is currently deployed on the report suite, ensure the organization you select in the Report Suite Mapping tool is the same organization specified in the [!DNL visitorAPI.js] file on your site. You can use the instructions in [Test and Verify the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/test-verify.html) to find the org ID that is being used by the Visitor ID service.

訪問者IDサービスが、レポートスイートのデータを収集するサイトにまだ導入されていない場合、将来Experience Cloud訪問者IDサービスを導入する場合は、導入が、レポートスイートマッピングツールで選択した組織と一致することを確認する必要があります。

### 一部の組織が灰色表示になっているのはなぜですか。

これは、灰色表示のレポートスイートにマッピングする権限がないことを示します。 次の例をご覧ください。


![](assets/rs-mapping.png)

この図では、青色の鍵が管理権限を示しています。灰色の線は表示/非表示を示します。

このユーザーは、2つのExperience Cloud組織にアクセスできます。 彼は次のことを行った。

* Chapek [!UICONTROL Analyticsログイン会社の管理者アカウントを] Chapek  Corp Experience Cloud組織アカウントにリンクしました。
* Doohan [!UICONTROL Analyticsログイン会社の管理者以外のアカウントを] Chapek  Corp Experience Cloud組織のアカウントにリンクしました。
* Nigel Analyticsログイン会社の管理者以外のアカウントをNigel Inc Experience Cloud組織のアカウントにリンクしました。

次のポイントリストは、このユーザーがこれらのレポートスイートに対して実行できるマッピング操作と実行できないマッピング操作です。

* [!UICONTROL このユーザーはAnalyticsのリンクされたログイン会社(] chapek [!UICONTROL )の管理者で、アカウントはこの組織にリンクされているので、Chapek-prodレポートスイートは] ChapekCorp組織にマッピングできます。
* [!UICONTROL このレポートスイートは] 、このレポートスイートが表示されるログイン会社の管理者ではないので、Nigel-prodレポートスイートをこのユーザーがリンクすることはできません。
* [!UICONTROL Doohan] -prodレポートスイートは、Experience Cloud組織にリンクされたログイン会社( [!UICONTROL chapek] )の管理者であるため、Chapek Corpにマッピングできます(Doohan Analyticsログイン会社の管理者ではないことに注意)。 Doohan-prod  (Doohan-prod)レポートスイートもNigel Inc Experience Cloud組織にマッピングできる資格があることに注意してください。ただし、このユーザーはこのマッピングを実行できません。 この場合、両方のExperience Cloud組織がリストに表示されますが、 [!UICONTROL Nigel Inc] は灰色表示になっています。 マッピングを行う前に、このユーザーはニジェルのログイン会社の管理者に問い合わせて、マッピングに最も適した組織を判断する必要があります。 UIには、この組織が最初にレポートスイートが作成された組織と異なる組織を選択した場合に、競合の可能性に関する警告が表示されます。

## よくある質問 {#section_099E485805994C929FF9C9F75219BEE1}

### すべてのレポートスイートが表示されないのはなぜですか。

一部のレポートスイートは、別のログイン会社で表示。 現在のログイン会社は、画面の上部にあるドロップダウンを使用して変更できます。

### レポートスイートの1つのドロップダウンに表示される組織が一部認識されない場合はどうなりますか。

The list shows you all the *possible* organizations your report suite could be mapped to, even you don’t have permission to map to all those report suites. レポートスイートをリスト内の灰色表示のレポートスイートの1つにマッピングする必要があるかどうかがわからない場合は、組織のExperience Cloud管理者に問い合わせて、最適な選択肢を決定してください。

### 「ログイン会社を表示」列にレポートスイート用のログイン会社の一部が表示されない場合はどうなりますか。

ある時点で、このレポートスイートは別のログイン会社と共有され、別のExperience Cloud組織の一部である可能性がありました。

### 別の組織が生成するレポートスイートに関する「競合の可能性」エラーは何ですか。 なぜ重要なの？

これは、レポートスイートのマッピングに関する十分な情報に基づく決定を行うのに役立つ通知です。 組織がこのレポートスイートに対してより適切である可能性がある場合に備えて、レポートスイートが最初に別の組織の下に作成されたことをお知らせします。

### レポートスイートがマッピングされているかどうかを知る方法を教えてください。

マップされたレポートスイートは編集不可の形式で表示されます。 マッピングを変更する必要がある場合は、カスタマーケアにお問い合わせください。

### Experience Cloud組織の組織IDのみを知っている場合はどうなりますか？ 組織 ID に対応する名前を調べるには、どうすればよいですか。

組織名は、「組織とアカウントの設 [定」で確認できます](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html)。

### 「Date Mapped」列に日付が表示されます。 誰が地図を？

Analyticsインターフェイスのレポートスイートの変更ログを参照して、変更を加えたユーザーIDを確認できます。 「IMS組織に関連付けられたイベント」を探します。
