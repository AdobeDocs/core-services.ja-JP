---
description: 1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。
seo-description: 1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。
seo-title: 組織へのレポートスイートのマッピング
title: 組織へのレポートスイートのマッピング
uuid: b983d5a6-b3d0-4137-ac53-bc5681d3e58b
translation-type: tm+mt
source-git-commit: 31811e718be130612c8688e80084cb7579e94f47

---


# 組織へのレポートスイートのマッピング {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

1 つまたは複数のレポートスイートを組織にマッピングする方法について説明します。

Experience Cloudサービス(Experience Cloud IDサービスや [!UICONTROL People])は、個々のレポートスイートではなく、組織に関連付けられます。 これらのサービスを正しく機能させるには、各 Analytics レポートスイートを組織にマッピングする必要があります。マッピングプロセス：

* Experience Cloud組織をレポートスイートの主な組織として設定します。
* レポートスイートにアクセスできるユーザーは変更されません（アクセスは、各ユーザーのAdobe Analyticsログインアカウントによって決まります）。

## 要件

マッピングするレポートスイートにアクセスできるログイン会社のAnalytics管理者である必要があります。 さらに、レポートスイートをその組織にマッピングするには、このアカウントをExperience Cloud組織 [(Experience Cloud組織](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1) )にリンクする必要があります。

指定したレポートスイートへのアクセス権を持つ組織のログイン会社の Analytics 管理者権限を持っていない場合、その組織はグレー表示されます。

## 組織へのレポートスイートのマッピング {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. **[!UICONTROL Experience Cloud]** / **[!UICONTROL 管理]** / **[!UICONTROL レポートスイートのマッピングをクリックします。]**

1. 各レポートスイートにアクセスできるログイン会社を確認するには、「**[!UICONTROL 表示可能なログイン会社名]**」をクリックします。

   この画面は、十分な情報に基づいてマッピングをおこなえるようにすることを目的としています。

1. レポートスイートの横にある「**[!UICONTROL マッピングされた組織]**」列のドロップダウンリストをクリックし、マッピングする組織を選択します。

   Experience Cloud 組織の選択に関するヒントについては、次の節を参照してください。

## 組織に複数のレポートスイートをマッピングする{#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. **[!UICONTROL Experience Cloud]** / **[!UICONTROL 管理]** / **[!UICONTROL レポートスイートのマッピングをクリックします]**。

1. マッピングするレポートスイートを選択します。

   ![](assets/rs-mapping-multiple.png)

1. 組織（この例では Outdoors Inc）を選択し、「**[!UICONTROL 選択]**」をクリックします。

   Experience Cloud 組織の選択に関するヒントについては、次の節を参照してください。

1. 「**[!UICONTROL マッピングを保存]**」をクリックします。

## Experience Cloud 組織の選択に関するヒント {#mapping-tips}

この節では、レポートスイートのマッピング先のExperience Cloud組織を選択する際に役立つヒントについて説明します。

### どの組織を選択すればよいですか。

If the Experience Cloud ID Service is currently deployed on the report suite, ensure the organization you select in the Report Suite Mapping tool is the same organization specified in the [!DNL visitorAPI.js] file on your site. You can use the instructions in [Test and Verify the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/test-verify.html) to find the org ID that is being used by the Visitor ID service.

レポートスイートのデータを収集するサイトに訪問者IDサービスがまだデプロイされていない場合、将来Experience Cloud訪問者IDサービスをデプロイするには、レポートスイートマッピングツールで選択した組織とデプロイが一致するようにする必要があります。

### 一部の組織が灰色表示になっているのはなぜですか。

これは、グレーアウトのレポートスイートにマップするのに十分な権限がないことを示します。 次の例をご覧ください。


![](assets/rs-mapping.png)

この図では、青色の鍵が管理権限を示しています。灰色の線は表示/非表示を示します。

このユーザーは、2つのExperience Cloud組織にアクセスできます。 彼は以下のことを行った。

