---
description: Experience Cloud の特定のアプリケーション向け統合検索機能について説明します。
solution: Experience Cloud
title: Experience Cloud 統合検索
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Beginner
exl-id: 70586f18-6f84-4308-bab3-1da7fab823d6
TQID: https://experienceleague.adobe.com/xE4H6kdjbKSwVygCsOV4zTBqPoBHAVMHfJMyYOummg0
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 5354e3c8a48184315ca4eaa8c8de1d12493cc227
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 88%

---

# Experience Cloud の [!UICONTROL Unified Search]

[!UICONTROL Unified Search] 検索を使用すると、一貫性のあるシームレスなワンクリックエクスペリエンスで、検索可能なビジネスオブジェクトやエンティティを見つけることができます。 この検索では、最近アクセスしたオブジェクトも表示されます。

![オブジェクトとエンティティのグローバル検索](../assets/platform-search.png)

## [!UICONTROL Unified Search] へのアクセス

[!UICONTROL Unified Search] は、ページ上部のExperience Cloud ヘッダーのすべてのページで使用できます。 キーボードショートカット（`command /` または `ctrl /`）を使用して検索にアクセスすることもできます。

現在この機能は、次のサポート対象製品でのみ使用できます。

* Experience Platform（AEP）
* Journey Optimizer（AJO）

さらに多くのコンテンツにインデックスを作成すると、この機能は関連するアプリケーションに追加されます。

## 検索可能なオブジェクトおよびフィールド

入力中、自身が表示アクセス権を持っているオブジェクトから、一致する上位の結果が表示されます。

当社のアルゴリズムは、最も関連性の高いレコードを最初に表示します。次のような複数の要因により、結果の順序は変わります。

機能とオブジェクト権限の
一致率
完全一致があるかどうか

Experience Cloudで ![[!UICONTROL Unified Search] う ](../assets/unified-search-results.png)

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

キーワードがナビゲーションページと一致する場合は、ナビゲーションページのサンプルデータセットへのクイックアクセスリンクを取得できます。この「上位の結果」セクションには、上位 30 件の結果が表示されます。

ヘルプ記事は、Experience League と Communities からも確認できます。自然言語のクエリがサポートされています。

例：_How to create a schema_ では、_[!UICONTROL Learning]_の下にExperience Leagueから結果が生成されます。

Experience Cloud ヘルプの ![[!UICONTROL Unified Search] を参照してください ](../assets/unified-search-learning.png)

検索アルゴリズムは、最も関連性の高いレコードを最初に表示します。結果の順序は、次のような複数の要因によって異なります。

* オブジェクトにアクセスするためのユーザー権限
* 一致率
* 完全一致
* _[!UICONTROL Top Results]_のセクションには、上位 30 件の結果が表示されます。

検索を絞り込むには、次のいずれかをクリックします。

* **[!UICONTROL All Learning]**：検索をExperience Leagueで開きます。
* **[!UICONTROL Show all...]**：結果をさらに絞り込んだりフィルターしたりできます。

## [!UICONTROL Unified Search] の機能

統合検索では、次の機能を利用できます。

| 機能 | 説明 |
| ------- | ------- |
| グローバル言語サポート | グローバル検索ではクエリを理解し、ドイツ語、スペイン語、フランス語、イタリア語、日本語、韓国語、ポルトガル語、中国語での結果を生成します。 |
| 誤字許容値 | 統合検索では、高度なアルゴリズムを使用した堅牢な誤字許容値を提供します。 これらのアルゴリズムは、編集内容を計算し、適切な結果を提供します。 |
| 強調表示 | 検索応答では、検索クエリから一致するキーワードが強調表示されるため、クエリに一致するセクションや単語を簡単に見つけることができます。 強調表示は、スペルミスのある単語にも機能します。 |
| スニペット | 検索応答で、結果のスニペットを確認できます。 スニペットは、一致する単語と、一致するキーワードの前後のコンテンツを返します。 |
| ストップワード | 英語でよく使用する単語の一部は、_ストップワード_&#x200B;として定義されています。 ストップワードが検索クエリに含まれる場合は、それらに与えられる重み付けは低くなります。<br>ストップワードの対象語： _a、an、and、are、as、at、be、but、by、for、if、in、into、is、it、no、not、of、on、or、such、that、the、their、then、there、these、they、this、to、was、will、 with_。<br>ストップワードは、他のグローバル言語ではサポートされていません。 |
| 自然言語クエリ | Experience League コミュニティでヘルプ記事やディスカッションを検索する際に、自然言語を使用して質問を入力し、回答を得ることができます。 検索例：「スキーマを作成するにはどうすればよいですか？」 |
| 引用符で囲まれた完全一致検索 | クエリで引用符を使用して、完全一致検索を実行できます。 完全一致クエリに対しては、誤字修正は行われません。 例：「Luma ジャーニー 2022」。 |
| フィルター | _オブジェクトタイプ_&#x200B;などのフィルターや、その他のオブジェクト固有のフィルターを完全な検索結果のポップアップに適用できます。検索クエリを入力した後に Enter キーを押すと、フルページのポップアップが開き、そのフィルターもポップアップに含まれます。 |

{style="table-layout:auto"}

## 見つからない場合は、

次のヒントを試してみてください。

* より具体的な検索語句を入力する
* スペルを確認する
* 検索語句全体を記述してみる
* 検索するオブジェクトへの権限があることを確認する

