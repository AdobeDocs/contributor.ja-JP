---
title: 大きな変更をする際の GitHub コントリビューションワークフロー
description: Experience League で Adobe ドキュメントに投稿する方法について説明します。
exl-id: ad467ad4-abd2-4166-8659-e29c48d268ec
source-git-commit: a1466cb4bcbef51689c659e25d56d5cb0d4843a6
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 96%
---
# 大きな変更をする際の GitHub コントリビューションワークフロー

<!--
>[!IMPORTANT]
>All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
-->

## 概要

このワークフローは、大きな変更を加える必要があるコントリビューターや、リポジトリに頻繁にコントリビューションするコントリビューターに適しています。 頻度の高いコントリビューターは、通常は継続的な（長期にわたる）変更を取り扱います。つまり、構築／検証／ステージングのサイクルを繰り返したり、プルリクエストのサインオフや結合までに数日かかったりする変更を扱います。

### 用語

まず、このワークフローで使用される Git／GitHub の用語をいくつか確認しましょう。

| 名前 | 説明 |
|-----------|-------------|
| フォーク | 通常は名詞として使用され、メイン GitHub リポジトリのコピーを指します。 実際のところ、フォークは単にもう 1 つのリポジトリですが、 メイン（親）リポジトリとの双方向的な接続が GitHub によって維持されるという特別な性質を持ちます。 「まずリポジトリをフォークする必要があります」のように、動詞として使用される場合もあります。 |
| リモート | リモートリポジトリへの名前付きの接続です。「origin」や「upstream」などのリモートがあります。 Git でこれらの接続をリモートと呼ぶのは、別のコンピューターにホストされているリポジトリを参照するときに使用されるからです。 このワークフローでは、リモートは常に GitHub リポジトリです。 |
| origin | ローカルリポジトリと、そのクローン元のリポジトリとの間の接続に割り当てられる名前です。 このワークフローでは、オリジンは、自分のフォークへの接続を表します。 「origin に対する変更を必ずプッシュしてください」のように、origin リポジトリ自体を指す名称として使用されることもあります。 |
| upstream | origin リモートと同じく、upstream も別のリポジトリへの接続の名称です。 このワークフローでは、upstream は、ローカルリポジトリとメインリポジトリ（フォーク作成元）との間の接続を表します。 「upstream から変更を必ずプルしてください」のように、upstream リポジトリ自体を指す名称として使用されることもあります。 |

Git および GitHub のリポジトリやブランチといった概念に馴染みがない場合は、[Git および GitHub の基礎](git-fundamentals.md)をまず確認してください。

## ワークフロー

>[!IMPORTANT]
>
> [設定](github-signup.md)の手順がまだ終わっていない場合は、まずそちらを完了してください。

このワークフローでは、変更は反復的なサイクルとして実行されます。 変更は、使用しているデバイスのローカルリポジトリから、GitHub フォークに反映され、次にメインの GitHub リポジトリに反映されます。その後、再度ローカルに反映されて、他のコントリビューターの変更内容が統合されます。

### GitHub フローの使用

[Git および GitHub の基礎](git-fundamentals.md)で説明したように、Git リポジトリには、main ブランチと、まだ main に統合されていない作業中のブランチが含まれています。 論理的に関連性のある一連の変更を導入するときは、このワークフローを通して変更を管理するための&#x200B;*作業ブランチ*&#x200B;を作成することをお勧めします。 これを作業ブランチと呼ぶのは、main ブランチに統合できる状態になるまで変更の反復修正や手直しをするための作業用スペースとなるからです。

関連する変更を特定のブランチに隔離しておくと、これらの変更を独立して管理したり導入したりでき、公開サイクルの特定のリリースをターゲットにすることもできます。 おこなう作業の種類にもよりますが、実際の作業環境では、リポジトリ内に複数の作業ブランチができることがよくあります。 それぞれ別のプロジェクトの複数のブランチで同時に作業することも珍しくありません。

<!--
>[!NOTE]
>
>Making your changes in the main branch *is not a good practice*. Imagine that you use the main branch to introduce a set of changes for a timed feature release. You finish the changes and are waiting to release them. Then in the interim, you have an urgent request to fix something, so you make the change to a file in the main branch and then publish the change. In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.
-->

次に、ローカルリポジトリ内に新しい作業ブランチを作成し、ここで変更案を反映します。 Git クライアントによって作業方法が異なるので、使用するクライアントのヘルプを参照してください。 プロセスの概要については、GitHub ガイドの [GitHub フロー](https://guides.github.com/introduction/flow/)の説明を参照してください。

## プルリクエストの処理

いくつかの変更案を新しいプルリクエスト（PR）にまとめて提出します。PR は、宛先リポジトリの PR キューに追加されます。 プルリクエストは GitHub の共同作業モデルを動かすための要素です。プルリクエストを使用して、作業ブランチから変更を取得し、別のブランチに結合するよう依頼することができます。 ほとんどの場合は、メインリポジトリ内のデフォルト／ main ブランチがマージ先になります。

### 検証

プルリクエストを宛先ブランチに結合する前に、1 つ以上の PR 検証プロセスを経なければならない場合があります。 検証プロセスは、変更案の範囲や宛先リポジトリのルールに応じて異なります。 プルリクエストを提出すると、そのコンテンツがレビューされ、適宜メインリポジトリに結合されます。

### レビューとサインオフ

すべてのPR処理が完了したら、結果（PR コメント、プレビューURLなど）を確認する必要があります。 ファイルに追加の変更が必要かどうかを判断するには、結合をログオフする前にそのファイルを変更します。 PR レビュー担当者がプルリクエストをレビューする場合は、結合前に解決すべき未処理の問題や質問があるときに、コメントでフィードバックが提供されることもあります。

プルリクエストが問題のない状態でサインオフされると、変更が親ブランチに結合されて、プルリクエストがクローズされます。

### パブリッシュ

プルリクエストは、変更内容が次回の公開スケジュールに反映される前に、PR レビュアーによって結合される必要があります。 プルリクエストは、通常は提出された順序でレビューおよび結合されます。 特定のパブリッシュ実行にプルリクエストをマージする必要がある場合は、事前に PR 担当者と話し合って、パブリッシュ前にマージが確実におこなわれるようにします。