* Analyticsログイン会社の管理者アカウントを [!UICONTROL Chapek] Corp Experience Cloud組織アカウントにリンクしました。
* Doohan [!UICONTROL Analyticsログイン会社の管理者以外のアカウントを] Chapek  Corp Experience Cloud組織アカウントにリンクしました。
* ニジェルAnalyticsログイン会社の管理者以外のアカウントを、Nigel Inc Experience Cloud組織のアカウントにリンクしました。

次のポイントリストは、これらのレポートスイートに関してこのユーザーが実行でき、実行できないマッピング操作を示します。

* [!UICONTROL Chapek] -prod [!UICONTROL report suiteは、] Chapek[!UICONTROL Corp組織にマッピングできます。これは、このユーザーがリンクされたAnalyticsログイン会社(]chapek)の管理者で、アカウントがこの組織にリンクされているからです。
* [!UICONTROL Nigel-prod] report suiteは、このレポートスイートが表示されるログイン会社の管理者ではないため、このユーザーはリンクできません。
* [!UICONTROL Doohan-prod] (Doohan-prod [!UICONTROL )のレポートスイートは、Experience Cloud組織にリンクされたログイン会社(] chapek[!UICONTROL )の管理者なので、]Chapek Corpにマッピングできます(Doohan Analyticsログイン会社の管理者ではないことに注意)。 このユーザーはマッピングを実行できないが、 [!UICONTROL Doohan-prod] （製品版）のレポートスイートもNigel Inc Experience Cloud組織にマッピングできる資格があることに注意してください。 この場合、両方のExperience Cloud組織がリストに表示されますが、 [!UICONTROL Nigel Inc] は灰色表示になっています。 マッピングの前に、このユーザーはニジェルログイン会社の管理者に問い合わせて、マッピングに最適な組織を決定する必要があります。 このIDは、レポートスイートが最初に作成された組織と異なる組織を選択した場合、競合の可能性を示す警告を表示します。

## よくある質問 {#section_099E485805994C929FF9C9F75219BEE1}

### すべてのレポートスイートが表示されないのはなぜですか？

一部のレポートスイートは、別のログイン会社で表示される場合があります。 画面上部のドロップダウンを使用して、現在のログイン会社を変更できます。

### レポートスイートの1つに対してドロップダウンリストに表示されている組織の一部が認識されない場合はどうなりますか。

The list shows you all the *possible* organizations your report suite could be mapped to, even you don’t have permission to map to all those report suites. レポートスイートがリスト内の灰色表示のレポートスイートの1つにマッピングされるべきかどうかがわからない場合は、組織のExperience Cloud管理者に問い合わせて、最適な選択方法を決定してください。

### 「ログイン会社に表示」列にレポートスイート用にリストされたログイン会社の一部が認識されない場合はどうなりますか。

ある時点で、このレポートスイートが別のログイン会社と共有され、別のExperience Cloud組織に属していた可能性がありました。

### 別の組織が生成するレポートスイートに関する「競合の可能性」エラーは何ですか。 なぜ重要なの？

これは、レポートスイートのマッピングに関する十分な情報に基づく決定を行うのに役立つ通知です。 このレポートスイートに対してより適切な組織が存在する場合に備えて、レポートスイートが最初に別の組織の下に作成されたことをお知らせします。

### レポートスイートがマッピングされているかどうかを知る方法を教えてください。

マッピングされたレポートスイートは、編集不可の形式で表示されます。 マッピングを変更する必要がある場合は、カスタマーケアにお問い合わせください。

### 組織IDしか知らないExperience Cloud組織の場合はどうなりますか？ 組織 ID に対応する名前を調べるには、どうすればよいですか。

組織名は、「 [組織」および「アカウント設定](https://docs.adobe.com/content/help/ja-JP/core-services/interface/manage-users-and-products/organizations.html)」で確認できます。

### 「Date Mapped」列に日付が表示されます。 誰が地図を？

Analyticsインターフェイスのレポートスイートの変更ログを参照して、変更を行ったユーザーIDを確認できます。 「IMS組織に関連付けられたスイート」というイベントを探します。
