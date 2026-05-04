---
description: Adobe CX Enterpriseの用語と、Creative Cloudでの用語の違いについて説明します。
solution: Experience Cloud
title: 用語
feature-set: Experience Cloud Services
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 3799f806-2794-43ab-9e70-06ee693871e7
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: bdea9bc8-5600-45db-b85e-d74bb59dfcff
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 581cd64936e5740d6288564abd25b5dd358f0dc6
workflow-type: tm+mt
source-wordcount: 1273
ht-degree: 68%

---

# 用語

<!--
TQID: https://experienceleague.adobe.com/6wm7HcuAbaV1iV3AgN55dY5WR---BnMM7lJgN0HZDsk
-->

CX Enterprise ユーザー向けの用語リファレンスと、これらの用語がCreative Cloudで使用される方法（該当する場合）。

| 用語 | Creative Cloud | CX Enterprise |
| --- | ----- | ---- |
| **アセット** | Creative Cloud では通常、アセットは画像ファイルです。<br>Photoshop ファイルのレイヤー、PowerPoint ファイルのスライド、PDF のページおよび ZIP 内のファイルがアセットになることもあります。 | CX Enterpriseでは、アセットとは、複数のレンディションを持つことができ、サブアセットを持つことができるデジタル文書、画像、ビデオ、またはオーディオのことです。 以下に例を示します。<ul><li>ファイル</li><li>ドキュメント</li><li>画像</li><li>ビデオ</li><li>オーディオクリップ</li><li>プレゼンテーション</li><li>画像テンプレート</li><li>ビデオテンプレート</li></ul> |
| **属性** | | [セグメント](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=ja)に適合する顧客の共通点です （Audience Manager の[特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-glossary.html?lang=ja)と似ています）。 |
| **オーディエンス** | Creative Cloud では、オーディエンスはビデオを閲覧するユーザーとすることができます。 | CX Enterpriseでは、「オーディエンス」とは、キャンペーンアクティビティでターゲットにできる人物のコレクションです。<br>オーディエンスのメンバーかどうかは、訪問者のコンテキストに影響を与える一連のルールまたは固定リストに基づいて判断できます。 例えば、電子メール登録者のリストや、Facebook グループのメンバーなどです。<br>[CX Enterprise Audiences](../services/audiences/overview.md)では、Audiencesの作成と管理は、セグメントの作成と使用に似ており、CX Enterpriseと共有する機能が追加されています。<br>**Adobe Target**<br> Adobe Targetでは、Audiencesは以前はセグメントと呼ばれていました。<br>**Adobe Analytics**<br> Analytics では、オーディエンスは web サイトの訪問者と考えることができます。 オーディエンスセグメントを作成し、CX Enterpriseにオーディエンスを公開できます。 |
| **キャンペーン** | Creative Cloud では、キャンペーンは、Creative Cloud 画像アセットを使用するマーケティングキャンペーンと考えることができます。 | CX Enterpriseでは、キャンペーンによって、オーディエンスに表示されるコンテンツが決まります。 また、コンテンツをどこ（場所）にいつ表示するかを決定します。 キャンペーンには具体的な目標があり、それは指標で追跡されます。<br>キャンペーンの実行には、訪問者のコンテキストとキャンペーンのルールセットを一致させ、キャンペーンの展開先チャネルの技術上の制限に従ってコンテンツを配信する必要があります。<br>Adobe Target では、キャンペーンとアクティビティは同義語です。 |
| **チャネル** | Creative Cloud では、チャネルは様々な種類の情報を格納するグレースケール画像であることがあります。 情報チャネルとカラーチャネルがあります。 | CX エンタープライズ版では、チャネルは場所、またはキャンペーン内のアクティビティの属性です。<br>Analytics では、マーケティングチャネルは、サイトに訪問者がどのように到達するか（メールキャンペーン経由など）を把握するために一般に使用されます。<br> 以下に例を示します。<ul><li>メール</li><li>ディスプレイ広告</li><li>SNS</li><li>有料検索</li><li>自然検索</li><li>参照ドメイン</li></ul> |
| **コンテンツ** | Creative Cloud では、コンテンツは、ページ上のテキストと画像を指します。 CreativeとCX Enterprisesでは、この用語が使用されています。 | CX エンタープライズ版では、コンテンツとは、特定の目標をサポートするために、キャンペーンの一部として使用できるマーケティングコンテンツを指します。<br>コンテンツは、特定の場所に使用され、アセットで構成することができます。 コンテンツには、構造化されているもの（製品情報など）も、構造化されていないもの（モバイルアプリの Web ページや画面など）もあります。<br> 以下に例を示します。<ul><li>Web ページ</li><li>バナー</li><li>ステータスの更新状況</li><li>コメント</li><li>テキスト広告</li><li>製品情報</li><li>製品レビュー</li><li>フォームデータ</li><li>検索インデックス内のドキュメント</li><li>Social への投稿</li><li>記事</li><li>公開物</li></ul> |
| **ダッシュボード** | 特別な用法はありません。 | 複数の主要指標を 1 つのビューで表示するデータ視覚化機能の集まりです。 |
| **データ使用の適用** | 特別な用法はありません。 | システム（アプリケーション、アプリ、サービス、SDK、APIなど）が制定および定義する、データ使用メタデータを使用して、データ使用がアドビコーポレートのプライバシーポリシー、契約上の約因、一般的なプライバシー原則を遵守できるようにするためのポリシー、システム設計、実務および手順です。 |
| **デバイス** | 特別な用法はありません。 | アプリケーションが動作するハードウェアデバイス（タブレット、スマートフォン、デスクトップ PC など）。 |
| **Device Co-op** | 特別な用法はありません。 | 様々なデバイスにわたって個人をより正確に識別し、より有意義で一貫したエクスペリエンスを実現するために、消費者がどのデバイスを使用しているかに関するデータを共有することに同意したブランドのグループです。 |
| **[!UICONTROL CX Enterprise ID Service]（ECID）** | 特別な用法はありません。 | サイト訪問者に割り当てられる一意の永続的な ID。 Experience Platform ID サービスで使用できる特定のエンティティです。 [詳細情報...](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja) |
| **[!UICONTROL Experience Platform Identity Service]** | 特別な用法はありません。 | ID をリンクするサービス。 ユーザーベースのエクスペリエンス管理を実現するための、デバイスリンクサービスです。 |
| **リンク** | 特別な用法はありません。 リンクは、ハイパーリンクナビゲーションや、フォント、プロパティ、レイヤーなどのアイテムをリンクすることを指します。 | CX Enterpriseでは、通常、リンクとは、異なるアプリケーションアカウントをインターフェイスにリンクすることを指します。<br>[組織とアカウントのリンク](../administration/organizations.md)を参照してください。<br>リンクは、他のユーザーに送信される Analytics レポートの標準的な URL を指す場合もあります。 |
| **場所** | Creative Cloud では、場所はファイルの場所、または開いている画像やドキュメント上の場所を指します。 | CX Enterpriseでは、場所とは、オーディエンスがコンテンツを閲覧している（および操作できる）場所です。 場所とコンテンツの関係は、ある程度静的に固定することも、キャンペーンのルールに従って動的に管理することもできます。 場所は必ず、特定のチャネルに属しています。このチャネルによってコンテンツの配信方法と指標の収集方法が決まります。<br> 以下に例を示します。<ul><li>Sites</li><li>プロパティ（Social）</li><li>ディスプレイインベントリ</li><li>ランディングページ</li><li>モバイルアプリ</li><li>スロット（ビデオ）</li></ul> |
| **指標** | Creative Cloud では使用されません。 | 主要概念や目標に関する数値の集計です。 Analytics では、指標は、ビュー数、選択スルー数、リロード数、平均滞在時間、数量、注文件数、売上高など、訪問者の行動に関する量的な情報を指します。 |
| **組織** | Creative Cloud では使用されません。 | 組織とは、管理者がユーザーと製品を設定し、CX Enterpriseでのシングルサインオンを制御できるようにするCX Enterprise エンティティのことです。 多くの場合、課金会社が組織になります。 |
| **Portfolio** | 複数のファイルやアセットの集合です。 | キャンペーンのコンテナです。 |
| **製品プロファイル** | [製品およびプロファイルの管理](https://helpx.adobe.com/jp/enterprise/using/manage-products.html)を参照してください。 | 製品またはサービスを利用する資格をユーザーに付与するには、そのユーザーを製品プロファイルに追加する必要があります。 製品管理者は、製品プロファイルを購入したプランに関連付けて、製品プロファイルにライセンスを割り当てます。<br> ユーザーは複数の製品プロファイルに属することができ、それぞれが異なるライセンスをユーザーに提供します。 ユーザーの最終的な実施要件は、そのユーザーに割り当てられた各製品プロファイルで付与されているライセンスをすべて合わせたものとなります。 |
| **スケジュール** | Adobe Story の一連のシーンや、ColdFusion でスケジュールされたタスクを指すことがあります。 | CX Enterpriseでは、スケジュールは、キャンペーン、チャネル、アクティビティをアクティブ化するための開始日（年、月、日）と終了日です。 アクティビティのスケジュールは、分単位の精度があります。 スケジュールを変更すると、カードが作成されます。<br> 以下に例を示します。<ul><li>キャンペーンスケジュール</li><li>チャネルスケジュール</li><li>アクティビティスケジュール</li></ul> |
| **セグメント** | 該当なし | オーディエンスの適合性を評価する一連のルールの出力です。 Analyticsでは、[&#x200B; セグメント &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=ja)をオプションで使用して、CX Enterpriseに渡すことができるオーディエンスを定義できます。 <br>Audience Manager では、セグメントは[特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/traits-overview.html?lang=ja)と、訪問者がそのセグメントのメンバーとして含まれるかどうかを評価するすべての条件の集まりです。 また、これらの共通の属性を共有する人々の集まりでもあります。 |
| **共有** | Creative Cloud では、ファイルを外部の様々なプラットフォーム（ソーシャル、コミュニティ、電子メールなど）にまたがって共有できます。 | CX Enterpriseでは、インターフェイス内のボード内で、アセットをカードとしてのみ共有できます。 共有は、サイトにログインしているユーザーのみが利用できます。 |
| **ソリューション** | 特別な用法はありません。 | CX Enterpriseでは、アプリケーションはAdobe Analytics、Adobe Targetなどの製品として知られています。 |
| **特性** | なし | キーと値のペア（例：color=blue）。 Audience Manager では、[特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/traits-overview.html?lang=ja)を使用してセグメントを作成します。 |

{style="table-layout:auto"}

