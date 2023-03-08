---
description: Adobe Target で Cookie を使用して、どのオンラインコンテンツおよびオファーが訪問者に対してより関連性が高いかを web サイトオペレーターがテストできるようにする方法について説明します。
solution: Experience Cloud,Analytics,Target
title: Adobe Target の cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 323a8a6f53e659369df867f19170c199aee3ac40
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 89%

---

# Adobe Target の cookie {#target-cookies}

Adobe Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。

cookie の期間を除き、必要に応じてこれらの設定を変更できます。 cookie の設定を変更する場合は、アカウント担当者にお問い合わせください。

>[!NOTE]
>
>Adobe Target ユーザーは、カスタマイズされたサードパーティ cookie を作成することもできます。

| 設定 | 情報 |
| --- | --- |
| cookie 名 | mbox です。 |
| cookie ドメイン | mbox を扱うドメインの 2 番目および最上位のレベルです。会社のドメインなので、cookie はファーストパーティ cookie になります。例：`mycompany.com`。 |
| サーバードメイン | `clientcode.tt.omtrdc.net`。[!DNL Adobe Target]アカウントのクライアントコードを使用します。 |
| cookie の期間 | cookie が訪問者のブラウザーに残る期間は、訪問者が最後にログインしてから 2 年間です。cookie の期間は変更できません。 |

{style="table-layout:auto"}

>[!NOTE]
>
>ドメイン名に `mycompany.co.uk` のような国コードが含まれている場合は、クライアントサービスにお問い合わせの上、このコードをサポートするように `at.js` を設定してください。

cookie には、訪問者が Adobe Target キャンペーンをエクスペリエンスとして体験する方法を管理するためにいくつかの値が保持されています。

| 値 | 定義 |
| --- | --- |
| session ID | 特定のユーザーセッションの一意の ID。デフォルトでは、セッションは 30 分間無操作状態が続くと有効期限が切れます。sessionId を自分で生成する場合（例えば、サーバーサイド実装の場合）は、以下を確認します。<ul><li>セッション ID には、スペース、疑問符（？）、またはスラッシュ（ / ）以外の印刷可能な文字列を使用できます。</li><li>セッション ID の長さは 1～128 文字にする必要があります。</li><li>特定のセッションでは、その値は複数のリクエスト間で同じにする必要があります</li><li>特定の訪問者に対して、どの時点でも並列セッション（個別の sessionIds）を使用しないでください。</li></ul>エッジクラスター内の特定のノードへのルーティングは、セッション ID を使用して行われます。<ul><li>セッションは、サーバサイドで 30 分間アクティブです。したがって、特定の `tntId/thirdPartyId` が `tntId/thirdPartyId`. そうしないと、プロファイルに対する変更に一貫性がなく、予測できないことがあります。</li><li>新しいセッション ID は、訪問者が 30 分間操作を実行しなかった場合に使用する必要があります。</li><li>同じセッション ID を複数の `tntIds/thirdPartyIds` と共に使用すると、`tntId/thirdPartyIDs` で識別されるプロファイルに予期しない変更が加えられる可能性があります。</li></ul>**注意**：特定のセッション ID の [同時リクエスト数の制限](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=ja#content-delivery) を参照してください。 |
| pc ID | 訪問者のブラウザーの半永久的な ID です。cookie が手動で削除されるまで存続します。 |
| check | 訪問者が cookie をサポートするかどうかを判別するために使用される簡単なテスト値。訪問者がページをリクエストするたびに設定されます。 |
| disable | 訪問者の読み込み時間が at.js ファイルで設定されているタイムアウトを超えた場合に設定されます。デフォルトでは、このタイムアウトは 1 時間続きます。 |

{style="table-layout:auto"}
