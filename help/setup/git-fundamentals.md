---
title: Git および GitHub のドキュメントの基礎
description: この記事では、Git、GitHub リポジトリ、コンテンツの編成方法と、アドビのドキュメントで使用される命名規則の概要について説明します。
exl-id: 2b2ec764-4201-4bcd-802d-a034d6675793
source-git-commit: 90122796acee9214ba96360eb7b5ff5c321a4bd6
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 100%

---

# Git および GitHub のドキュメントの基礎

## 概要

記事のテキストのみを一部変更するだけの場合は、この記事の詳細を理解する必要はありません。この記事では、新規記事の作成、画像の追加、アドビのドキュメントに対する継続的な編集といった大きな変更を加える際のワークフローについて説明します。

アドビのドキュメントにコントリビューションする際には、複数のツールおよびプロセスを利用することができます。他のコントリビューターと並行して、同じプロジェクトの、場合によってはまったく同じコンテンツに対して、同時に作業をすることもできます。この機能は Git と GitHub ソフトウェアによって実現されています。

Git は共同作業を可能にするオープンソースのバージョン管理システムです。*リポジトリ*&#x200B;内のファイルに対して、複数のコントリビューターが作業することができます。

GitHub は Git リポジトリをホスティングする Web サービスであり、[docs.adobe.com](https://docs.adobe.com) のコンテンツを保管する目的などに使用されます。どのプロジェクトでも、GitHub にはメインリポジトリがホストされます。コントリビューターはここからリポジトリのコピーを作成して、自分の作業をおこなうことができます。

## Git

Git では、分散モデルをサポートするために独自のコントリビューションワークフローと用語が使用されます。例えば、通常のチェックイン／チェックアウト操作につきもののファイルロック機能がありません。Git では、より細かいレベルで変更の競合を解決するために、ファイルをバイト単位で比較します。

さらに、プロジェクトのコンテンツを保管および管理するために、次のような階層構造を使用します。

- *リポジトリ*：英語では *repo* と表記されることもあります。保管の最上位レベルの単位です。1 つのリポジトリに 1 つ以上のブランチが含まれています。
- *ブランチ*：各リポジトリには、デフォルトブランチ（一般的な名称は「main」）と、main ブランチにマージされる予定の 1 つ以上のブランチが含まれています。main ブランチは最新バージョンであり、コンテンツがパブリッシュされるときには main ブランチがソースになります。このブランチは、リポジトリ内の他のすべてのブランチの親になります。

コントリビューターは、ローカルと GitHub の両方のレベルで Git を使用してリポジトリの更新および操作をおこないます。

- ローカルのレベルでは、GitHub Desktop などのツールを使用します。
- [www.github.com](https://www.github.com) は統合されている Git の機能を使用して、メインリポジトリに書き戻されるコントリビューションの紐付けを行います。

## GitHub

すべてのワークフローは GitHub レベルを始点および終点とします。ここにアドビの全ドキュメントプロジェクトのメインリポジトリが保管されています。コントリビューターが作成する作業用コピーは複数のコンピューターに分散しています。これらのコピーが最終的に紐付けられて、プロジェクトのメイン GitHub リポジトリに反映されます。

### ディレクトリ編成

プロジェクトのデフォルト／main ブランチは、プロジェクトのコンテンツの最新バージョンとなります。main ブランチとそこから作成されたブランチ内のコンテンツは、記事のトピックの構造に従って編成されます。コンテンツおよび画像アセットを編成するために、サブディレクトリが使用されます。

メインの `help` ディレクトリは、通常はリポジトリのルートの直下にあります。この記事ディレクトリには、一連のサブディレクトリが含まれています。サブディレクトリ内の記事は、*.md* の拡張子を使用する Markdown ファイルとして作成されます。

このディレクトリのルートには、サービスまたは製品全体に関連する一般的な記事が配置されます。通常は、さらにこの下に、機能／サービスまたは一般的なシナリオに対応する一連のサブディレクトリがあります。

### Assets ディレクトリ

ユーザーガイドのディレクトリには、ディレクトリ内で参照される画像ファイル用の `/assets` サブディレクトリが含まれています。

<!--

### Markdown file template

For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`. You can use this template file as a "starter file" if you need to create a new article for submission to the repository. The file contains:

- A **metadata header** at the top of the file, delineated by two, 3-hyphen lines. It contains the various tags used for tracking information related to the article. It also includes SEO optimizations and reporting processes that Adobe uses to evaluate the performance of the content. So the metadata is important!
- Various **examples of using Markdown** to format the elements of an article.
- General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.
- Examples of **embedding video** by using an iframe.
- General **instructions on the use of docs.adobe.com extensions**, which you can use for special controls such as buttons and selectors.

-->

## プルリクエスト

*プルリクエスト*&#x200B;は、コントリビューターがデフォルトブランチへの変更を提案するための方法です。変更（*コミット*&#x200B;とも呼ばれます）はコントリビューターのブランチに保存されるので、GitHub はまず、その変更をデフォルトブランチに&#x200B;*マージ*&#x200B;した場合の影響をモデル化することができます。また、プルリクエストは、コントリビューターに構築／検証プロセス（プルリクエストのレビュー担当者）からのフィードバックを提供するための仕組みでもあります。これにより、デフォルトブランチに変更をマージする前に、潜在的な問題や質問を解決することが可能になります。

プルリクエストを通じてコントリビューションするには 2 つの方法があり、提案する変更の種類に応じて使い分けます。詳しくは、このガイドの [GitHub ワークフロー](local-repo.md)の節で説明します。
