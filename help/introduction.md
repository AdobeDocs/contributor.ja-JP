---
title: アドビドキュメントのコントリビューターガイド
seo-title: Adobe Experience Cloudテクニカルドキュメントの寄稿者ガイドの概要
description: このガイドでは、アドビのドキュメントサイトに提案や追加をおこなう方法について説明します。
seo-description: このガイドでは、[!UICONTROL Adobe Experience Cloud] 技術ドキュメントへのコントリビューションの方法を説明します。
translation-type: tm+mt
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---


# アドビドキュメントの寄稿者ガイドの概要

## コラボレーションドキュメントとは

2019年に、Adobe Experience Cloudの技術ドキュメントおよび有効化コンテンツはすべて、Github、markown、Adobe Experience Cloudソリューション（Adobe Experience Manager、Analytics、Launch、Targetなど）を使用して、オープンソースの原則に基づいて新しいプラットフォームへの移行中です。

このオープンソースモデルは、コンテンツの品質や顧客、ドキュメントチームおよび製品チーム間の通信を強化します。すべてのページで、コンテンツの有用性、問題のログ、コンテンツ提案をGitプルリクエスト（PrS）として利用できるようになりました。アドビのドキュメントチームは、毎日の提供状況と問題を監視し、必要に応じて更新、改善、調整を行います。

## コラボレーティブドキュメントの操作

この資料のユーザーとして、自分が従業員、パートナー、顧客、または見込み客であるかどうかにかかわらず、いくつかの簡単な方法でこのドキュメントに貢献するかどうかを選択できます。

* ページのヘルプ機能を評価する
* 特定のページに対する問題のログ
* アセットやコードサンプルを使用して、記事全体をオーサリングすることで、すばやく編集を行うこともできます

このガイドでは、操作に必要なすべての事柄について説明し、この資料セットに貢献します。

<!--
> [!IMPORTANT]
> All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
--->

## 既存ドキュメントのクイック編集

クイック編集は、ドキュメント内の小さな不備や欠落を修正するのに便利です。記事に以下のような編集ボタンが表示されている場合は、閲覧者がその場で修正できます。文書を編集するときには、修正または提案をアドビに提出するためのプルリクエスト（PR）を送信します。その提案をアドビがレビューして承認し、公開します。

1. 同意できる場合は [、寄稿者使用許諾契約（CLA）](http://opensource.adobe.com/cla.html) に署名します。

   Adobe CLAを一度に送信する必要があります。
1. 右列の ** をクリックして、GitHub の markdown ソースファイルに移動します。`Edit this page`**
1. 鉛筆アイコンをクリックして記事を編集します。

   > [!NOTE]
   > 鉛筆アイコンがグレー表示になっている場合は、GitHub アカウントにログインするか、新しいアカウントを作成する必要があります。

   ![鉛筆アイコンの場所](assets/edit-icon.png)

1. Web エディターで変更をおこないます。「**Preview changes**」タブをクリックすると、変更部分の書式を確認できます。
1. 変更を済ませたら、ページの下部までスクロールします。PR のタイトルと説明を入力し、次の図に示す「**Propose file change**」をクリックします。

   ![変更の提案](assets/submit-pull-request.png)

   >[!NOTE] 寄稿者使用許諾契約（CLA）への署名に関する検証エラーメッセージが表示されたら、「 **詳細」** をクリックして使用許諾契約書を開きます。同意できる場合は、契約に署名します。次に、プルリクエストを閉じて開き、続行します。

必要な操作は以上です。ご協力ありがとうございます。提出されたプルリクエストをドキュメントチームメンバーがレビューしてマージします。

## 問題のログ

コンテンツの一部についての問題を指摘するもう 1 つの方法は、その問題をログに記録することです。

1. コンテンツの一部に問題がある場合は、ページの右下にある「`Log an Issue`」リンクをクリックします。以下の図を参照してください。

   ![](assets/git_log_issue.png)

   > [!NOTE]
   > 問題をログに記録するには、GitHub アカウントにログインするか、新しいアカウントを作成する必要があります。

   このリンクをクリックすると、Github Issue インターフェイスを使用して、アドビ宛のクイックチケットを登録できます。

1. 問題を含むページの URL が説明フィールドに自動的に挿入されます。タイトルを入力し、問題の簡単な説明を書いてから、「*Submit new issue*」をクリックします。

   ![](assets/git_issue_example.png)

問題を送信すると、アクションを実行できるこのページのコンテンツチームに直接通知されます。担当チームがコンテンツを更新すると、Github Issues インターフェイス上で登録者に通知されます。問題に進展があるか、問題がクローズされると、電子メールで通知されます。

## GitHub の権限について

GitHub の編集 UI は、利用者のリポジトリ権限に応じて変化します。前掲の画像は、ターゲットリポジトリへの書き込み権限を持たないコントリビューターに表示されるものです。GitHub は自動的に利用者のアカウント内にターゲットリポジトリのフォークを作成します。利用者がターゲットリポジトリへの書き込み権限を持っている場合は、GitHub はターゲットリポジトリ内に新しいブランチを作成します。

アドビはすべての変更でプルリクエストを使用します。書き込み権限を持つコントリビューターによる変更でも同様です。ほとんどのリポジトリには保護された`master`ブランチがあり、アップデートはプルリクエストとして送信される必要があります。

ブラウザー内編集の機能は、小さな変更や頻繁でない変更に適しています。大きな変更を加える場合や、高度な Git 機能を使用する場合は、[リポジトリをフォークしてローカルで作業する](setup/full-workflow.md)ことをお勧めします。

## フィードバックの提供

アドビのソリューションセットのように大規模なものになると、ドキュメントは常に作業中になります。エラーを見つけた場合はログに記録し、提案がある場合はアドビまでお知らせください。どのような情報を探しているか、ご意見をお聞かせください。必要な情報が見つからない場合は、その旨をお知らせください。タスクをうまく完了できない場合は、どこがわからないかをご指摘ください。

コラボレーティブドキュメントの担当チームと [!UICONTROL Adobe Experience Cloud] のすべてのライターおよびコンテンツプロデューサーを代表して、皆様のご協力に感謝を申し上げます。