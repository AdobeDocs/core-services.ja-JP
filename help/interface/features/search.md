---
description: CX Enterpriseの特定のアプリケーションの統合検索機能について説明します。
solution: Experience Cloud
title: Experience Cloud 統合検索
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Beginner
exl-id: 70586f18-6f84-4308-bab3-1da7fab823d6
TQID: 'https://experienceleague.adobe.com/gMxoCIKGEqZIN-DwgvSVfh36iiYLFqB58dRBfsgamBc'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:
role_v2: id:
level_v2: id:
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 639
ht-degree: 84%

---

# CX Enterpriseの[!UICONTROL Unified Search]

[!UICONTROL Unified Search]検索を使用すると、シームレスで一貫性のあるワンクリック操作で、検索可能なビジネスオブジェクトまたはエンティティを見つけることができます。 この検索では、最近アクセスしたオブジェクトも表示されます。

![オブジェクトとエンティティのグローバル検索](../assets/platform-search.png)

## [!UICONTROL Unified Search] へのアクセス

[!UICONTROL Unified Search]は、ページ上部のCX Enterprise ヘッダーのすべてのページで利用できます。 キーボードショートカット（`command /` または `ctrl /`）を使用して検索にアクセスすることもできます。

現在この機能は、次のサポート対象製品でのみ使用できます。

* Experience Platform（AEP）
* Journey Optimizer（AJO）

さらに多くのコンテンツにインデックスを作成すると、この機能は関連するアプリケーションに追加されます。

## 検索可能なオブジェクトおよびフィールド

入力中、自身が表示アクセス権を持っているオブジェクトから、一致する上位の結果が表示されます。

当社のアルゴリズムは、最も関連性の高いレコードを最初に表示します。 次のような複数の要因により、結果の順序は変わります。

機能とオブジェクトの権限
一致率
完全に一致するものがあるかどうかを確認します

CX Enterprise![&#128279;](../assets/unified-search-results.png)の[!UICONTROL Unified Search]

検索可能なビジネスオブジェクトには、次のものが含まれます。

* セグメント（名前、説明、ID）
* スキーマ（名前、説明、ID）
* データセット（名前、説明、ID）
* ソース（名前、説明、ID）
* 宛先（名前、説明、ID）
* クエリ（名前、説明、ID）
* メッセージ（名前、説明、ID）
* オファー（名前、説明、ID）
* コンポーネント（名前、説明、ID）
* ジャーニー（名前、説明、ID）

キーワードがナビゲーションページと一致する場合は、ナビゲーションページのサンプルデータセットへのクイックアクセスリンクを取得できます。 この「上位の結果」セクションには、上位 30 件の結果が表示されます。

ヘルプ記事は、Experience League と Communities からも確認できます。 自然言語のクエリがサポートされています。

例えば、_How to create a schema_&#x200B;は、_[!UICONTROL Learning]_&#x200B;の下のExperience Leagueから結果を生成します。

CX エンタープライズ ヘルプ ![&#128279;](../assets/unified-search-learning.png)の[!UICONTROL Unified Search]

検索アルゴリズムは、最も関連性の高いレコードを最初に表示します。 結果の順序は、次のような複数の要因によって異なります。

* オブジェクトにアクセスするためのユーザー権限
* 一致率
* 完全一致
* _[!UICONTROL Top Results]_&#x200B;セクションには、上位30件の結果が表示されます。

検索を絞り込むには、次のいずれかをクリックします。

* **[!UICONTROL All Learning]**: Experience Leagueで検索を開きます。
* **[!UICONTROL Show all...]**：さらに絞り込んで結果を絞り込むことができます。

## [!UICONTROL Unified Search]機能

統合検索では、次の機能を利用できます。

| 機能 | 説明 |
| ------- | ------- |
| グローバル言語サポート | グローバル検索ではクエリを理解し、ドイツ語、スペイン語、フランス語、イタリア語、日本語、韓国語、ポルトガル語、中国語での結果を生成します。 |
| 誤字許容値 | 統合検索では、高度なアルゴリズムを使用した堅牢な誤字許容値を提供します。 これらのアルゴリズムは、編集内容を計算し、適切な結果を提供します。 |
| 強調表示 | 検索応答では、検索クエリから一致するキーワードが強調表示されるため、クエリに一致するセクションや単語を簡単に見つけることができます。 強調表示は、スペルミスのある単語にも機能します。 |
| スニペット | 検索応答で、結果のスニペットを確認できます。 スニペットは、一致する単語と、一致するキーワードの前後のコンテンツを返します。 |
| ストップワード | 英語でよく使用する単語の一部は、_ストップワード_&#x200B;として定義されています。 ストップワードが検索クエリに含まれる場合は、それらに与えられる重み付けは低くなります。 <br>ストップワードの対象語： _a、an、and、are、as、at、be、but、by、for、if、in、into、is、it、no、not、of、on、or、such、that、the、their、then、there、these、they、this、to、was、will、 with_。 <br>ストップワードは、他のグローバル言語ではサポートされていません。 |
| 自然言語クエリ | Experience League コミュニティでヘルプ記事やディスカッションを検索する際に、自然言語を使用して質問を入力し、回答を得ることができます。 検索例：「スキーマを作成するにはどうすればよいですか？」 |
| 引用符で囲まれた完全一致検索 | クエリで引用符を使用して、完全一致検索を実行できます。 完全一致クエリに対しては、誤字修正は行われません。 例：「Luma ジャーニー 2022」。 |
| フィルター | _オブジェクトタイプ_&#x200B;などのフィルターや、その他のオブジェクト固有のフィルターを完全な検索結果のポップアップに適用できます。 検索クエリを入力した後に Enter キーを押すと、フルページのポップアップが開き、そのフィルターもポップアップに含まれます。 |

{style="table-layout:auto"}

## 見つからない場合は、

次のヒントを試してみてください。

* より具体的な検索語句を入力する
* スペルを確認する
* 検索語句全体を記述してみる
* 検索するオブジェクトへの権限があることを確認する

