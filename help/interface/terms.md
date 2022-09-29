---
description: Adobe Experience Cloud の用語と Creative Cloud での用語の違いについて説明します。
solution: Experience Cloud
title: 用語
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 3799f806-2794-43ab-9e70-06ee693871e7
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: ht
source-wordcount: '1445'
ht-degree: 100%

---

# 用語

Experience Cloud ユーザー向けの用語リファレンスと、これらの用語の Creative Cloud での用法について説明します（該当する場合）。

| 用語 | Creative Cloud | Experience Cloud |
|--- |----- |---- |
| アセット | Creative Cloud では通常、アセットは画像ファイルです。<br>Photoshop ファイルのレイヤー、PowerPoint ファイルのスライド、PDF のページおよび ZIP 内のファイルがアセットになることもあります。 | Experience Cloud では、アセットは、デジタルドキュメント、画像、ビデオまたはオーディオで、複数のレンディションを持つことができ、サブアセットを持つことができます。以下に例を示します。<ul><li>ファイル</li><li>ドキュメント</li><li>画像</li><li>Video</li><li>オーディオクリップ</li><li>プレゼンテーション</li><li>画像テンプレート</li><li>ビデオテンプレート</li></ul> |
| 属性 |  | [セグメント](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=ja)に適合する顧客の共通点です（Audience Manager の[特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-glossary.html?lang=ja)と似ています）。 |
| オーディエンス | Creative Cloud では、オーディエンスはビデオを閲覧するユーザーとすることができます。 | Experience Cloud では、Audience は、Campaign アクティビティのターゲットとなり得る人の集まりです。<br>オーディエンスのメンバーかどうかは、訪問者のコンテキストに影響を与える一連のルールまたは固定リストに基づいて判断できます。例えば、電子メール登録者のリストや、Facebook グループのメンバーなどです。<br>[Experience Cloud Audiences](audience-library.md) では、Audiences の作成と管理はセグメントの作成と使用と似ていますが、さらに Experience Cloud で共有することができます。<br>**Adobe Target**<br> Adobe Target では、Audiences は、以前セグメントと呼ばれていました。<br>**Adobe Analytics**<br> Analytics では、Audiences は Web サイトの訪問者と考えることができます。オーディエンスセグメントを作成し、オーディエンスを Experience Cloud に公開できます。 |
| キャンペーン | Creative Cloud では、キャンペーンは、Creative Cloud 画像アセットを使用するマーケティングキャンペーンと考えることができます。 | Experience Cloud では、キャンペーンは、オーディエンスにどのコンテンツを表示するかを決定します。また、コンテンツをどこ（場所）にいつ表示するかを決定します。キャンペーンには具体的な目標があり、それは指標で追跡されます。<br>キャンペーンの実行には、訪問者のコンテキストとキャンペーンのルールセットを一致させ、キャンペーンの展開先チャネルの技術上の制限に従ってコンテンツを配信する必要があります。<br>Adobe Target では、キャンペーンとアクティビティは同義語です。 |
| チャネル | Creative Cloud では、チャネルは様々な種類の情報を格納するグレースケール画像であることがあります。情報チャネルとカラーチャネルがあります。 | Experience Cloud では、チャネルは、場所の属性またはキャンペーンのアクティビティを指します。<br>Analytics では、マーケティングチャネルは、サイトに訪問者がどのように到達するか（電子メール経由など）を把握するために一般に使用されます。<br> 以下に例を示します。<ul><li>電子メール</li><li>ディスプレイ広告</li><li>SNS</li><li>有料検索</li><li>自然検索</li><li>参照ドメイン</li></ul> |
| コンテキスト | 通常は、選択または実行中のタスクに関連して使用可能なメニューまたは情報を指します。 | コンテキストは、訪問者の現在のインタラクションの詳細をデジタルプロパティと併せて説明します。コンテキストの例としては、マウスの位置、フォームフィールドの状態、買い物かごの値または使用されているデバイスがあります。<br>[Dynamic Tag Management](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja) は、今日の市場で最も堅牢なコンテキスト検出およびサービスアクティブ化機能を備え、プロファイルおよびオーディエンスサービスのコンテキストコンポーネントを提供します。 |
| 消費者 ID | 特別な用法はありません。 | 人物を認識するために、Experience Platform Co-op Graph メンバーによって使用される ID。この番号はブランドによって割り当てられ、多くの場合 CRM システムで維持管理されます。**メモ：** この ID を、消費者 ID を Experience Cloud に送信する [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/intro/about-id-service.html?lang=ja)関数呼び出しである _setCustomerIDs_ と混同しないでください。 |
| コンテンツ | Creative Cloud では、コンテンツは、ページ上のテキストと画像を指します。この用語は、Creative Clouds と Experience Clouds の間でも同じように使用されています。 | Experience Cloud ではコンテンツとはマーケティングコンテンツを指し、特定の目標を達成するためにキャンペーンの一部として使用されることがあります。<br>コンテンツは、特定の場所に使用され、アセットで構成することができます。コンテンツには、構造化されているもの（製品情報など）も、構造化されていないもの（モバイルアプリの Web ページや画面など）もあります。<br> 以下に例を示します。<ul><li>Web ページ</li><li>バナー</li><li>ステータスの更新状況</li><li>コメント</li><li>テキスト広告</li><li>製品情報</li><li>製品レビュー</li><li>フォームデータ</li><li>検索インデックス内のドキュメント</li><li>Social への投稿</li><li>記事</li><li>公開物</li></ul> |
| ダッシュボード | 特別な用法はありません。 | 複数の主要指標を 1 つのビューで表示するデータ視覚化機能の集まりです。 |
| データ使用規定 | 特別な用法はありません。 | システム（アプリケーション、アプリ、サービス、SDK、APIなど）が制定および定義する、データ使用メタデータを使用して、データ使用がアドビコーポレートのプライバシーポリシー、契約上の約因、一般的なプライバシー原則を遵守できるようにするためのポリシー、システム設計、実務および手順です。 |
| デバイス | 特別な用法はありません。 | アプリケーションが動作するハードウェアデバイス（タブレット、スマートフォン、デスクトップ PC など）。 |
| Device Co-op | 特別な用法はありません。 | 様々なデバイスにわたって個人をより正確に識別し、より有意義で一貫したエクスペリエンスを実現するために、消費者がどのデバイスを使用しているかに関するデータを共有することに同意したブランドのグループです。 |
| [!UICONTROL Experience Cloud ID サービス]（ECID） | 特別な用法はありません。 | サイト訪問者に割り当てられる一意の永続的な ID。Experience Platform ID サービスで使用できる特定のエンティティです。[詳細情報...](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja) |
| [!UICONTROL Experience Platform ID サービス] | 特別な用法はありません。 | ID をリンクするサービス。ユーザーベースのエクスペリエンス管理を実現するための、デバイスリンクサービスです。 |
| リンク | 特別な用法はありません。リンクは、ハイパーリンクナビゲーションや、フォント、プロパティ、レイヤーなどのアイテムをリンクすることを指します。 | Experience Cloud において通常、リンクとは、様々なアプリケーションアカウントをインターフェイスにリンクすることを指します。<br>[組織とアカウントのリンク](organizations.md)を参照してください。<br>リンクは、他のユーザーに送信される Analytics レポートの標準的な URL を指す場合もあります。 |
| 場所 | Creative Cloud では、場所はファイルの場所、または開いている画像やドキュメント上の場所を指します。 | Experience Cloud では、場所とは、コンテンツがオーディエンスに表示される場所のことです。Audiences とのやり取りがおこなわれる場合もあります。場所とコンテンツの関係は、ある程度静的に固定することも、キャンペーンのルールに従って動的に管理することもできます。場所は必ず、特定のチャネルに属しています。このチャネルによってコンテンツの配信方法と指標の収集方法が決まります。<br> 以下に例を示します。<ul><li>サイト</li><li>プロパティ（Social）</li><li>ディスプレイインベントリ</li><li>ランディングページ</li><li>モバイルアプリ</li><li>スロット（ビデオ）</li></ul> |
| 指標 | Creative Cloud では使用されません。 | 主要概念や目標に関する数値の集計です。Analytics では、指標は、ビュー数、選択スルー数、リロード数、平均滞在時間、数量、注文件数、売上高など、訪問者の行動に関する量的な情報を指します。 |
| 組織 | Creative Cloud では使用されません。 | 組織とは、管理者がユーザーおよび製品を設定し、Experience Cloud でのシングルサインオンを制御するために使用する Experience Cloud エンティティです。多くの場合、課金会社が組織になります。 |
| ポートフォリオ | 複数のファイルやアセットの集合です。 | キャンペーンのコンテナです。 |
| 製品プロファイル | [製品およびプロファイルの管理](https://helpx.adobe.com/jp/enterprise/using/manage-products.html)を参照してください。 | 製品またはサービスを利用する資格をユーザーに付与するには、そのユーザーを製品プロファイルに追加する必要があります。製品管理者は、購入されたプランに製品プロファイルを関連付けることによって製品プロファイルにライセンスを割り当てます。<br>ユーザーには複数の製品プロファイルを割り当てることができ、各プロファイルで異なるライセンスをユーザーに付与することができます。ユーザーの最終的な資格は、そのユーザーに割り当てられた各製品プロファイルで付与されているライセンスをすべて合わせたものとなります。 |
| スケジュール | Adobe Story の一連のシーンや、ColdFusion でスケジュールされたタスクを指すことがあります。 | Experience Cloud では、スケジュールはキャンペーン、チャネルおよびアクティビティのアクティブ化の開始日（年、月、日）と終了日を指します。アクティビティのスケジュールは、分単位の精度があります。スケジュールを変更すると、カードが作成されます。<br> 以下に例を示します。<ul><li>キャンペーンスケジュール</li><li>チャネルスケジュール</li><li>アクティビティスケジュール</li></ul> |
| セグメント | 該当なし | オーディエンスの適合性を評価する一連のルールの出力です。Analytics では、オプションで[セグメント](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=ja)を使用して、Experience Cloud に渡すことができるオーディエンスを定義できます。<br>Audience Manager では、セグメントは[特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/traits-overview.html?lang=ja)と、訪問者がそのセグメントのメンバーとして含まれるかどうかを評価するすべての条件の集まりです。また、これらの共通の属性を共有する人々の集まりでもあります。 |
| 共有 | Creative Cloud では、ファイルを外部の様々なプラットフォーム（ソーシャル、コミュニティ、電子メールなど）にまたがって共有できます。 | Experience Cloud では、インターフェイス内部のボード内で、カードのみをアセットとして共有できます。共有は、サイトにログインしているユーザーのみが利用できます。 |
| ソリューション | 特別な用法はありません。 | Experience Cloud のソリューションには、Adobe Analytics、Adobe Social、Adobe Target などの製品があります。Experience Cloud では、アプリケーションは Adobe Analytics、Adobe Social、Adobe Target などの製品として知られています。 |
| 特性 | 該当なし | キーと値のペア（例：color=blue）。 Audience Manager では、[特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/traits-overview.html?lang=ja)を使用してセグメントを作成します。 |

{style=&quot;table-layout:auto&quot;}
