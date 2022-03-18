---
description: Experience Cloudの特定のアプリケーションに対する統合検索機能について説明します。
solution: Experience Cloud
title: 'Experience Cloud統合検索 '
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Beginner
source-git-commit: 7e7129fbf0c3407dac3a91b645bddc878b1a7d45
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 1%

---


# [!UICONTROL 統合検索] オブジェクトとエンティティ {#globally-search}

この [!UICONTROL 統合検索] 検索を使用すると、シームレスで一貫性のあるワンクリックエクスペリエンスで、検索可能なビジネスオブジェクトやエンティティを検索できます。 この検索では、最近アクセスしたオブジェクトも表示されます。

![オブジェクトとエンティティのグローバル検索](assets/platform-search.png)

## 統合検索へのアクセス

統合検索は、ページ上部のExperience Cloudヘッダーのすべてのページで使用できます。 キーボードショートカットを使用することもできます `command /` または `ctrl /` をクリックして検索にアクセスします。

この機能は、現在は次のサポート対象製品でのみ使用できます。

* Experience Platform(AEP)
* Journey Optimizer(AJO)

コンテンツのインデックスがさらに作成されると、この機能は関連するアプリケーションに追加されます。

## 検索可能なオブジェクトおよびフィールド

入力中、一致する上位の結果は、表示するアクセス権のあるオブジェクトから得られます。

アルゴリズムは、最も関連性の高いレコードを最初に表示します。 結果の順序は、次のような複数の要因によって異なります。

機能とオブジェクト権限の一致率完全一致があるかどうか

![統合検索Experience Cloud](assets/unified-search-results.png)

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

キーワードがナビゲーションページと一致する場合は、ナビゲーションページのサンプルデータセットへのクイックアクセスリンクを取得できます。 上位の結果セクションには、上位 30 件の結果が表示されます。

ヘルプ記事は、Experience Leagueとコミュニティからも入手できます。 自然言語のクエリがサポートされています。

例： _スキーマの作成方法_ 下のExperience Leagueから結果を生成する _[!UICONTROL 学習]_:

![統合検索のExperience Cloud](assets/unified-search-learning.png)

検索アルゴリズムは、最も関連性の高いレコードを最初に表示します。 結果の順序は、次のような複数の要因によって異なります。

* オブジェクトにアクセスするためのユーザー権限
* 一致率
* 完全一致
* この _[!UICONTROL 上位の結果]_ 「 」セクションには、上位 30 件の結果が表示されます。

検索を絞り込むには、次のいずれかをクリックします。

* **[!UICONTROL すべてのラーニング]**:検索をExperience Leagueで開く。
* **[!UICONTROL すべて表示…]**:結果をさらに絞り込んだりフィルターしたりできます。

## 統合検索機能

統合検索では、次の機能を使用できます。

| 機能 | 説明 |
| ------- | ------- |
| グローバル言語サポート | グローバル検索では、ドイツ語、スペイン語、フランス語、イタリア語、日本語、韓国語、ポルトガル語、中国語に関するクエリを理解し、結果を生成できます。 |
| 誤差許容値 | 統合検索では、高度なアルゴリズムを使用して堅牢なタイポトレランスを提供します。 これらのアルゴリズムは、編集内容を計算し、適切な結果を提供します。 |
| ハイライト | 検索応答では、検索クエリから一致するキーワードが強調表示され、クエリに一致するセクションや単語を簡単に見つけることができます。 ハイライトは、スペルミスのある単語に対しても機能します。 |
| スニペット | 検索応答で、結果のスニペットを確認できます。 スニペットは、一致するキーワードと一部のコンテンツを一致するキーワードに返します。 |
| ストップワード | 英語でよく使用される単語の一部は、 _言葉を止める_. ストップワードが検索クエリに含まれる場合は、より少ない重みが付与されます。 <br>ストップワードの対象： _a, a, and, a, a, at, a, a, a, a, a, a, a, a, a, in, in, i, it, no, on, on, on, on, os, a, the, ther, ther, the, ther, the, this, to, to, as, a_. <br>ストップワードは、他のグローバル言語ではサポートされていません。 |
| 自然言語クエリ | Experience Leagueコミュニティでヘルプ記事やディスカッションを検索する際に、自然言語を使用して質問を入力し、回答を得ることができます。 検索例：「スキーマを作成するにはどうすればよいですか？」 |
| 引用符で囲まれた完全一致検索 | クエリで引用符を使用して正確な検索を実行できます。 正確な一致クエリに対しては、誤植修正は行われません。 例：&quot;Lumaジャーニー2022&quot;。 |
| フィルター | 次のようなフィルターを適用できます。 _オブジェクトタイプ_ や、検索結果の完全なポップアップに対するその他のオブジェクト固有のフィルター。 検索クエリを入力した後に Enter キーを押すと、フィルターを含む完全なページのポップアップが開きます。 |

{style=&quot;table-layout:auto&quot;}

## 見つからない？

次のヒントを試してみてください。

* より具体的な検索語句を入力
* スペルを確認する
* 検索語句全体を記述してみてください
* 検索するオブジェクトに対する権限があることを確認します。










